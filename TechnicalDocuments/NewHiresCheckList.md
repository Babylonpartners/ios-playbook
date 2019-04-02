# New Hires Checklist

Prior to starting, make sure you have a Babylon GitHub account and that you have access to the following repositories:

- [babylon-ios](https://github.com/Babylonpartners/babylon-ios)
- [ios-charts](https://github.com/Babylonpartners/ios-charts)
- [ios-private-podspecs](https://github.com/Babylonpartners/ios-private-podspecs)
- [ios-build-distribution](https://github.com/Babylonpartners/ios-build-distribution)
- [ios-fastlane-match](https://github.com/Babylonpartners/ios-fastlane-match)

As an iOS Engineer, you should be in the following Slack channels:
Public:
- #ios
- #ios-build
- #ios-usa-support
- #ios-standup
- #ios-automation
- #ios-crash-reports
- #ios-recruiting

Private (ask someone to invite you):
- ios-underground
- ios-questions
- ios-sdk
- ios-oss
- ios-recruiting

Others
- demo_frontend
- developers

Apps
- pull-reminders
- peakon
- betterworks

Make sure you join your Tribe/Squad's Slack channels.

Here's how to get the iOS project up and running.

1. Globally configure Git to use SSH instead of HTTPS:
     ```
     git config --global url."git@github.com:".insteadOf "https://github.com/"
     ```
1. Install Homebrew if you don't already have it installed:    
     ```
     /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
     ```
   
1. Setup Git LFS:
     ```
     brew install git-lfs
     git lfs install
     ```
1. [Generate](https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key) & add the SSH key to your [GitHub account](https://help.github.com/en/articles/adding-a-new-ssh-key-to-your-github-account)

1. Clone the iOS repository: https://github.com/Babylonpartners/babylon-ios  
*Make sure you've already done the `Setup Git LFS` step before cloning the project.*
     ```
     git clone git@github.com:Babylonpartners/babylon-ios.git
     ```

1. Install RVM and Ruby version 2.4
     ```
     curl -sSL https://get.rvm.io | bash -s stable
     source ~/.rvm/scripts/rvm
     rvm install 2.4
     rvm use 2.4
     ```
1. Install Ruby gems (do this in the root of the project directory):
     ```
     bundle install
     ```
1. Install Cocoapods pods:
     ```
     bundle exec pod install
     ```
      It can be useful to create a command line alias for `pod` to `bundle exec pod` so that you are guaranteed to always be running the correct version of Cocoapods.
      
1. Open `Babylon.xcworkspace` in Xcode (there may be several warnings; they can be ignored). You can use `xed .` on the command line at the root of the project to open the workspace.

1. Configure the Xcode **Text Editing -> Editing** preferences as follows:
     - Automatically trim trailing whitespace
     - Including whitespace-only lines
     - Default line endings: macOS / Unix (LF)
     - Convert existing files on save
     
1. Configure the Xcode **Text Editing -> Indentation** preferences as follows:
     - Prefer indent using: Spaces
     - Tab width: 4 spaces
     - Indent width: 4 spaces
     - Tab key: Indents in leading whitespace
     
1. Compile the project 🎉

1. Add yourself to the team list in the [playbook](https://github.com/Babylonpartners/ios-playbook) by making your first PR 😉

1. Don't hesitate to create a PR with an update to this `NewHiresCheckList` if you have spotted something is missing here.
