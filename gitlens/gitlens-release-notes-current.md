---

title: GitLens Release Notes
description: GitLens Release Notes 
taxonomy:
    category: gitlens

---

Find out what’s new, what’s fixed, or just take a trip down memory lane remembering those bugs of yesterday.


Check out our [Changelog](https://github.com/gitkraken/vscode-gitlens/blob/main/CHANGELOG.md) to see linked issues and past changes.


<a href="https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens" target="_blank" class="button button--basic ">Install Current Version Now</a>

***

<a id="v13-2"></a>
## Version 13.2

### Tuesday, Dec 20th, 2022

Since the release of [GitLens 13](https://www.gitkraken.com/blog/gitlens-13), we know how the power of GitLens+ features like the Commit Graph, have been helping supercharge your dev workflow. That’s why we’re excited to present GitLens 13.2, with all new (and highly requested) Graph improvements like filtering, to quickly focus on what is most important to you. We've also streamlined the Commit Graph interface with a new header bar, providing context and quick access to switch between repositories or branches, and even fetch to keep up to date. Get ready to level up your Git game with GitLens 13.2!

<img src="/wp-content/uploads/gitlens-13.2-hero.png" class="img-responsive center img-bordered">

### Filtering

GitLens 13.2 introduces filtering , which allows you to display a subset of your graph’s information and helps you hone in on specific details of your graph that matter the most.

<img src="/wp-content/uploads/gitlens-filter-options.gif" class="img-responsive center img-bordered">

#### Filtering Capabilities

Use graph filtering in GitLens to get laser focused on the branch you're working on and its remote:

- Only Show the Current Branch
  - Display only the branch that you’re currently working on and it’s remote. In order to focus your attention on the things landing in this branch, and then quickly unfilter to "zoom" back out and see everything in flight. 

- Hide Remote Branches
  - Hides commits from the graph view that are only on remote branches.

- Hide Tags
  - Hides all tags that point to commit rows. 

- Hide Stashes
  - Hides all stash rows.

- Dim Merge Commit Rows
  - Deemphasizes merge commit rows. 

### Graph UX Improvements

We've updated the user interface, so you can get to all your favorite features even faster. Now, you can access change repo, account status, and filtering from the top of the Commit Graph page.

<img src="/wp-content/uploads/graph-ux-improvements.png" class="img-responsive center img-bordered">

### Header Updates

By merging the contextual information from the footer into the header, including the new Branch Picker and Fetch Action we’ve made it easier for you to manage your branches and work more effectively.

<img src="/wp-content/uploads/drop-down.png" class="img-responsive center img-bordered">

- Branch Picker
  - Save time, by easily selecting the branch you want from the drop down branch picker.

- Fetch Action
  - Easily keep your local repo up-to-date and in sync with the fetch action.

### Shortcut Keys

Using the new keyboard shortcuts, `SHIFT+UP` and `SHIFT+DOWN` on the Commit Graph helps you locate what you need more efficiently and effectively by staying within the branch and moving between graph rows. This can be particularly useful if you are working on a complex project with many branches.

<img src="/wp-content/uploads/shift-up-down.gif" class="img-responsive center img-bordered">

### Added
- Adds many all-new _Commit Graph_ features and improvements
  - Adds the ability to filter commits, branches, stashes, and tags
    - Adds a new _Filter Graph_ dropdown button at the start of the search bar
    - Adds ability to quickly switch between _Show All Local Branches_ and _Show Current Branch Only branch_ filtering options
      - _Show All Local Branches_ — displays all local branches (default)
      - _Show Current Branch Only_ — displays only the current branch and it's upstream remote (if exists and _Hide Remote Branches_ isn't enabled)
    - Adds ability to hide all remote branches, stashes, and tags
    - Adds the ability to dim (deemphasize) merge commits
  - Adds a new header bar to provide quick access to common actions
    - Shows the currently selected repository with the ability to switch repositories when clicked (if multiple repositories are open)
    - Shows the current branch with the ability to switch branches when clicked
    - Provides a fetch action which also shows the last fetched time
    - Also moves GitLens+ feature status and feedback links to the top right
  - Adds new ability to reorder columns by dragging and dropping column headers (not all columns are reorderable)
  - Adds new keyboard shortcuts
      - Use `shift+down arrow`  and `shift+up arrow` to move to the parent/child of the selected commit row
      - Holding the `ctrl` key with a commit row selected will highlight rows for that commit's branch
  - Adds new settings
    - Adds a `gitlens.graph.dimMergeCommits` setting to specify whether to dim (deemphasize) merge commit rows
    - Adds a `gitlens.graph.scrollRowPadding` setting to specify the number of rows from the edge at which the graph will scroll when using keyboard or search to change the selected row

### Changed
- In the _Commit Graph_, increases the time to highlight associated rows when hovering over a branch to 1s
- Removes the status bar from the _Commit Graph_ as it was replaced by the new header bar

### Fixed
- Fixes [#2394](https://github.com/gitkraken/vscode-gitlens/issues/2394) - Work in progress file diff compares working tree with working tree, instead of working tree with head
- Fixes [#2207](https://github.com/gitkraken/vscode-gitlens/issues/2207) - Error when trying to push individual commit
- Fixes [#2301](https://github.com/gitkraken/vscode-gitlens/issues/2301) - Create Worktree button doesn't work in certain cases
- Fixes [#2382](https://github.com/gitkraken/vscode-gitlens/issues/2382) - commits disappearing from commit details view when they shouldn't
- Fixes [#2318](https://github.com/gitkraken/vscode-gitlens/issues/2318) - GitLens need to login again after VS Code insiders upgrade every day
- Fixes [#2377](https://github.com/gitkraken/vscode-gitlens/issues/2377) - Missing Azure Devops Icon
- Fixes [#2380](https://github.com/gitkraken/vscode-gitlens/issues/2380) - Autolink fails with curly braces
- Fixes [#2362](https://github.com/gitkraken/vscode-gitlens/issues/2362) - Visual File History becomes unavailable when the workspace contains private repo
- Fixes [#2381](https://github.com/gitkraken/vscode-gitlens/issues/2381) - can't use scrollbar in 'Commit Graph' view
- Fixes an issue where focusout hides toolbar actions for the graph
- Fixes an issue where _Switch to Another Branch..._ doesn't work in the Graph editor toolbar
- Fixes graph issue with row highlighting/dimming sticking when the graph loses focus
- Fixes graph issue with branches remaining hovered/extended when the mouse leaves the graph

***

<a id="v13-1"></a>
## Version 13.1

### Thursday, November 17th, 2022

With GitLens 13, we released the power of GitLens+ features like the Commit Graph, Visual File History, and Worktrees to ALL users on local and public repos. No account required. Learn more about the changes happening with GitLens in this [article](https://www.gitkraken.com/blog/gitlens-13).

<img src="/wp-content/uploads/GitLens-13-1-Hero.png" class="img-responsive center img-bordered">

## Commit Graph Enhancements

### Search History

Find what you seek with ease! Quickly navigate through your search history by using the  UP⇧ or DOWN⇩ arrow keys.

<img src="/wp-content/uploads/New-Search-History.gif" class="img-responsive center img-bordered">

### New Search Filter @me

Want to see only your commits? Search For  @me to highlight only your commits.

<img src="/wp-content/uploads/atmegif.gif" class="img-responsive center img-bordered">

## Faster Interactive Rebase Editor

With GitLens 13.1, we overhauled the Interactive Rebase Editor. It is now dramatically faster, especially for large rebases. We also streamlined the user experience with a persistent header and footer to ensure you always have important context visible and can quickly start or abort the rebase. Also, anytime the commit author and committer are different, you will see both of their avatars.

<img src="/wp-content/uploads/Faster-Interactive-Rebase-Editor.png" class="img-responsive center img-bordered">

### Commit Details View Usage

Need additional details to complete your rebase more efficiently? Now, as you navigate commits, we show the selected commit details in the Commit Details view.

## Commit Details View Improvements

### Custom Autolinks

Custom and basic provider-based autolinks are now shown in the Autolinks section.

### Customizable Settings

You can now customize the Commit Details view from the GitLens Settings editor to personalize how it looks and behaves so you can focus on the most  important details.

<img src="/wp-content/uploads/commit-details-view-1.png" class="img-responsive center img-bordered">

## Terminal Links Can Use the Commit Details View

Terminal Links for commits in VS Code’s integrated terminal now use the Commit Details view to provide rich details about the selected commit.

## GitLens Home View Updates

Keeping a home tidy is important! We’ve streamlined the Home view to make it even easier to get started with GitLens, learn about its features, and how to personalize your experience.

<img src="/wp-content/uploads/New-Home-Side-Panel.png" class="img-responsive center img-bordered">

## Added 

- Adds Commit Graph enhancements
  - Adds the ability to set keyboard shortcuts to commits and stashes on the Commit Graph — closes [#2345](https://github.com/gitkraken/vscode-gitlens/issues/2345)
    - Keyboard shortcuts can be applied to many of the gitlens.graph.* commands and should use gitlens:webview:graph:focus && !gitlens:webview:graph:inputFocus for their "When Expression" to only apply when the Commit Graph is focused
    - For example, add the following to your keybindings.json to allow Ctrl+C to copy the selected commit's SHA to the clipboard
{
    "key": "ctrl+c",
    "command": "gitlens.graph.copySha",
    "when": "gitlens:webview:graph:focus && !gitlens:webview:graph:inputFocus"
}
- Automatically selects the HEAD commit in the Commit Graph when switching branches
- Improves performance of updating the Commit Graph when the repository changes
- Improves performance by avoiding unnecessary updates to the Commit Details view when selection changes
- Adds a @me search filter to the search box
- Adds history navigation to the search box in the Commit Graph
  - When the search field is focused, use the up arrow and down arrow to navigate through any previous searches that yielded results
  - Adds ability to reset to any commit in the Commit Graph and GitLens views — closes [#2326](https://github.com/gitkraken/vscode-gitlens/issues/2326)
- Adds Interactive Rebase Editor performance and UX improvements
  - Changes the header and footer to always be visible
  - Shows the Commit Details view on commit selection
    - Adds a gitlens.rebaseEditor.showDetailsView setting to specify when to show the Commit Details view for the selected row in the Interactive Rebase Editor
  - Adds full (multiline) commit message
  - Adds the f fixup shortcut key to UI
  - Consolidates the UI for author and committer information into a stack of avatars
  - Adds emoji support for commit messages — closes [#1789](https://github.com/gitkraken/vscode-gitlens/issues/1789)
  - Ensures that large rebases show rich commit details
- Adds Commit Details view improvements
  - Adds custom and non-rich integration-based autolinks and improves autolink display
  - Improves performance by avoiding unnecessary updates
  - Avoids "pinning" commits by default when opened from the Commit Graph, Visual File History, quick picks, etc
  - Adds a Open in Commit Graph button even when showing uncommitted changes
- Adds new sections and settings to the GitLens Interactive Settings
  - Adds a new Commit Details view section
  - Adds a new Terminal Links section
  - Adds autolink configuration to the Hovers section
- Adds a @me search filter to commit search in the Search & Compare view and quick pick
- Adds product usage telemetry
  - Honors the overall VS Code telemetry settings and add a gitlens.telemetry.enabled setting opt-out specifically for GitLens

## Changed

- Changes the Home view to always be available and polishes the experience
- Changes SHA terminal links to use the Commit Details view — closes [#2320](https://github.com/gitkraken/vscode-gitlens/issues/2320)
  - Adds a gitlens.terminalLinks.showDetailsView setting to specify whether to show the Commit Details view when clicking on a commit link
- Changes to uses VS Code as Git's core.editor for terminal run commands — closes [#2134](https://github.com/gitkraken/vscode-gitlens/issues/2134) thanks to PR [#2135](https://github.com/gitkraken/vscode-gitlens/pull/2135) by Nafiur Rahman Khadem [@ShafinKhadem](https://github.com/ShafinKhadem)
  - Adds a gitlens.terminal.overrideGitEditor setting to specify whether to use VS Code as Git's core.editor for GitLens terminal commands
- Polishes webview (Commit Graph, Interactive Rebase Editor, etc) scroll bars to match VS Code's style and behavior

## Fixed

- Fixes [#2339](https://github.com/gitkraken/vscode-gitlens/issues/2339) - Commit details "Autolinks" group shows wrong count
- Fixes [#2346](https://github.com/gitkraken/vscode-gitlens/issues/2346) - Multiple cursors on the same line duplicate inline annotations; thanks to PR [#2347](https://github.com/gitkraken/vscode-gitlens/pull/2347) by Yonatan Greenfeld [@YonatanGreenfeld](https://github.com/YonatanGreenfeld)
- Fixes [#2344](https://github.com/gitkraken/vscode-gitlens/issues/2344) - copying abbreviated commit SHAs is not working
- Fixes [#2342](https://github.com/gitkraken/vscode-gitlens/issues/2342) - Local remotes are incorrectly treated as private
- Fixes [#2052](https://github.com/gitkraken/vscode-gitlens/issues/2052) - Interactive Rebase fails to start when using xonsh shell due to command quoting
- Fixes [#2141](https://github.com/gitkraken/vscode-gitlens/issues/2141) - GitLens' rebase UI randomly fails loading interactive rebase when performed outside of VSC
- Fixes [#1732](https://github.com/gitkraken/vscode-gitlens/issues/1732) - Phantom rebase-merge directory (rm -rf ".git/rebase-merge")
- Fixes [#1652](https://github.com/gitkraken/vscode-gitlens/issues/1652) - Closing interactive rebase editor after "git rebase --edit" aborts rebase-in-progress
- Fixes [#1549](https://github.com/gitkraken/vscode-gitlens/issues/1549) - Fetch does not work when local branch name differs from remote branch name
- Fixes [#2292](https://github.com/gitkraken/vscode-gitlens/issues/2292) - Push button in BranchTrackingStatusNode of non-current branch does not trigger "Push force"
- Fixes [#1488](https://github.com/gitkraken/vscode-gitlens/issues/1488) - Open Folder History not working with non-English language pack
- Fixes [#2303](https://github.com/gitkraken/vscode-gitlens/issues/2303) - "Googlesource" gerrit only supports two levels of domain — thanks to PR [#2304](https://github.com/gitkraken/vscode-gitlens/pull/2304) by Matt Buckley [@Mattadore](https://github.com/Mattadore)
- Fixes [#2315](https://github.com/gitkraken/vscode-gitlens/issues/2315) - Commit details secondary side bar banner doesn't stay dismissed
- Fixes [#2329](https://github.com/gitkraken/vscode-gitlens/issues/2329) - Remember UI settings in Commit Details panel
- Fixes [#1606](https://github.com/gitkraken/vscode-gitlens/issues/1606) - Adjusts capitalization of "URL" — thanks to PR [#2341](https://github.com/gitkraken/vscode-gitlens/pull/2341) by Dave Nicolson [@dnicolson](https://github.com/dnicolson)
- Fixes issue where we weren't honoring the default gravatar style (gitlens.defaultGravatarsStyle) in certain cases
- Fixes graph issue where stashes are sometimes assigned the wrong column
- Fixes graph issue with commit rows being incorrectly hidden in some cases
- Fixes graph issue with merge commits not being hidden correctly in some cases
- Fixes some graph issues with hover on branch/tag labels


***

<a id="v13-0"></a>
## Version 13.0

### Monday, October 17th, 2022

Find what you seek. 

<img src="/wp-content/uploads/gitlens-13-social-3x.png" class="img-responsive center img-bordered">

## ✨GitLens+ Features for All on Local & Public Repos

With GitLens 13.0, we are excited to bring the power of GitLens+ features like the Commit Graph, Visual File History, and Worktrees to ALL  users on local and public repos. No account required. Learn more about the changes happening with GitLens in this [article](https://www.gitkraken.com/blog/gitlens-13).

Here’s how to get started with each of the GitLens+ features with your local or public repos:

- [Commit Graph](https://help.gitkraken.com/gitlens/gitlens-plus/#commit-graph)
- [Worktrees](https://help.gitkraken.com/gitlens/gitlens-plus/#worktrees)
- [Visual File History](https://help.gitkraken.com/gitlens/gitlens-plus/#visual-file-history)

## ✨Commit Graph  - Now out of Preview!

We’re delighted to announce that the Commit Graph is out of Preview, and is full featured! This means you may now interact with the Commit Graph directly and take actions like:

- Interact with branches, commits, tags and more with right-click context menus
- Double click a branch to checkout a branch
- Search and filter for commits
- Get information about Pull Requests

### Full context menu support

Interact with your branches, commits, and more! Context menus are now available when you right click on any branch, tag, commit, or author in the Commit Graph. You may even interact with the Commit Graph column headers to the author, date or SHA columns. So much power! 

<img src="/wp-content/uploads/Commit-Search-Context-Menus.gif" class="img-responsive center img-bordered">

Context menu actions include but are not limited to:

- Switch to Branch
- Revert Commit
- Switch to Commit
- Create Branch
- Merge
- Rebase
- Create Worktree
- Create Pull Request

### Rich commit search

Find exactly what you are looking for with the rich search on the powerful new Commit Graph. 

Whether searching for a specific commit, message, author, a changed file or files, or even a specific code change, the Commit Graph will highlight matching results across your entire repository. Use shortcut keys or the up/down arrows on the search bar  to navigate the search results; `F3` (also `Cmd+G` on macOS) goes to the next result from your selection while  `Shift+F3`  ( also `Shift+Cmd+G` on macOS) goes to the previous. Additionally you can quickly jump to the first or  last result, by holding `Shift` while clicking on the up/down arrows respectively – to make it easy to see when a file or change was introduced into the codebase.

<img src="/wp-content/uploads/Rich-Commit-Search.png" class="img-responsive center img-bordered">

Once you type search filtering criteria, use the arrow icons to move through each result.

<img src="/wp-content/uploads/Commit-Search-Moving-Arrow-Keys.gif" class="img-responsive center img-bordered">

### PR information in form of icon

Wait, which branch has that PR? 

If connected to one of the rich integrations with GitHub or GitLab, the Commit Graph will display a PR icon for any branch currently in PR. Right-click on the PR icon to open the PR on the GitHub or GitLab, or copy the URL.

<img src="/wp-content/uploads/PR-Icon.png" class="img-responsive center img-bordered">

### Hiding remotes, branches or tags

Need to focus and have too many remotes or just want to curate how much is shown in your Commit Graph? Now you can hide entire remotes, or specific branches and tags. Hover over any  branch or tag to access the “Hide” button  or right-click to hide the whole remote, or just the local or remote branch, to help focus your Commit Graph.

<img src="/wp-content/uploads/Branch-Hide.png" class="img-responsive center img-bordered">

### All new home view

It’s a homecoming! Our GitLens home view has a new look, with quick links to our Getting Started guides, Integrations, Trial info, and Feature spotlights. 

<img src="/wp-content/uploads/GitLens-Home.png" class="img-responsive center img-bordered">

### List or tree view in Commit Details View

The Commit Details View, which gives you contextual change info about your code, got a new toggle for List and Tree view.

<img src="/wp-content/uploads/view-as-list.png" class="img-responsive center img-bordered">

To open the Commit Details view, open the command palette using <kbd>Cmd+Shift+P</kbd> and type: Show Commit Details view or navigate to the Commit Details view in the Side Bar.

# Change Log

### Added

- ✨ All GitLens+ features on public and local repos are now available to everyone -- no account required!
  - We want to bring the power of GitLens+ features to more people without any gates.
- ✨ Commit Graph is out of preview!
  - Rich search features to find exactly what you're looking for:
    - Powerful filters to search by commit, message, author, a changed file or files, or even a specific code change
    - Searches look at ALL commits in a repository, not just what's shown in the graph
  - PR support for connected rich integrations (GitHub/GitLab)
  - Contextual right-click menus with popular actions for commits, branches, tags, and authors
  - Personalization of your graph experience
    - Show and hide branches and columns
    - Settings UI for easy fine-grain control over advanced settings
- Adds `View as Tree` option for changed files in the _Commit Details_ view
- Adds an `Open in Commit Graph` action to the hovers and commit quick pick menus

### Changed

- Updates the `Home View` with all new design and content
- Changes the `Show Commit` action in the hovers to `Show Details` and opens the _Commit Details_ view

### Fixed

- Fixes [#2203](https://github.com/gitkraken/vscode-gitlens/issues/2203) - Autolinks missing under commit details
- Fixes [#2230](https://github.com/gitkraken/vscode-gitlens/issues/2230) - j and k are inverted in ascending rebase order
- Fixes [#2195](https://github.com/gitkraken/vscode-gitlens/issues/2195) - Cannot open new files from commit details
- Fixes Commit Details view showing incorrect diffs for certain commits
- Fixes Commit Details view showing incorrect actions for uncommitted changes
- Fixes prioritization of multiple PRs associated with the same commit to choose a merged PR over others
- Fixes Graph not showing account banners when access is not allowed and trial banners were previously dismissed


***

<a id="v12-2"></a>
## Version 12.2

### Tuesday, August 30th, 2022

The new Commit Graph 🎨 in GitLens 12.2 will fix all your commitment problems...in your code 🥁 👩‍💻

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/EsnA4zIUvWY?controls=1&modestbranding=1" frameborder="0" allowfullscreen></iframe>
</div>

## ✨Commit Graph  - Preview 

Users may now view the Commit Graph of their repository through GitLens. 

This beloved feature from GitKraken Client helps visualize your repo commit history and give you information about branches, commits, and collaborators all in one view — making it easier to see contributions and help you make faster, more informed decisions.

<img src="/wp-content/uploads/1-commit-graph.png" class="img-responsive center img-bordered">

To open the Commit Graph, open the command palette using the keyboard shortcut <kbd>Cmd</kbd> <kbd>Shift</kbd> <kbd>P</kbd> and type `Show Commit Graph`.

<img src="/wp-content/uploads/2-commit-graph.gif" class="img-responsive center img-bordered">

This will open a new tab and render your current repo’s commit history, where you may scroll through your history and resize any of the columns widths. 

You may also access the Commit Graph by clicking this graph icon from the Source Control view in the Sidebar or Status Bar.

<img src="/wp-content/uploads/How-to-open-commit-graph-B.png" class="img-responsive center img-bordered">

The Commit Graph is available to all users working on public repositories, and requires no account. Additionally, users with a paid GitLens+ subscription can use the Commit Graph with private repos. 

For those on [vscode.dev](vscode.dev) or [github.dev](github.dev), this also means you can open the Commit Graph on a web browser. 

The Commit Graph is in `Preview` mode, and we’d love to hear your feedback in the [Commit Graph discussion on GitHub](https://github.com/gitkraken/vscode-gitlens/discussions/2158).



## Commit Details View

GitLens 12.2 also ships with a `Commit Details View`, which gives you contextual change info about your code.

<img src="/wp-content/uploads/3-commit-details-view.png" class="img-responsive center img-bordered">

To open the `Commit Details View`, open the command palette using <kbd>Cmd</kbd> <kbd>Shift</kbd> <kbd>P</kbd> and this time type: `Show Commit Details View` or navigate to the Commit Details View in the Sidebar.

<img src="/wp-content/uploads/4-commit-details-view.gif" class="img-responsive center img-bordered">

The `Commit Details View` updates as you move your cursor throughout the file with information about the commit that modified that line of code. Get quick information about the commit author, commit ID, links to Pull Requests, files modified in the commit, and more.

Click on a file to open the diff, and see what changed. You may also hover over the file name to access options like Open File, Open Changes with Working File, and Open Remote.


## ✨ GitHub Enterprise Integration

Next, GitLens+ now offers a richer integration with GitHub Enterprise.

Once authenticated, GitLens will enrich GitHub autolinks in the hovers. You’ll see your GitHub Enterprise avatar, links to related pull requests, along with a footnote of the pull request or issue details. 

<img src="/wp-content/uploads/6-GitHub-Enterprise.png" class="img-responsive center img-bordered">

You’ll see similar details from the Sidebar views for any commit or branch associated with a pull  request or issue.

## ✨ Single Sign On


Single Sign On is here, providing GitLens+ users with a more secure sign in method! 


### Requirements and configuration

Your GitKraken account may now initiate an Oauth authentication flow with the following supported Identity Providers (IdPs):

- Azure Active Directory
- Okta
- Google Identity Platform
- Ping Identity


<img src="/wp-content/uploads/SSO-setup.png" class="img-responsive center img-bordered">

Please note that your IdP will first need to be configured before setting up the connection in your GitKraken account. For assistance, please contact your IdP administrator or consult the IdP documentation for help. 

Additional requirements:
    - Configurable only by GitKraken Owner or Admin of an organization
    - Subscribed to either the Teams or Enterprise plan

→ [Documentation: How to set up SSO in GitKraken](https://help.gitkraken.com/gitkraken-client/single-sign-on/)

### Signing in with SSO

GitLens+ users should see a new option to Sign in with SSO from the login screen.

<img src="/wp-content/uploads/9-GitLens-SSO.png" class="img-responsive center img-bordered">

After clicking `Sign in with SSO`, the SSO form will open and ask for an email address to use for SSO login. The app will then check the email and determine whether the email address belongs to a single IdP for SSO. When the email address is successfully identified, the user will be taken to that IdP to login.

Once authenticated, the user may use GitLens+


## More improvements

### Stash naming defaults

When applying or popping a stash, GitLens will default the commit message input to the stash message. 

<img src="/wp-content/uploads/10-stash-commit-message.gif" class="img-responsive center img-bordered">

And when stashing changes, the stash name will now default to any entry in the commit message input.

### Stats in comparisons

There are now stats about additions & deletions in files nodes in comparisons. To get these stats, navigate to the `Search & Compare` view in the Sidebar and create a comparison between commits.

<img src="/wp-content/uploads/11-comparison-stats.png" class="img-responsive center img-bordered">

### Search for text in Interactive Rebase Editor

And users may now search for text on the `Interactive Rebase Editor` using <kbd>Ctrl</kbd> <kbd>F</kbd>.

<img src="/wp-content/uploads/12-interactive-rebase-text-search.png" class="img-responsive center img-bordered">


## Change Log


### Added

- Adds Commit Graph
- Adds Commit Details View
- Adds [**rich integration**](https://github.com/gitkraken/vscode-gitlens#remote-provider-integrations-) with GitHub Enterprise &mdash; closes [#1210](https://github.com/gitkraken/vscode-gitlens/issues/1210)
  - Adds associated pull request to line annotations and hovers
    ![Pull requests on line annotation and hovers](https://raw.githubusercontent.com/gitkraken/vscode-gitlens/main/images/docs/hovers-current-line-details.png)
  - Adds associated pull request to status bar blame
    ![Pull requests on status bar](https://raw.githubusercontent.com/gitkraken/vscode-gitlens/main/images/docs/status-bar.png)
  - Adds GitHub avatars
  - Adds associated pull requests to branches and commits in GitLens views
  - Adds rich autolinks for GitHub issues and merge requests, including titles, status, and authors
  - Adds rich support to _Autolinked Issues and Pull Requests_ within comparisons to list autolinked GitHub issues and merge requests in commit messages
- Adds new stash behaviors to use the Source Control (commit message) input box &mdash; closes [#2081](https://github.com/gitkraken/vscode-gitlens/issues/2081)
  - When a stash is applied or popped and the Source Control input is empty, we will now update the Source Control input to the stash message
  - When stashing changes and the Source Control input is not empty, we will now default the stash message input to the Source Control input value
- Adds the ability to search (<kbd>Ctrl</kbd>+<kbd>F</kbd>) for text on the Interactive Rebase Editor &mdash; closes [#2050](https://github.com/gitkraken/vscode-gitlens/issues/2050)
- Adds stats (additions & deletions) to files nodes in comparisons &mdash; closes [#2078](https://github.com/gitkraken/vscode-gitlens/issues/2078) thanks to help via [PR #2079](https://github.com/gitkraken/vscode-gitlens/pull/2079) by Nafiur Rahman Khadem ([@ShafinKhadem](https://github.com/ShafinKhadem))
- Adds the ability to uniquely format uncommitted changes for the current line blame annotations &mdash; closes [#1987](https://github.com/gitkraken/vscode-gitlens/issues/1987)
  - Adds a `gitlens.currentLine.uncommittedChangesFormat` setting to specify the uncommitted changes format of the current line blame annotation. **NOTE**: Setting this to an empty string will disable current line blame annotations for uncommitted changes
- Adds variable expansion support to the `gitlens.worktrees.defaultLocation` setting
  - `${userHome}` &mdash; the path of the user's home folder
  - `${workspaceFolder}` &mdash; the path of the folder opened in VS Code containing the specified repository
  - `${workspaceFolderBasename}` &mdash; the name of the folder opened in VS Code containing the specified repository without any slashes (/)
- Adds owner avatars to remotes in the _Remotes_ view for GitHub remotes

### Changed

- Greatly improves performance of many view interactions when connected to a rich integration and pull request details are enabled, including:
  - Showing and refreshing the _Commits_ view
  - Expanding commits, branches, and worktrees
- Remembers chosen filter on files nodes in comparisons when refreshing
- Changes display of filtered state of files nodes in comparisons
- Improves diff stat parsing performance and reduced memory usage
- Disallows comparisons with the working tree on the right-side (left-side still works as expected) and disables swapping
- Uses VS Code as `core.editor` in rebase &mdash; closes [#2084](https://github.com/gitkraken/vscode-gitlens/issues/2084) thanks to [PR #2085](https://github.com/gitkraken/vscode-gitlens/pull/2085) by Nafiur Rahman Khadem ([@ShafinKhadem](https://github.com/ShafinKhadem))

### Fixed

- Fixes [#2156](https://github.com/gitkraken/vscode-gitlens/issues/2156) - Reduce extension package size
- Fixes [#2136](https://github.com/gitkraken/vscode-gitlens/issues/2136) - Search & Compare quickpick shouldn't select the mode text when opening
- Fixes [#1896](https://github.com/gitkraken/vscode-gitlens/issues/1896) - Cannot read property 'fsPath' of undefined
- Fixes [#1550](https://github.com/gitkraken/vscode-gitlens/issues/1550) - Push button in commit widget does not trigger "Push force" when ALT is pressed.
- Fixes [#1991](https://github.com/gitkraken/vscode-gitlens/issues/1991) - Git lens status bar entry has an incomprehensible accessibility label
- Fixes [#2125](https://github.com/gitkraken/vscode-gitlens/issues/2125) - "git log" command in version 12.x is very slow
- Fixes [#2121](https://github.com/gitkraken/vscode-gitlens/issues/2121) - Typo in GitLens header &mdash; thanks to [PR #2122](https://github.com/gitkraken/vscode-gitlens/pull/2122) by Chase Knowlden ([@ChaseKnowlden](https://github.com/ChaseKnowlden))
- Fixes [#2082](https://github.com/gitkraken/vscode-gitlens/issues/2082) - GitLens Home view unreadable in certain themes
- Fixes [#2070](https://github.com/gitkraken/vscode-gitlens/issues/2070) - Quoted HTML / JSX syntax is not escaped correctly
- Fixes [#2069](https://github.com/gitkraken/vscode-gitlens/issues/2069) - Heatmap - incorrect behavior of gitlens.heatmap.fadeLines with gitlens.heatmap.ageThreshold
- Fixes an issue where choosing "Hide Current Branch Pull Request" from the _Commits_ view overflow menu wouldn't hide the PR node
- Fixes an issue where stashes without a message aren't displayed properly
- Fixes an issue where the _Stashes_ view empty state isn't displayed properly when there are no stashes
- Fixes typos via [PR #2086](https://github.com/gitkraken/vscode-gitlens/pull/2086) by stampyzfanz ([@stampyzfanz](https://github.com/stampyzfanz)), and [PR #2043](https://github.com/gitkraken/vscode-gitlens/pull/2043), [PR #2040](https://github.com/gitkraken/vscode-gitlens/pull/2040), [PR #2042](https://github.com/gitkraken/vscode-gitlens/pull/2042) by jogo- ([@jogo-](https://github.com/jogo-))
