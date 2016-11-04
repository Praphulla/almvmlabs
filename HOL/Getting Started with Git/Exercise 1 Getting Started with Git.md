

### <span id="_Toc430533662" class="anchor"><span id="_Toc430533856" class="anchor"></span></span>Exercises

1.  This hands-on lab includes the following exercises:

<!-- -->

1.  Getting Started with Git

2.  Git Branching and Merging

3.  

<!-- -->

1.  Estimated time to complete this lab: **60 minutes**.

<!-- -->

1.  

<span id="_Toc428376557" class="anchor"></span>

**  
**

<span id="_Toc430533663" class="anchor"><span id="_Toc430533857" class="anchor"></span></span>**Exercise 1: Getting Started with Git**
--------------------------------------------------------------------------------------------------------------------------------------

1.  In this exercise, you will learn how to create, clone, and push
    commits to a Git repository with Team Foundation Server.

#### <span id="_Toc428376558" class="anchor"><span id="_Toc430533664" class="anchor"><span id="_Toc430533858" class="anchor"></span></span></span>Task 1: Create a Git Repository

1.  Log in as **Julia Ilyiana** (VSALM\\Julia). All user passwords are
    **P2ssw0rd**.

2.  Launch **Visual Studio 2015** from the taskbar and open **Team
    Explorer**. You should now be connected to the FabrikamFiber
    team project. If you are not automatically connected to the
    FabrikamFiber project, click the **Connect to Team Projects** button
    (<img src="./media/image2.png" width="18" height="22" />) to do so.

3.  There are a few reasons why Fabrikam Fiber might want to use Git as
    their source control option within Team Foundation Server. One
    reason could be that they are collaborating with developers using a
    tool such as Xcode, which supports the Git protocol natively.
    Another reason could be that they have developers working offline
    (such as during a commute) who want to commit code locally when they
    are offline and check this code into Team Foundation Server when
    they get into the office. Microsoft now offers teams the ability to
    utilize Git without sacrificing the integrated application lifecycle
    management capabilities offered by Team Foundation Server. Visual
    Studio 2015 also provides developers with a great experience for
    working with any Git repository – whether it’s hosted by Team
    Foundation Server, a local repository, or another Git provider.

4.  Select **File | New | Team Project** from the main menu.

5.  Name the new project “**FabrikamCommunity**” and click **Next**.

<!-- -->

1.  <img src="./media/image3.png" width="423" height="344" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating new team project

<!-- -->

1.  

<!-- -->

1.  Select the **Scrum** process template and click **Next**
    to continue.

<!-- -->

1.  <img src="./media/image4.png" width="418" height="343" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating new team project

<!-- -->

1.  

<!-- -->

1.  Select the option labeled “**Do not configure a SharePoint site at
    this time**” and then click **Next**.

<!-- -->

1.  <img src="./media/image5.png" width="405" height="330" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating a new team project

<!-- -->

1.  

<!-- -->

1.  Select the **Git** version control system and then click **Finish**.

<!-- -->

1.  <img src="./media/image6.png" width="378" height="308" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating new team project backed by a Git repository

<!-- -->

1.  

<!-- -->

1.  After the new Git team project has been created, click **Close** to
    return to Visual Studio.

2.  

#### <span id="_Toc428376559" class="anchor"><span id="_Toc430533665" class="anchor"><span id="_Toc430533859" class="anchor"></span></span></span>Task 2: Clone Git Repository

1.  Click the **Connect to Team Projects** button.

<!-- -->

1.  <img src="./media/image7.png" width="345" height="45" />

<!-- -->

1.  Figure

<!-- -->

1.  Location of Connect button

<!-- -->

1.  

<!-- -->

1.  **Right-click** the **FabrikamCommunity** project node and then
    select the option to **Clone**.

<!-- -->

1.  <img src="./media/image8.png" width="344" height="314" />

<!-- -->

1.  Figure

<!-- -->

1.  Cloning the repository

<!-- -->

1.  

<!-- -->

1.  Accept the default endpoint and repository location and then click
    **Clone**.

<!-- -->

1.  <img src="./media/image9.png" width="271" height="125" />

<!-- -->

1.  Figure

<!-- -->

1.  Clone repository to local folder

<!-- -->

1.  

<!-- -->

1.  

#### <span id="_Toc428376560" class="anchor"><span id="_Toc430533666" class="anchor"><span id="_Toc430533860" class="anchor"></span></span></span>Task 3: Commit Code and Link to Work Item

1.  In **Team Explorer – Home**, click **Settings**.

<!-- -->

1.  <img src="./media/image10.png" width="225" height="253" />

<!-- -->

1.  Figure

<!-- -->

1.  Project settings

<!-- -->

1.  

<!-- -->

1.  Click **Global Settings** under **Git**.

<!-- -->

1.  <img src="./media/image11.png" width="251" height="299" />

<!-- -->

1.  Figure

<!-- -->

1.  Git settings

<!-- -->

1.  

<!-- -->

1.  Enter an email address for Julia (**julia.ilyiana@vsalm**) and then
    click **Update**.

<!-- -->

1.  <img src="./media/image12.png" width="246" height="328" />

<!-- -->

1.  Figure

<!-- -->

1.  Setting email address

<!-- -->

1.  

<!-- -->

1.  Click the **Home** button in **Team Explorer**.

<!-- -->

1.  <img src="./media/image13.png" width="344" height="44" />

<!-- -->

1.  Figure

<!-- -->

1.  Navigating home

<!-- -->

1.  Create a new work item for the product backlog by selecting **Team |
    New Work Item | Product Backlog Item** from the main menu.

2.  Enter a title of “**Create new web site**” and then click **Save
    Work Item**. Take note of the **ID** once the work item is saved.

<!-- -->

1.  <img src="./media/image14.png" width="242" height="143" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating new Product Backlog Item

<!-- -->

1.  

<!-- -->

1.  In **Team Explorer – Home**, click **New…** underneath the
    **Solutions** section.

<!-- -->

1.  <img src="./media/image15.png" width="296" height="337" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating a new solution

<!-- -->

1.  

<!-- -->

1.  In the **New Project** window, select the **Visual C\# | Web |
    ASP.NET Web Application** template. Ensure the **Application
    Insights** option is unchecked and then click **OK**.

<!-- -->

1.  <img src="./media/image16.png" width="547" height="303" />

<!-- -->

1.  Figure

    Creating new web site

<!-- -->

1.  Select the **MVC** template, **de-select** the option to “**Host in
    the cloud**”, and then click **OK**.

<!-- -->

1.  <img src="./media/image17.png" width="450" height="347" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating a new web site

<!-- -->

1.  

<!-- -->

1.  In **Team Explorer – Home**, click **Changes**.

<!-- -->

1.  <img src="./media/image18.png" width="232" height="156" />

<!-- -->

1.  Figure

<!-- -->

1.  Viewing changes

<!-- -->

1.  

<!-- -->

1.  Scroll down the list of included changes to the end and note that
    .gitattributes and .gitignore files were automatically added to
    the project. The **.gitattributes** file contains various settings
    to control Git behavior whereas the **.gitignore** file specifies
    patterns and extensions to ignore when detecting changes.

<!-- -->

1.  <img src="./media/image19.png" width="318" height="146" />

<!-- -->

1.  Figure

<!-- -->

1.  Included changes

<!-- -->

1.  

<!-- -->

1.  Enter a commit message of “**initial MVC site for work item
    \#247**”. If the Product Backlog Item that you saved has a different
    ID, use that number instead. Typing ‘**\#**’ followed by the work
    item ID will automatically link the commit to the work item when
    pushed to the server.

<!-- -->

1.  <img src="./media/image20.png" width="351" height="116" />

<!-- -->

1.  Figure

<!-- -->

1.  Entering a commit message

<!-- -->

1.  

<!-- -->

1.  Commit the changes by clicking **Commit All**. Note that the commit
    is persisted locally and is not shared with the server.

<!-- -->

1.  <img src="./media/image21.png" width="280" height="93" />

<!-- -->

1.  Figure

<!-- -->

1.  Committing changes locally

<!-- -->

1.  

<!-- -->

1.  Let’s make a small change to the web site. In **Solution Explorer**,
    open **\_Layout.cshtml** from the **Views\\Shared** folder.

<!-- -->

1.  <img src="./media/image22.png" width="280" height="324" />

<!-- -->

1.  Figure

<!-- -->

1.  Opening \_Layout.cshtml

<!-- -->

1.  

<!-- -->

1.  Modify the title as shown in the following screenshot (from “**My
    ASP.NET Application**” to “**Community**”).

<!-- -->

1.  <img src="./media/image23.png" width="536" height="124" />

<!-- -->

1.  Figure

<!-- -->

1.  Modifying markup

<!-- -->

1.  

<!-- -->

1.  In **Team Explorer – Changes**, enter a commit message and then
    click **Commit All**. **Save** changes to files when prompted.

<!-- -->

1.  <img src="./media/image24.png" width="300" height="156" />

<!-- -->

1.  Figure

<!-- -->

1.  Entering a commit message

<!-- -->

1.  

<!-- -->

1.  

#### <span id="_Toc428376561" class="anchor"><span id="_Toc430533861" class="anchor"></span></span>Task 4: Synchronize Commits with Server

1.  Navigate to the commits view by clicking **Sync**.

<!-- -->

1.  <img src="./media/image25.png" width="343" height="119" />

<!-- -->

1.  Figure

<!-- -->

1.  Navigating to commits view

<!-- -->

1.  

<!-- -->

1.  The **Team Explorer – Synchronization** view shows both incoming and
    outgoing commits. Here we can see the two local commits that are
    ready to be pushed to the server.

<!-- -->

1.  <img src="./media/image26.png" width="272" height="264" />

<!-- -->

1.  Figure

<!-- -->

1.  Outgoing commits

<!-- -->

1.  

<!-- -->

1.  Click **Sync** to perform both a **pull** and a **push** to ensure
    we have the latest source before pushing our updates.

<!-- -->

1.  <img src="./media/image27.png" width="285" height="103" />

<!-- -->

1.  Figure

<!-- -->

1.  Synchronizing with the server

<!-- -->

1.  

<!-- -->

1.  <img src="./media/image28.png" width="272" height="98" />

<!-- -->

1.  Figure

<!-- -->

1.  Synchronizing with the server

<!-- -->

1.  

<!-- -->

1.  Finally, let’s take a quick peek at what these commits look like in
    the web portal. In **Team Explorer – Home**, click **Web Portal**.

<!-- -->

1.  <img src="./media/image29.png" width="261" height="161" />

<!-- -->

1.  Figure

<!-- -->

1.  Launching web portal

<!-- -->

1.  

<!-- -->

1.  Select the **Code** tab in the web portal.

<!-- -->

1.  <img src="./media/image30.png" width="471" height="66" />

<!-- -->

1.  Figure

<!-- -->

1.  Navigating to Code

<!-- -->

1.  

<!-- -->

1.  Select the **History** child tab to see the two commits. Note that
    the relative size of the commits (in terms of number of
    modified files) can be determined by viewing the size of the circles
    rendered to the left of the commits.

<!-- -->

1.  <img src="./media/image31.png" width="306" height="225" />

<!-- -->

1.  Figure

<!-- -->

1.  Commits view

<!-- -->

1.  

<!-- -->

1.  **Note:** It may take a few moments after pushing a commit before
    the commit size indicators show up. You can refresh the page
    if necessary.

<!-- -->

1.  Click the link associated with the first commit.

<!-- -->

1.  <img src="./media/image32.png" width="464" height="94" />

<!-- -->

1.  Figure

<!-- -->

1.  Selecting the first commit

<!-- -->

1.  

<!-- -->

1.  Note that the “**Create new web site**” work item is linked to
    the commit. Click the link to open the work item.

<!-- -->

1.  **Note:** It may take a few minutes before the work item gets linked
    to the commit. In the event that the link has not been made yet, go
    ahead and continue on with the rest of the lab.

<!-- -->

1.  <img src="./media/image33.png" width="273" height="249" />

<!-- -->

1.  Figure

<!-- -->

1.  Viewing linked work item

<!-- -->

1.  

<!-- -->

1.  <img src="./media/image34.png" width="277" height="113" />

<!-- -->

1.  Figure

<!-- -->

1.  Viewing linked work item

<!-- -->

1.  

<!-- -->

1.  

<span id="_Toc428376562" class="anchor"><span id="_Toc430533667" class="anchor"><span id="_Toc430533862" class="anchor"></span></span></span>Exercise 2: Git Branching and Merging
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

1.  In this exercise, you will learn about Git branching and merging
    support in Visual Studio. In general, branching is often used to
    help switch development contexts and to isolate risk. Git branching
    is no different in that regard. Creating a Git branch is a
    lightweight (and therefore fast) operation, as you are simply
    creating a new reference to an existing commit. This is very
    different from Team Foundation Version Control (TFVC) branching
    where the entire source tree needs to be duplicated server-side. We
    will also take a quick look at the merging support for Git projects.

#### <span id="_Toc428376563" class="anchor"><span id="_Toc430533668" class="anchor"><span id="_Toc430533863" class="anchor"></span></span></span>Task 1: Branching

1.  Return to Visual Studio and open **Team Explorer – Home**.

2.  Click **Branches**.

<!-- -->

1.  <img src="./media/image35.png" width="345" height="196" />

<!-- -->

1.  Figure

<!-- -->

1.  Branches tile

<!-- -->

1.  

<!-- -->

1.  Let’s say that we would like to create a new branch to do some
    development work on the web site. Right-click the **master** branch
    node and then select **New Local Branch From**.

<!-- -->

1.  <img src="./media/image36.png" width="344" height="259" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating new local branch

<!-- -->

1.  

<!-- -->

1.  Provide a name of **Development**, select the **master** branch,
    select the **Checkout Branch** option, and then click **Create
    Branch**.

<!-- -->

1.  <img src="./media/image37.png" width="347" height="214" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating new branch

<!-- -->

1.  

<!-- -->

1.  **Note:** It is also possible to create a new branch from backlog
    items or the Kanban board view of TFS.

    <img src="./media/image38.png" width="235" height="177" />
    <img src="./media/image39.png" width="249" height="177" />

<!-- -->

1.  

<!-- -->

1.  Note that you are now connected to the new local branch, and that it
    has not been published to the server yet.

<!-- -->

1.  <img src="./media/image40.png" width="348" height="218" />

<!-- -->

1.  Figure

<!-- -->

1.  New local branch

<!-- -->

1.  

<!-- -->

1.  In **Solution Explorer**, open the **HomeController.cs** file from
    the **Controllers** folder.

2.  Modify the **About** method as shown in the following screenshot.

<!-- -->

1.  <img src="./media/image41.png" width="422" height="122" />

<!-- -->

1.  Figure

<!-- -->

1.  Modifying source code from new branch

<!-- -->

1.  

<!-- -->

1.  Right-click somewhere in the whitespace of the editor and select
    **Source Control | Commit**.

    <img src="./media/image42.png" width="564" height="248" />

2.  In **Team Explorer - Changes**, enter a commit message of “**dev
    version**” and click **Commit All**. Save the changes when prompted.

<!-- -->

1.  <img src="./media/image43.png" width="349" height="208" />

<!-- -->

1.  Figure

<!-- -->

1.  Commit changes

<!-- -->

1.  

<!-- -->

1.  At this point, the changes have been committed locally. In the
    **Team Explorer – Changes** window, click the **Development** branch
    link to quickly navigate to the **Team Explorer - Branches** view.

<!-- -->

1.  <img src="./media/image44.png" width="346" height="146" />

<!-- -->

1.  Figure

<!-- -->

1.  Switching between branches

<!-- -->

1.  

<!-- -->

1.  Double-click the **Master** branch and note that original version of
    the *HomeController.cs* file is shown in the code editor window.

<!-- -->

1.  <img src="./media/image45.png" width="255" height="164" />

<!-- -->

1.  Figure

<!-- -->

1.  Switching active branch

<!-- -->

1.  <img src="./media/image46.png" width="409" height="113" />

<!-- -->

1.  Figure

    Switching between branches

<!-- -->

1.  You don’t have to publish the branch to the server yet if you want
    to continue working locally. As you saw in the previous exercise,
    you can continue to work locally and add additional commits to the
    new branch. In **Team Explorer – Branches**, **right-click** the
    **Development** branch and select **View History**.

<!-- -->

1.  <img src="./media/image47.png" width="265" height="261" />

<!-- -->

1.  Figure

<!-- -->

1.  Viewing history for local branch

<!-- -->

1.  

<!-- -->

1.  <img src="./media/image48.png" width="624" height="111" />

<!-- -->

1.  Figure

<!-- -->

1.  Source history for selected branch

<!-- -->

1.  

<!-- -->

1.  When you are ready, you can delete the branch, merge it back into
    your master branch, or push it to the server-side repository so that
    teammates can access it. Let’s go ahead and publish the branch by
    **right-clicking** the Development branch and selecting the
    **Publish Branch** option.

<!-- -->

1.  <img src="./media/image49.png" width="345" height="343" />

<!-- -->

1.  Figure

<!-- -->

1.  Publishing branch

<!-- -->

1.  

<!-- -->

1.  <img src="./media/image50.png" width="277" height="206" />

<!-- -->

1.  Figure

<!-- -->

1.  Successful publication

<!-- -->

1.  

<!-- -->

1.  Now let’s say that another team member makes a modification to the
    **HomeController.cs** file and commits that change to the master
    branch, before Julia has a chance to merge in her
    development changes.

2.  Open a **Remote Desktop** session to **VSALM**. Connect using user
    **Adam Barr** (VSALM\\Adam). All user passwords are **P2ssw0rd**.

3.  Launch **Visual Studio** from the taskbar.

4.  Connect to the **FabrikamCommunity** team project (using the
    **Manage Connections** button as before, and this time select
    **Manage Connections | Connect to Team Project**).

5.  Select the **FabrikamCommunity** team project and then click
    **Connect**.

<!-- -->

1.  <img src="./media/image51.png" width="420" height="300" />

<!-- -->

1.  Figure

<!-- -->

1.  Connect to team project

<!-- -->

1.  

<!-- -->

1.  **Double-click** the **FabrikamCommunity** project shown in Team
    Explorer - Connect. Note that the Git project has a special icon.

<!-- -->

1.  <img src="./media/image52.png" width="257" height="181" />

<!-- -->

1.  Figure

<!-- -->

1.  Connect to team project

<!-- -->

1.  

<!-- -->

1.  **Clone** the repository using default options as you did in the
    first exercise.

2.  Open the **Global Settings** from Team Explorer – Settings as you
    did in the first exercise and add an email address for Adam. The
    email address that you use does not matter for the purposes of
    this demonstration.

<!-- -->

1.  <img src="./media/image53.png" width="242" height="227" />

<!-- -->

1.  Figure

<!-- -->

1.  Setting up Git email

<!-- -->

1.  

<!-- -->

1.  **Double-click** the **MvcApplication1.sln** solution shown in
    **Team Explorer – Home**.

<!-- -->

1.  <img src="./media/image54.png" width="219" height="248" />

<!-- -->

1.  Figure

<!-- -->

1.  Open solution

<!-- -->

1.  

<!-- -->

1.  Modify the same ***HomeController.cs*** file that Julia did, but
    this time change the text to be something different.

<!-- -->

1.  <img src="./media/image55.png" width="400" height="123" />

<!-- -->

1.  Figure

<!-- -->

1.  Modifying web page title

<!-- -->

1.  

<!-- -->

1.  In **Team Explorer – Changes**, enter a commit message of “**Adam’s
    version**” and then click **Commit All**. Save changes
    when prompted. Note that Adam has committed changes to the
    master branch.

<!-- -->

1.  <img src="./media/image56.png" width="328" height="196" />

<!-- -->

1.  Figure

<!-- -->

1.  Commit changes

<!-- -->

1.  

<!-- -->

1.  Click **Sync** from the commit response.

<!-- -->

1.  <img src="./media/image57.png" width="342" height="126" />

<!-- -->

1.  Figure

<!-- -->

1.  Sync changes with server

<!-- -->

1.  

<!-- -->

1.  Click **Sync** to execute the actual sync.

<!-- -->

1.  <img src="./media/image58.png" width="344" height="287" />

<!-- -->

1.  Figure

<!-- -->

1.  Sync button

<!-- -->

1.  

<!-- -->

1.  Switch users back to **Julia** by minimizing the remote
    desktop session.

2.  

#### <span id="_Toc428376564" class="anchor"><span id="_Toc430533669" class="anchor"><span id="_Toc430533864" class="anchor"></span></span></span>Task 2: Merging

1.  From Julia’s perspective, she has so far created a local branch
    based off the master, made a change to a file, and then published
    that branch. Julia would like to go ahead and merge her Development
    branch back into the master branch.

2.  In **Team Explorer – Branches**, select the **Merge** dropdown.

<!-- -->

1.  <img src="./media/image59.png" width="345" height="214" />

<!-- -->

1.  Figure

<!-- -->

1.  Merging Git branches

<!-- -->

1.  

<!-- -->

1.  Select **Development** as the source and **Master** as the target.
    Click **Merge** to start the process.

<!-- -->

1.  <img src="./media/image60.png" width="346" height="360" />

<!-- -->

1.  Figure

<!-- -->

1.  Merging Git branches

<!-- -->

1.  

<!-- -->

1.  Note that the **Master** repository is currently selected and that
    ***HomeController.cs*** shows the development version of the text.
    The merge was performed locally by updating the Master branch to
    point to the latest commit of the Development branch.

<!-- -->

1.  <img src="./media/image61.png" width="570" height="119" />

<!-- -->

1.  Figure

<!-- -->

1.  Merge completed locally

<!-- -->

1.  

<!-- -->

1.  **Right-click** the **Master** branch in **Team Explorer –
    Branches** and select the **View History…** option.

    <img src="./media/image62.png" width="297" height="295" />

2.  The history view should look identical to the one you saw earlier,
    except this time both the Development and Master branch designators
    (in red) point to the same commit.

<!-- -->

1.  <img src="./media/image63.png" width="572" height="67" />

<!-- -->

1.  Figure

<!-- -->

1.  Merge completed locally

<!-- -->

1.  

<!-- -->

1.  Still unaware of Adam’s change that he pushed to the Main branch
    earlier, Julia will now attempt to push her commit. Navigate to the
    **Team Explorer - Synchronization** view and then click **Sync** to
    attempt a pull and a push with the server.

<!-- -->

1.  <img src="./media/image64.png" width="267" height="223" />

<!-- -->

1.  Figure

<!-- -->

1.  Sync with server repository

<!-- -->

1.  **Note:** If you see a popup notifying that an open file has been
    changed externally, click **Yes** as this is expected.

<!-- -->

1.  Visual Studio reports that we can’t push our commit yet due to
    a conflict.

<!-- -->

1.  <img src="./media/image65.png" width="258" height="352" />

<!-- -->

1.  Figure

<!-- -->

1.  Conflict between two different commits

<!-- -->

1.  

<!-- -->

1.  Click **Resolve the Conflicts**.

<!-- -->

1.  <img src="./media/image66.png" width="345" height="134" />

<!-- -->

1.  Figure

<!-- -->

1.  Resolving conflicts

<!-- -->

1.  

<!-- -->

1.  In the **Team Explorer – Resolve Conflicts** view, select the
    ***HomeController.cs*** file listed under the Conflicts section and
    then click **Merge**.

<!-- -->

1.  <img src="./media/image67.png" width="349" height="308" />

<!-- -->

1.  Figure

<!-- -->

1.  Starting manual merge process

<!-- -->

1.  

<!-- -->

1.  The Merge window used for Git conflict resolution is very similar to
    the one used with Team Foundation Version Control. We will go ahead
    and assume that Julia’s change is correct, so check the box shown in
    the top-right pane.

<!-- -->

1.  <img src="./media/image68.png" width="566" height="308" />

<!-- -->

1.  Figure

<!-- -->

1.  Merge window

<!-- -->

1.  

<!-- -->

1.  Click **Accept Merge**.

<!-- -->

1.  <img src="./media/image69.png" width="567" height="99" />

<!-- -->

1.  Figure

<!-- -->

1.  Merge window

<!-- -->

1.  

<!-- -->

1.  Click **Commit Merge**.

<!-- -->

1.  <img src="./media/image70.png" width="376" height="163" />

<!-- -->

1.  Figure

<!-- -->

1.  Commit the resolved merge

<!-- -->

1.  

<!-- -->

1.  In the Team Explorer – Changes view, note that conflicts have been
    resolved but the merge still needs to be committed. Enter a message
    and then click **Commit All**. Save changes when prompted.

<!-- -->

1.  <img src="./media/image71.png" width="289" height="187" />

<!-- -->

1.  Figure

<!-- -->

1.  Commit the resolved merge

<!-- -->

1.  

<!-- -->

1.  Click **Sync**.

<!-- -->

1.  <img src="./media/image72.png" width="331" height="107" />

<!-- -->

1.  Figure

<!-- -->

1.  Unsynced Commits

<!-- -->

1.  

<!-- -->

1.  Click **Sync** to finish the merge process.

<!-- -->

1.  <img src="./media/image73.png" width="277" height="238" />

<!-- -->

1.  Figure

<!-- -->

1.  Syncing with server

<!-- -->

1.  

<!-- -->

1.  Click **Web Portal** from **Team Explorer – Home**.

<!-- -->

1.  <img src="./media/image74.png" width="234" height="167" />

<!-- -->

1.  Figure

<!-- -->

1.  Opening the Fabrikam Fiber web portal

<!-- -->

1.  

<!-- -->

1.  Select the **Code** tab.

<!-- -->

1.  <img src="./media/image75.png" width="403" height="59" />

<!-- -->

1.  Figure

<!-- -->

1.  Navigating to Code view

<!-- -->

1.  

<!-- -->

1.  Select the **History** tab to view all commits pushed to
    the repository.

<!-- -->

1.  <img src="./media/image76.png" width="356" height="314" />

<!-- -->

1.  Figure

<!-- -->

1.  Commits view

<!-- -->

1.  

<!-- -->

1.  Select the **Branches** tab to view all branches published to
    the repository.

<!-- -->

1.  <img src="./media/image77.png" width="565" height="143" />

<!-- -->

1.  Figure

<!-- -->

1.  Branches view

<!-- -->

1.  

<!-- -->

1.  

#### <span id="_Toc428376565" class="anchor"><span id="_Toc430533670" class="anchor"><span id="_Toc430533865" class="anchor"></span></span></span>Task 3: Managing Security and Permissions

1.  Now let’s take a quick peek at managing security and permissions for
    Git repositories hosted in Team Foundation Server. Select the
    **FabrikamCommunity** dropdown and then **Manage Repositories**.

<!-- -->

1.  <img src="./media/image78.png" width="273" height="163" />

<!-- -->

1.  Figure

<!-- -->

1.  Managing repositories

<!-- -->

1.  

<!-- -->

1.  The first thing to note is that you can create additional Git
    repositories within the same team project.

<!-- -->

1.  <img src="./media/image79.png" width="400" height="222" />

<!-- -->

1.  Figure

<!-- -->

1.  Option to create additional Git repositories

<!-- -->

1.  

<!-- -->

1.  Select the **FabrikamCommunity** repository node.

<!-- -->

1.  <img src="./media/image80.png" width="193" height="116" />

<!-- -->

1.  Figure

<!-- -->

1.  Navigating to repository node

<!-- -->

1.  

<!-- -->

1.  You can manage repository level security here for your users and
    security groups.

<!-- -->

1.  <img src="./media/image81.png" width="566" height="280" />

<!-- -->

1.  Figure

<!-- -->

1.  Managing repository security

<!-- -->

1.  

<!-- -->

1.  Select the **Master** branch node. Security level settings that
    affect only the currently selected branch can be made here,
    providing fine-grained control for your repository if needed.

<!-- -->

1.  <img src="./media/image82.png" width="510" height="267" />

<!-- -->

1.  Figure

<!-- -->

1.  Managing branch security

<!-- -->

1.  

<!-- -->

1.  

#### <span id="_Toc428376566" class="anchor"><span id="_Toc430533671" class="anchor"><span id="_Toc430533866" class="anchor"></span></span></span>Task 4: Branch Policies

1.  When you want people on your team to review code in a Git team
    project, you can use a pull request to review and merge the code.
    Pull requests enable developers working in topic branches to get
    feedback on their changes from other developers prior to submitting
    the code into the master branch. Any developer participating in the
    review can see the code changes, leave comments in the code, and
    give a "thumbs up" approval if they're satisfied with those changes.

<!-- -->

1.  Navigate to the administrative section for the FabrikamCommunity
    project in the portal and then select the **master** branch. You
    should already be there if continuing on from the previous task.

<!-- -->

1.  <img src="./media/image83.png" width="438" height="206" />

<!-- -->

1.  Figure

<!-- -->

1.  Master branch

<!-- -->

1.  

<!-- -->

1.  Although it is possible to utilize pull requests without any further
    configuration, let’s take a quick look at how to setup
    branch policies. Select the **Branch Policies** tab.

<!-- -->

1.  <img src="./media/image84.png" width="454" height="113" />

<!-- -->

1.  Figure

<!-- -->

1.  Branch policies tab

<!-- -->

1.  

<!-- -->

1.  You can make use of branch policies that effectively put in a gate
    that helps prevent inadvertent or low quality commits by
    automatically initiating a build, or by requiring code reviews by
    certain individuals. Select the option to **Require…reviewers per
    pull request** and set the minimum number of reviewers to “1”.

<!-- -->

1.  <img src="./media/image85.png" width="574" height="390" />

<!-- -->

1.  Figure

<!-- -->

1.  Require code reviews

<!-- -->

1.  

<!-- -->

1.  **Note:** It is also possible to configure branch policy such that a
    build is triggered whenever updates are made to the master branch.
    You can even have the merge fail when the build fails. This is
    useful for teams looking to adopt continuous integration.

<!-- -->

1.  It is also possible to require specific reviewers for specific
    portions of your code base. For example, let’s say that Julia needs
    to sign off on all changes made to the ASP.NET MVC controllers.
    Click **Add a new path**.

<!-- -->

1.  <img src="./media/image86.png" width="411" height="177" />

<!-- -->

1.  Figure

<!-- -->

1.  Add required reviewers based on code path

<!-- -->

1.  

<!-- -->

1.  Leave the default options of **Enabled** and **Required** selected,
    set the **Path** to be everything in the **Controllers** folder, and
    then click **Add User**.

<!-- -->

1.  <img src="./media/image87.png" width="624" height="61" />

<!-- -->

1.  Figure

<!-- -->

1.  Add required reviewers based on code path

<!-- -->

1.  

<!-- -->

1.  Select **Julia Ilyiana** from the Add Required Reviewers window and
    then click **Save Changes**.

<!-- -->

1.  <img src="./media/image88.png" width="561" height="253" />

<!-- -->

1.  Figure

<!-- -->

1.  Add required reviewer

<!-- -->

1.  

<!-- -->

1.  Click **Save Changes** to update the master branch policies. Close
    the administration browser tab.

<!-- -->

1.  <img src="./media/image89.png" width="624" height="106" />

<!-- -->

1.  Figure

<!-- -->

1.  Updating branch policies

<!-- -->

1.  

<!-- -->

1.  

#### <span id="_Toc428376567" class="anchor"><span id="_Toc430533672" class="anchor"><span id="_Toc430533867" class="anchor"></span></span></span>Task 5: Code Review and Merge using Pull Requests

1.  Switch users back to **Adam** and ensure that you are connected to
    the FabrikamCommunity project still.

2.  In the **Team Explorer - Branches** view, double-click **master** to
    change to that branch.

3.  In the **Team Explorer - Synchronization** view, note that there are
    two incoming commits listed (if there are not, try a
    **Fetch** operation).

4.  Click **Sync** to ensure that the local copy of master matches
    what’s on the server. If you have **HomeController.cs** open in the
    editor, you may be prompted to reload it.

<!-- -->

1.  <img src="./media/image90.png" width="344" height="257" />

<!-- -->

1.  Figure

<!-- -->

1.  Synchronize with server

<!-- -->

1.  

<!-- -->

1.  Now let’s say that Adam is working on the project and needs to
    update some of the controller code. To do this, he will first create
    a topic branch based on master. In **Team Explorer - Branches**,
    right-click the **master** branch and select **New Local Branch
    From**…

<!-- -->

1.  <img src="./media/image91.png" width="344" height="372" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating local topic branch

<!-- -->

1.  

<!-- -->

1.  For the branch name, use something like
    “**users/adam/controllerupdate**”. Use the default option to
    “**Checkout branch**”. Click **Create Branch**.

<!-- -->

1.  <img src="./media/image92.png" width="343" height="211" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating local topic branch

<!-- -->

1.  

<!-- -->

1.  Update the **About** method from **HomeController.cs** with a new
    message, something like “**Adam’s enhanced description page.**”

<!-- -->

1.  <img src="./media/image93.png" width="451" height="125" />

<!-- -->

1.  Figure

<!-- -->

1.  Code update

<!-- -->

1.  

<!-- -->

1.  In **Team Explorer - Changes**, provide a commit message and then
    **Commit All**. Save the changes when prompted.

<!-- -->

1.  <img src="./media/image94.png" width="327" height="198" />

<!-- -->

1.  Figure

<!-- -->

1.  Commit change

<!-- -->

1.  

<!-- -->

1.  In **Team Explorer - Branches**, right-click the topic branch and
    select **Publish Branch**.

<!-- -->

1.  <img src="./media/image95.png" width="343" height="383" />

<!-- -->

1.  Figure

<!-- -->

1.  Publish topic branch

<!-- -->

1.  

<!-- -->

1.  After successfully publishing the branch, click **Create a pull
    request**.

<!-- -->

1.  <img src="./media/image96.png" width="346" height="295" />

<!-- -->

1.  Figure

<!-- -->

1.  Initiating a pull request

<!-- -->

1.  

<!-- -->

1.  Check **Open in browser after creating pull request** and click
    **Create** to create a pull request with the default options.

    <img src="./media/image97.png" width="326" height="325" />

2.  After the pull request is created, note that the pull request view
    shows what merge is proposed, Adam’s description is provided, and
    there are tabs listing affected files and commits. It also indicates
    that there are no merge conflicts detected, and that due to branch
    policy, Julia must approve the changes in order to proceed

<!-- -->

1.  <img src="./media/image98.png" width="563" height="242" />

<!-- -->

1.  Figure

<!-- -->

1.  Pull request view

<!-- -->

1.  

<!-- -->

1.  To demonstrate the branch policy in action, let’s say Adam attempts
    to complete the pull request by himself. Click **Complete Pull
    Request**.

<!-- -->

1.  <img src="./media/image99.png" width="203" height="396" />

<!-- -->

1.  Figure

<!-- -->

1.  Attempt to complete pull request

<!-- -->

1.  

<!-- -->

1.  When asked to confirm the merge, notice the warning about the merge
    going against policy. Click **Complete merge** to try anyway.

<!-- -->

1.  <img src="./media/image100.png" width="377" height="273" />

<!-- -->

1.  Figure

<!-- -->

1.  Attempt to complete pull request

<!-- -->

1.  

<!-- -->

1.  Note that Adam is notified that the request first needs to be
    approved by all required reviewers first.

<!-- -->

1.  <img src="./media/image101.png" width="615" height="143" />

<!-- -->

1.  Figure

<!-- -->

1.  Attempt to complete pull request

<!-- -->

1.  

<!-- -->

1.  At this point in the workflow, Julia needs to be notified of this
    pull request through some communication channel, whether that is in
    person, through Skype, through team room notification, or via TFS
    pull request alert. For the purposes of this short exercise,
    however, we will just skip to Julia checking pull requests for
    this project.

2.  Switch users back to **Julia**.

3.  In the web portal, navigate to the **FabrikamCommunity** project and
    the **Code | Pull Requests** view.

<!-- -->

1.  <img src="./media/image102.png" width="469" height="103" />

<!-- -->

1.  Figure

<!-- -->

1.  Pull requests view

<!-- -->

1.  

<!-- -->

1.  Select the link provided on the pull request from Adam.

<!-- -->

1.  <img src="./media/image103.png" width="556" height="89" />

<!-- -->

1.  Figure

<!-- -->

1.  Viewing pull request

<!-- -->

1.  

<!-- -->

1.  At this point, Julia can review all of the files and commits
    associated with the pull request and make a decision. It is also
    possible for Julia to have a conversation with Adam (and perhaps
    other reviewers) in order to help make the decision, or perhaps even
    request additional work be performed before the pull request will
    be approved.

2.  Let’s assume that Julia is ready to approve the request as-is, so
    select the response drop down underneath Julia’s name in the
    Reviewers section and select the **Approved** option.

<!-- -->

1.  <img src="./media/image104.png" width="251" height="361" />

<!-- -->

1.  Figure

<!-- -->

1.  Approving pull request

<!-- -->

1.  

<!-- -->

1.  Note that the **Active** section now shows that there are no merge
    conflicts and that required reviewers have indicated approval. Click
    **Complete Pull Request** to complete the pull request and merge
    changes from Adam’s topic branch into master.

<!-- -->

1.  <img src="./media/image105.png" width="191" height="176" />

<!-- -->

1.  Figure

<!-- -->

1.  Completing pull request

<!-- -->

1.  

<!-- -->

1.  Now when the pull request confirmation is shown, you can click
    **Complete merge** with success. Note that you have the option to
    delete the source branch as part of the process.

    <img src="./media/image106.png" width="442" height="284" />

2.  Switch users back to **Adam**.

3.  Refresh the pull request view and note that it has been updated as
    expected with the actions made by Julia.

<!-- -->

1.  <img src="./media/image107.png" width="568" height="184" />

<!-- -->

1.  Figure

<!-- -->

1.  Completed pull request

<!-- -->

1.  2.  

<!-- -->

1.  
