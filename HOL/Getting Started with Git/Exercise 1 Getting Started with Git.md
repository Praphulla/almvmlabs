#Exercise 1: Getting Started with Git

In this exercise, you will learn how to create, clone, and push commits to a Git repository with Team Foundation Server.

##Task 1: Create a Git Repository

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

  <img src="./media/image3.png" width="423" height="344" />

    **Figure** Creating new team project

6.  Select the **Scrum** process template and click **Next**
    to continue.

  <img src="./media/image4.png" width="418" height="343" />
   
   **Figure** Creating new team project

7.  Select the option labeled “**Do not configure a SharePoint site at
    this time**” and then click **Next**.

  <img src="./media/image5.png" width="405" height="330" />
    
    **Figure** Creating a new team project

8.  Select the **Git** version control system and then click **Finish**.
  
  <img src="./media/image6.png" width="378" height="308" />
    
    **Figure** Creating new team project backed by a Git repository

9.  After the new Git team project has been created, click **Close** to
    return to Visual Studio.

##Task 2: Clone Git Repository

1.  Click the **Connect to Team Projects** button.

  <img src="./media/image7.png" width="345" height="45" />
   
   **Figure** Location of Connect button

1.  **Right-click** the **FabrikamCommunity** project node and then
    select the option to **Clone**.
    
     <img src="./media/image8.png" width="344" height="314" />
      
      **Figure** Cloning the repository

1.  Accept the default endpoint and repository location and then click
    **Clone**.

    <img src="./media/image9.png" width="271" height="125" />

    **Figure** Clone repository to local folder
 
##Task 3: Commit Code and Link to Work Item

1.  In **Team Explorer – Home**, click **Settings**.

   <img src="./media/image10.png" width="225" height="253" />

    **Figure** Project settings

1.  Click **Global Settings** under **Git**.

   <img src="./media/image11.png" width="251" height="299" />
 
    **Figure**  Git settings

1.  Enter an email address for Julia (**julia.ilyiana@vsalm**) and then
    click **Update**.

   <img src="./media/image12.png" width="246" height="328" />

    **Figure** Setting email address

1.  Click the **Home** button in **Team Explorer**.

   <img src="./media/image13.png" width="344" height="44" />

    **Figure** Navigating home

1.  Create a new work item for the product backlog by selecting **Team |
    New Work Item | Product Backlog Item** from the main menu.

2.  Enter a title of “**Create new web site**” and then click **Save
    Work Item**. Take note of the **ID** once the work item is saved.

   <img src="./media/image14.png" width="242" height="143" />

    **Figure** Creating new Product Backlog Item

1.  In **Team Explorer – Home**, click **New…** underneath the
    **Solutions** section.
 
   <img src="./media/image15.png" width="296" height="337" />
    
    **Figure** Creating a new solution

1.  In the **New Project** window, select the **Visual C\# | Web |
    ASP.NET Web Application** template. Ensure the **Application
    Insights** option is unchecked and then click **OK**.

  <img src="./media/image16.png" width="547" height="303" />

   **Figure** Creating new web site

1.  Select the **MVC** template, **de-select** the option to “**Host in
    the cloud**”, and then click **OK**.

  <img src="./media/image17.png" width="450" height="347" />

   **Figure** Creating a new web site

1.  In **Team Explorer – Home**, click **Changes**.

  <img src="./media/image18.png" width="232" height="156" />

  **Figure** Viewing changes

1.  Scroll down the list of included changes to the end and note that
    .gitattributes and .gitignore files were automatically added to
    the project. The **.gitattributes** file contains various settings
    to control Git behavior whereas the **.gitignore** file specifies
    patterns and extensions to ignore when detecting changes.

  <img src="./media/image19.png" width="318" height="146" />

  **Figure** ncluded changes

1.  Enter a commit message of “**initial MVC site for work item
    \#247**”. If the Product Backlog Item that you saved has a different
    ID, use that number instead. Typing ‘**\#**’ followed by the work
    item ID will automatically link the commit to the work item when
    pushed to the server.

   <img src="./media/image20.png" width="351" height="116" />
  
    **Figure** Entering a commit message

1.  Commit the changes by clicking **Commit All**. Note that the commit
    is persisted locally and is not shared with the server.

   <img src="./media/image21.png" width="280" height="93" />
   
    **Figure** Committing changes locally

1.  Let’s make a small change to the web site. In **Solution Explorer**,
    open **\_Layout.cshtml** from the **Views\\Shared** folder.

   <img src="./media/image22.png" width="280" height="324" />

    **Figure** Opening \_Layout.cshtml

1.  Modify the title as shown in the following screenshot (from “**My
    ASP.NET Application**” to “**Community**”).

  <img src="./media/image23.png" width="536" height="124" />

   **Figure** Modifying markup

1.  In **Team Explorer – Changes**, enter a commit message and then
    click **Commit All**. **Save** changes to files when prompted.

  <img src="./media/image24.png" width="300" height="156" />
   
   **Figure** Entering a commit message
 

##Task 4: Synchronize Commits with Server

1.  Navigate to the commits view by clicking **Sync**.

  <img src="./media/image25.png" width="343" height="119" />

  **Figure** Navigating to commits view

1.  The **Team Explorer – Synchronization** view shows both incoming and
    outgoing commits. Here we can see the two local commits that are
    ready to be pushed to the server.

  <img src="./media/image26.png" width="272" height="264" />

  **Figure** Outgoing commits

1.  Click **Sync** to perform both a **pull** and a **push** to ensure
    we have the latest source before pushing our updates.

  <img src="./media/image27.png" width="285" height="103" />

   **Figure** Synchronizing with the server

 <img src="./media/image28.png" width="272" height="98" />
   
   **Figure** Synchronizing with the server

1.  Finally, let’s take a quick peek at what these commits look like in
    the web portal. In **Team Explorer – Home**, click **Web Portal**.

  <img src="./media/image29.png" width="261" height="161" />

  **Figure** Launching web portal

1.  Select the **Code** tab in the web portal.

  <img src="./media/image30.png" width="471" height="66" />

   **Figure** Navigating to Code

1.  Select the **History** child tab to see the two commits. Note that
    the relative size of the commits (in terms of number of
    modified files) can be determined by viewing the size of the circles
    rendered to the left of the commits.

   <img src="./media/image31.png" width="306" height="225" />

    **Figure** Commits view

  >**Note:** It may take a few moments after pushing a commit before
    the commit size indicators show up. You can refresh the page
    if necessary.
    
1.  Click the link associated with the first commit.

  <img src="./media/image32.png" width="464" height="94" />

   **Figure** Selecting the first commit

1.  Note that the “**Create new web site**” work item is linked to
    the commit. Click the link to open the work item.

  >**Note:** It may take a few minutes before the work item gets linked
    to the commit. In the event that the link has not been made yet, go
   ahead and continue on with the rest of the lab.

  <img src="./media/image33.png" width="273" height="249" />

  **Figure** Viewing linked work item

  <img src="./media/image34.png" width="277" height="113" />

  **Figure** Viewing linked work item
  
