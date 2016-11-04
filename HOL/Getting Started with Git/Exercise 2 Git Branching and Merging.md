#Exercise 2: Git Branching and Merging

  In this exercise, you will learn about Git branching and merging
    support in Visual Studio. In general, branching is often used to
    help switch development contexts and to isolate risk. Git branching
    is no different in that regard. Creating a Git branch is a
    lightweight (and therefore fast) operation, as you are simply
    creating a new reference to an existing commit. This is very
    different from Team Foundation Version Control (TFVC) branching
    where the entire source tree needs to be duplicated server-side. We
    will also take a quick look at the merging support for Git projects.

##Task 1: Branching

1.  Return to Visual Studio and open **Team Explorer – Home**.

2.  Click **Branches**.
   
   <img src="./media/image35.png" width="345" height="196" />

    **Figure** Branches tile

1.  Let’s say that we would like to create a new branch to do some
    development work on the web site. Right-click the **master** branch
    node and then select **New Local Branch From**.

   <img src="./media/image36.png" width="344" height="259" />

    **Figure** Creating new local branch

1.  Provide a name of **Development**, select the **master** branch,
    select the **Checkout Branch** option, and then click **Create
    Branch**.
    
   <img src="./media/image37.png" width="347" height="214" />
  
    **Figure** Creating new branch

  >**Note:** It is also possible to create a new branch from backlog
    items or the Kanban board view of TFS.

    <img src="./media/image38.png" width="235" height="177" />
    <img src="./media/image39.png" width="249" height="177" />

1.  Note that you are now connected to the new local branch, and that it
    has not been published to the server yet.

    <img src="./media/image40.png" width="348" height="218" />

     **Figure** New local branch

1.  In **Solution Explorer**, open the **HomeController.cs** file from
    the **Controllers** folder.

2.  Modify the **About** method as shown in the following screenshot.
  
    <img src="./media/image41.png" width="422" height="122" />

     **Figure** Modifying source code from new branch

1.  Right-click somewhere in the whitespace of the editor and select
    **Source Control | Commit**.

    <img src="./media/image42.png" width="564" height="248" />

2.  In **Team Explorer - Changes**, enter a commit message of “**dev
    version**” and click **Commit All**. Save the changes when prompted.

    <img src="./media/image43.png" width="349" height="208" />

     **Figure** Commit changes

1.  At this point, the changes have been committed locally. In the
    **Team Explorer – Changes** window, click the **Development** branch
    link to quickly navigate to the **Team Explorer - Branches** view.

   <img src="./media/image44.png" width="346" height="146" />

   **Figure** Switching between branches

1.  Double-click the **Master** branch and note that original version of
    the *HomeController.cs* file is shown in the code editor window.

   <img src="./media/image45.png" width="255" height="164" />
   
    **Figure**   Switching active branch

   <img src="./media/image46.png" width="409" height="113" />
    
    **Figure** Switching between branches

1.  You don’t have to publish the branch to the server yet if you want
    to continue working locally. As you saw in the previous exercise,
    you can continue to work locally and add additional commits to the
    new branch. In **Team Explorer – Branches**, **right-click** the
    **Development** branch and select **View History**.

   <img src="./media/image47.png" width="265" height="261" />
    
    **Figure** Viewing history for local branch

   <img src="./media/image48.png" width="624" height="111" />

    **Figure** Source history for selected branch

1.  When you are ready, you can delete the branch, merge it back into
    your master branch, or push it to the server-side repository so that
    teammates can access it. Let’s go ahead and publish the branch by
    **right-clicking** the Development branch and selecting the
    **Publish Branch** option.
  
    <img src="./media/image49.png" width="345" height="343" />

    **Figure** Publishing branch

    <img src="./media/image50.png" width="277" height="206" />

    **Figure** Successful publication

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
 
   <img src="./media/image51.png" width="420" height="300" />

    **Figure** Connect to team project

1.  **Double-click** the **FabrikamCommunity** project shown in Team
    Explorer - Connect. Note that the Git project has a special icon.

    <img src="./media/image52.png" width="257" height="181" />
    
    **Figure** Connect to team project

1.  **Clone** the repository using default options as you did in the
    first exercise.

2.  Open the **Global Settings** from Team Explorer – Settings as you
    did in the first exercise and add an email address for Adam. The
    email address that you use does not matter for the purposes of
    this demonstration.

    <img src="./media/image53.png" width="242" height="227" />

     **Figure** Setting up Git email

1.  **Double-click** the **MvcApplication1.sln** solution shown in
    **Team Explorer – Home**.

    <img src="./media/image54.png" width="219" height="248" />

       **Figure** Open solution

1.  Modify the same ***HomeController.cs*** file that Julia did, but
    this time change the text to be something different.

    <img src="./media/image55.png" width="400" height="123" />

     **Figure** Modifying web page title

1.  In **Team Explorer – Changes**, enter a commit message of “**Adam’s
    version**” and then click **Commit All**. Save changes
    when prompted. Note that Adam has committed changes to the
    master branch.

   <img src="./media/image56.png" width="328" height="196" />
    
    **Figure** Commit changes


1.  Click **Sync** from the commit response.

  <img src="./media/image57.png" width="342" height="126" />

    **Figure** Sync changes with server

1.  Click **Sync** to execute the actual sync.

  <img src="./media/image58.png" width="344" height="287" />
    
    **Figure** Sync button

1.  Switch users back to **Julia** by minimizing the remote
    desktop session.

##Task 2: Merging

1.  From Julia’s perspective, she has so far created a local branch
    based off the master, made a change to a file, and then published
    that branch. Julia would like to go ahead and merge her Development
    branch back into the master branch.

2.  In **Team Explorer – Branches**, select the **Merge** dropdown.

 <img src="./media/image59.png" width="345" height="214" />



   **Figure** Merging Git branches 

1.  Select **Development** as the source and **Master** as the target.
    Click **Merge** to start the process. 
	
	<img src="./media/image60.png" width="346" height="360" />

     **Figure** Merging Git branches 


1.  Note that the **Master** repository is currently selected and that
    ***HomeController.cs*** shows the development version of the text.
    The merge was performed locally by updating the Master branch to
    point to the latest commit of the Development branch. 
	
	<img src="./media/image61.png" width="570" height="119" />

     **Figure** Merge completed locally 

1.  **Right-click** the **Master** branch in **Team Explorer –
    Branches** and select the **View History…** option.

    <img src="./media/image62.png" width="297" height="295" />

2.  The history view should look identical to the one you saw earlier,
    except this time both the Development and Master branch designators
    (in red) point to the same commit.

    <img src="./media/image63.png" width="572" height="67" />

     **Figure** Merge completed locally 

1.  Still unaware of Adam’s change that he pushed to the Main branch
    earlier, Julia will now attempt to push her commit. Navigate to the
    **Team Explorer - Synchronization** view and then click **Sync** to
    attempt a pull and a push with the server. 
	
	<img src="./media/image64.png" width="267" height="223" />

     **Figure** Sync with server repository 

    >**Note:** If you see a popup notifying that an open file has been
    changed externally, click **Yes** as this is expected.

1.  Visual Studio reports that we can’t push our commit yet due to
    a conflict. 
	
	<img src="./media/image65.png" width="258" height="352" />

     **Figure** Conflict between two different commits 

1.  Click **Resolve the Conflicts**. 

    <img src="./media/image66.png" width="345" height="134" />

     **Figure** Resolving conflicts 
	 
1.  In the **Team Explorer – Resolve Conflicts** view, select the
    ***HomeController.cs*** file listed under the Conflicts section and
    then click **Merge**. 
	 
	 <img src="./media/image67.png" width="349" height="308" />

     **Figure** Starting manual merge process 

1.  The Merge window used for Git conflict resolution is very similar to
    the one used with Team Foundation Version Control. We will go ahead
    and assume that Julia’s change is correct, so check the box shown in
    the top-right pane. 
	
	<img src="./media/image68.png" width="566" height="308" />

     **Figure** Merge window 

1.  Click **Accept Merge**. 

	 <img src="./media/image69.png" width="567" height="99" />

     **Figure** Merge window 

1.  Click **Commit Merge**.


1.  <img src="./media/image70.png" width="376" height="163" />

     **Figure** Commit the resolved merge 

1.  In the Team Explorer – Changes view, note that conflicts have been
    resolved but the merge still needs to be committed. Enter a message
    and then click **Commit All**. Save changes when prompted. 
	
	<img src="./media/image71.png" width="289" height="187" />

     **Figure** Commit the resolved merge 

1.  Click **Sync**. 

    <img src="./media/image72.png" width="331" height="107" />

     **Figure** Unsynced Commits  

1.  Click **Sync** to finish the merge process. 

	<img src="./media/image73.png" width="277" height="238" />

     **Figure** Syncing with server 

1.  Click **Web Portal** from **Team Explorer – Home**. 

	<img src="./media/image74.png" width="234" height="167" />

     **Figure** Opening the Fabrikam Fiber web portal 


1.  Select the **Code** tab. 

    <img src="./media/image75.png" width="403" height="59" />

     **Figure** Navigating to Code view 

1.  Select the **History** tab to view all commits pushed to
    the repository.

    <img src="./media/image76.png" width="356" height="314" />

     **Figure** Commits view 

1.  Select the **Branches** tab to view all branches published to
    the repository. 
	
	<img src="./media/image77.png" width="565" height="143" />

     **Figure** Branches view  

##Task 3: Managing Security and Permissions

1.  Now let’s take a quick peek at managing security and permissions for
    Git repositories hosted in Team Foundation Server. Select the
    **FabrikamCommunity** dropdown and then **Manage Repositories**.

	<img src="./media/image78.png" width="273" height="163" />

     **Figure**  Managing repositories 

1.  The first thing to note is that you can create additional Git
    repositories within the same team project.

	<img src="./media/image79.png" width="400" height="222" /> 

     **Figure**  Option to create additional Git repositories  

1.  Select the **FabrikamCommunity** repository node.

    <img src="./media/image80.png" width="193" height="116" />

     **Figure**  Navigating to repository node

1.  You can manage repository level security here for your users and
    security groups.

    <img src="./media/image81.png" width="566" height="280" />

     **Figure**  Managing repository security  

1.  Select the **Master** branch node. Security level settings that
    affect only the currently selected branch can be made here,
    providing fine-grained control for your repository if needed.

	<img src="./media/image82.png" width="510" height="267" />

     **Figure**  Managing branch security    

##Task 4: Branch Policies

1.  When you want people on your team to review code in a Git team
    project, you can use a pull request to review and merge the code.
    Pull requests enable developers working in topic branches to get
    feedback on their changes from other developers prior to submitting
    the code into the master branch. Any developer participating in the
    review can see the code changes, leave comments in the code, and
    give a "thumbs up" approval if they're satisfied with those changes.

1.  Navigate to the administrative section for the FabrikamCommunity
    project in the portal and then select the **master** branch. You
    should already be there if continuing on from the previous task.

    <img src="./media/image83.png" width="438" height="206" />

     **Figure**  Master branch  

1.  Although it is possible to utilize pull requests without any further
    configuration, let’s take a quick look at how to setup
    branch policies. Select the **Branch Policies** tab. 

	<img src="./media/image84.png" width="454" height="113" />

     **Figure**  Branch policies tab   

1.  You can make use of branch policies that effectively put in a gate
    that helps prevent inadvertent or low quality commits by
    automatically initiating a build, or by requiring code reviews by
    certain individuals. Select the option to **Require…reviewers per
    pull request** and set the minimum number of reviewers to “1”. 
	 
	 <img src="./media/image85.png" width="574" height="390" />

     **Figure**  Require code reviews  

  >**Note:** It is also possible to configure branch policy such that a
    build is triggered whenever updates are made to the master branch.
    You can even have the merge fail when the build fails. This is
    useful for teams looking to adopt continuous integration.

1.  It is also possible to require specific reviewers for specific
    portions of your code base. For example, let’s say that Julia needs
    to sign off on all changes made to the ASP.NET MVC controllers.
    Click **Add a new path**.  
	
	<img src="./media/image86.png" width="411" height="177" />

     **Figure**  Add required reviewers based on code path  

1.  Leave the default options of **Enabled** and **Required** selected,
    set the **Path** to be everything in the **Controllers** folder, and
    then click **Add User**.  
	 
	 <img src="./media/image87.png" width="624" height="61" />

     **Figure**  Add required reviewers based on code path  

1.  Select **Julia Ilyiana** from the Add Required Reviewers window and
    then click **Save Changes**.

	<img src="./media/image88.png" width="561" height="253" />

     **Figure**  Add required reviewer  

1.  Click **Save Changes** to update the master branch policies. Close
    the administration browser tab.

	<img src="./media/image89.png" width="624" height="106" />

     **Figure**  Updating branch policies    

##Task 5: Code Review and Merge using Pull Requests

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
	
	<img src="./media/image90.png" width="344" height="257" />

     **Figure**  Synchronize with server  

1.  Now let’s say that Adam is working on the project and needs to
    update some of the controller code. To do this, he will first create
    a topic branch based on master. In **Team Explorer - Branches**,
    right-click the **master** branch and select **New Local Branch
    From**…  
	
	<img src="./media/image91.png" width="344" height="372" />

     **Figure**  Creating local topic branch 

1.  For the branch name, use something like
    “**users/adam/controllerupdate**”. Use the default option to
    “**Checkout branch**”. Click **Create Branch**.

    <img src="./media/image92.png" width="343" height="211" />

     **Figure**  Creating local topic branch 

1.  Update the **About** method from **HomeController.cs** with a new
    message, something like “**Adam’s enhanced description page.**”

	<img src="./media/image93.png" width="451" height="125" />

     **Figure**  Code update  

1.  In **Team Explorer - Changes**, provide a commit message and then
    **Commit All**. Save the changes when prompted.

	<img src="./media/image94.png" width="327" height="198" />

     **Figure**  Commit change  

1.  In **Team Explorer - Branches**, right-click the topic branch and
    select **Publish Branch**.

	<img src="./media/image95.png" width="343" height="383" />

     **Figure**  Publish topic branch  

1.  After successfully publishing the branch, click **Create a pull
    request**.

    <img src="./media/image96.png" width="346" height="295" />

     **Figure**  Initiating a pull request 

1.  Check **Open in browser after creating pull request** and click
    **Create** to create a pull request with the default options.

    <img src="./media/image97.png" width="326" height="325" />

2.  After the pull request is created, note that the pull request view
    shows what merge is proposed, Adam’s description is provided, and
    there are tabs listing affected files and commits. It also indicates
    that there are no merge conflicts detected, and that due to branch
    policy, Julia must approve the changes in order to proceed

    <img src="./media/image98.png" width="563" height="242" />

     **Figure**  Pull request view  

1.  To demonstrate the branch policy in action, let’s say Adam attempts
    to complete the pull request by himself. Click **Complete Pull
    Request**.

	<img src="./media/image99.png" width="203" height="396" />

     **Figure**  Attempt to complete pull request  

1.  When asked to confirm the merge, notice the warning about the merge
    going against policy. Click **Complete merge** to try anyway.

 	<img src="./media/image100.png" width="377" height="273" />

     **Figure**  Attempt to complete pull request  

1.  Note that Adam is notified that the request first needs to be
    approved by all required reviewers first.

    <img src="./media/image101.png" width="615" height="143" />

     **Figure**  Attempt to complete pull request  

1.  At this point in the workflow, Julia needs to be notified of this
    pull request through some communication channel, whether that is in
    person, through Skype, through team room notification, or via TFS
    pull request alert. For the purposes of this short exercise,
    however, we will just skip to Julia checking pull requests for
    this project.

2.  Switch users back to **Julia**.

3.  In the web portal, navigate to the **FabrikamCommunity** project and
    the **Code | Pull Requests** view.

    <img src="./media/image102.png" width="469" height="103" />

     **Figure**  Pull requests view  

1.  Select the link provided on the pull request from Adam.

    <img src="./media/image103.png" width="556" height="89" />

     **Figure**  Viewing pull request  

1.  At this point, Julia can review all of the files and commits
    associated with the pull request and make a decision. It is also
    possible for Julia to have a conversation with Adam (and perhaps
    other reviewers) in order to help make the decision, or perhaps even
    request additional work be performed before the pull request will
    be approved.

2.  Let’s assume that Julia is ready to approve the request as-is, so
    select the response drop down underneath Julia’s name in the
    Reviewers section and select the **Approved** option. 

	<img src="./media/image104.png" width="251" height="361" />

     **Figure** Approving pull request  

1.  Note that the **Active** section now shows that there are no merge
    conflicts and that required reviewers have indicated approval. Click
    **Complete Pull Request** to complete the pull request and merge
    changes from Adam’s topic branch into master.

	<img src="./media/image105.png" width="191" height="176" />

     **Figure** Completing pull request

1.  Now when the pull request confirmation is shown, you can click
    **Complete merge** with success. Note that you have the option to
    delete the source branch as part of the process.

    <img src="./media/image106.png" width="442" height="284" />

2.  Switch users back to **Adam**.

3.  Refresh the pull request view and note that it has been updated as
    expected with the actions made by Julia.

	<img src="./media/image107.png" width="568" height="184" />

     **Figure** Completed pull request   
