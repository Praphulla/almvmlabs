Hands-On Lab

Embracing Continuous Delivery with Release Management for Visual Studio 2015
============================================================================

Lab version: 14.0.25123.0

Last updated: 5/19/2016

1.  

<!-- -->

1.  ![](media/image1.png){width="4.267175196850394in"
    height="0.7166666666666667in"}

<!-- -->

1.  <span id="_Toc429731976" class="anchor"></span>**TABLE OF CONTENT**

[Embracing Continuous Delivery with Release Management for Visual Studio
2015
1](#embracing-continuous-delivery-with-release-management-for-visual-studio-2015)

[Overview 3](#overview)

[Prerequisites 3](#prerequisites)

[About the Fabrikam Fiber Scenario
3](#about-the-fabrikam-fiber-scenario)

[Exercise 1: Continuous Release Management
3](#exercise-1-continuous-release-management)

[Task 1: Configuring a continuous build
3](#task-1-configuring-a-continuous-build)

[Task 2: Creating a continuous release
7](#task-2-creating-a-continuous-release)

[Exercise 2: Gated Releases 15](#exercise-2-gated-releases)

[Task 1: Adding a QA environment 15](#task-1-adding-a-qa-environment)

[Exercise 3: Releasing To Azure (optional)
20](#exercise-3-releasing-to-azure-optional)

[Task 1: Creating an Azure Web site and database
21](#task-1-creating-an-azure-web-site-and-database)

[Task 2: Configuring the build to produce a Web Deploy package
30](#task-2-configuring-the-build-to-produce-a-web-deploy-package)

[Task 3: Creating a release environment for Azure
31](#task-3-creating-a-release-environment-for-azure)

[Task 4: Checking in a change to kick off the release workflow
39](#task-4-checking-in-a-change-to-kick-off-the-release-workflow)

**Overview**
------------

1.  In this lab, you will learn about the release management features
    available in Visual Studio 2015 and its suite of release and
    deployment tools that automate the deployment of applications across
    the desktop, server, and the cloud. The release management features
    of Visual Studio 2015 help development and operations teams
    integrate with Team Foundation Server to configure and automate
    complex deployments of their automated builds to target environments
    more easily. Development teams can also model their release
    processes and track approvals, sign-offs, and visualize their
    release status.

### Prerequisites

1.  In order to complete this lab you will need the Visual Studio 2015
    virtual machine provided by Microsoft. For more information on
    acquiring and using this virtual machine, please see [this blog
    post](http://aka.ms/ALMVM).

### About the Fabrikam Fiber Scenario

1.  This set of hands-on-labs uses a fictional company, Fabrikam Fiber,
    as a backdrop to the scenarios you are learning about. Fabrikam
    Fiber provides cable television and related services to the
    United States. They are growing rapidly and have embraced Windows
    Azure to scale their customer-facing web site directly to end-users
    to allow them to self-service tickets and track technicians. They
    also use an on-premises ASP.NET MVC application for their customer
    service representatives to administer customer orders.

    In this set of hands-on labs, you will take part in a number of
    scenarios that involve the development and testing team at
    Fabrikam Fiber. The team, which consists of 8-10 people, has decided
    to use Visual Studio application lifecycle management tools to
    manage their source code, run their builds, test their web sites,
    and plan and track the project.

<!-- -->

1.  

<!-- -->

1.  Estimated time to complete this lab: **60 minutes**.

<!-- -->

1.  

**Exercise 1: Continuous Release Management**
---------------------------------------------

1.  In this exercise, you will use the release management features of
    Team Foundation Server to produce an automated deployment solution.
    This exercise will take an existing enterprise application and
    automate its deployment to the development team’s testing
    environment after each source check-in.

#### Task 1: Configuring a continuous build

1.  Log in as **Brian Keller** (VSALM\\Brian). All user passwords are
    **P2ssw0rd**.

2.  Open **Internet Explorer**.

3.  Navigate to the **TFS FF Portal** using the bookmark at the top of
    the browser.

    ![](media/image2.png){width="2.622642169728784in"
    height="0.7079111986001749in"}

4.  Click the **Code** tab.

    ![](media/image3.png){width="2.0660378390201224in"
    height="0.7250623359580053in"}

5.  You can easily edit files on the server and check them in from the
    > browser, which is great for scenarios where you only need to make
    > minor tweaks. You’ll come back to this tab in future steps, so
    > leave it open as you move forward.

6.  Right-click the **Build** tab and select **Open in new tab** to
    view builds. You’re going to move back and forth between parts of
    TFS, so keeping these separate tabs open will make things easier as
    you go along. After the tab opens, go to it.

    ![](media/image4.png){width="2.0094346019247595in"
    height="0.8727843394575678in"}

7.  Click the **Create new build definition** button from the left
    > navigation panel.

    ![](media/image5.png){width="1.169811898512686in"
    height="0.7988965441819773in"}

8.  Select the **Visual Studio** template and click **Next**.

    ![](media/image6.png){width="3.9245286526684167in"
    height="3.9245286526684167in"}

9.  The default settings are fine here, so just check the box to enable
    > **continuous integration** and click **Create**.

    ![](media/image7.png){width="3.9433967629046367in"
    height="3.9433967629046367in"}

10. Select the **Repository** tab and update the **Mappings** so that
    > both use the **“\$/FabrikamFiber/Dev”** branch.

    ![](media/image8.png){width="3.905660542432196in"
    height="2.339560367454068in"}

11. Return to the **Build** tab and select the **Visual Studio
    > Build** step. Set the **MSBuild Arguments** to the text below.

    **/p:OutDir=\$(build.stagingDirectory)**

    ![](media/image9.png){width="5.613207567804024in"
    height="1.9196445756780403in"}

12. Remove the **Visual Studio Test** and **Index Sources & Publish
    > Symbols** steps from the process.

    ![](media/image10.png){width="2.7924518810148733in"
    height="2.509433508311461in"}

13. Click **Save**.

    ![](media/image11.png){width="2.405660542432196in"
    height="1.4974004811898514in"}

14. Set the **Name** to **“Fabrikam Development CI”** and click **OK**.

    ![](media/image12.png){width="4.037736220472441in"
    height="1.69666447944007in"}

15. Return to the browser tab opened to the **Code** hub.

16. Navigate to the path below to open a shared layout file used to
    > present a consistent look and feel for the site.

    \$/FabrikamFiber/Dev/FabrikamFiber.CallCenter/FabrikamFiber.Web/Views/Shared/\_Layout.cshtml

    ![](media/image13.png){width="5.641509186351706in"
    height="1.0788779527559056in"}

17. Click **Edit** to enable editing directly in the browser.

    ![](media/image14.png){width="0.8315277777777778in"
    height="1.0283016185476817in"}

18. Locate the “Support” text within a **H2** tag. Change it to “Support
    v2.0” and click the **Save** icon to check in the change. This
    check-in will invoke a build now that continuous integration builds
    have been enabled.

    ![](media/image15.png){width="5.792452974628172in"
    height="1.1071259842519685in"}

19. Switch back to the browser tab with the builds.

20. Select the **Queued** tab to view builds that have not
    yet completed. The CI (continuous integration) build definition
    created earlier should have picked up the code change and kicked off
    a new build.

    ![](media/image16.png){width="3.6226410761154857in"
    height="1.1383245844269467in"}

21. You don’t need to wait for the build to complete to move on to the
    next step.

#### Task 2: Creating a continuous release

1.  Now that there is an automatic build that occurs when changes are
    checked in, it’s time to set up a continuous release so that this
    new build can make its way out to stakeholders. Right-click the
    **Release** tab and select **Open in new tab**. You should now have
    three tabs open: Code, Build, and Release.

    ![](media/image17.png){width="2.2169805336832895in"
    height="0.5238757655293088in"}

2.  To create your first release, click the **here** link as
    shown below.

    ![](media/image18.png){width="4.849056211723535in"
    height="1.125229658792651in"}

3.  Start with an empty definition and click **OK**.

    ![](media/image19.png){width="3.9905653980752405in"
    height="1.4165299650043746in"}

4.  Enter “Fabrikam Release” as the release name and press **Enter**.

    ![](media/image20.png){width="3.820754593175853in"
    height="1.3812871828521436in"}

5.  The next step is to link this release with a build definition. Click
    **Link to a build definition** to select one.

    ![](media/image21.png){width="4.103772965879265in"
    height="0.4568066491688539in"}

6.  The CI build definition created earlier should be the default
    option, but select it if it’s not. Click **Link** to confirm.

    ![](media/image22.png){width="4.103472222222222in"
    height="2.1759700349956255in"}

7.  The purpose of this release process is to pick up a completed build
    and deploy it to a target environment. In order to automate that,
    select the **Triggers** tab and select the **Continuous Deployment**
    option with **Fabrikam Development CI**. Note that this setting
    merely indicates when the release process is begun and doesn’t
    actually indicate when or how any actual work is done. That will be
    up to each environment.

    ![](media/image23.png){width="5.547169728783902in"
    height="3.2548140857392824in"}

8.  Click the **Environments** tab. By default, there is one
    environment, which you will rename “Dev”. This will represent the
    “Dev” environment used by the dev team during development.

    ![](media/image24.png){width="4.575471347331583in"
    height="2.4408180227471568in"}

9.  The first thing you need to do with this environment is to indicate
    the conditions under which it will be deployed to. Click the
    ellipses button in the environment box and select **Deployment
    conditions**.

    ![](media/image25.png){width="2.820754593175853in"
    height="2.0137674978127733in"}

10. Under **Trigger**, select **After release creation** to indicate
    that you want this deployment process to begin after the release has
    been created (which will be the result of the target build
    completing, as configured earlier). Click **OK** to confirm.

    ![](media/image26.png){width="5.330188101487314in"
    height="3.3313681102362205in"}

11. Now that the basic settings of the environment have been defined,
    it’s time to configure exactly how a release is deployed. This is
    done through a series of **Tasks** that involve any process you need
    to get the job done. The “Dev” environment is pretty straightforward
    since it just involves copying files from the build directory to a
    directory configured to be used by IIS (which happens to be on the
    same machine in this lab scenario). Click **Add tasks** to select
    which tasks this deployment process will use.

    ![](media/image27.png){width="2.811321084864392in"
    height="1.1080457130358705in"}

12. Under the **Utility** tab, click **Add** from **Copy Files** to add
    one of those tasks to the workflow. Note that you could add a
    variety of tasks to the process, so the dialog doesn’t close after
    you hit **Add**. Instead, just click it once and then click
    **Close** to return to the main view.

    ![](media/image28.png){width="5.160377296587926in"
    height="4.752398293963255in"}

13. There are three key settings for the **Copy Files** task. First, set
    **Source Folder** to the path below.

    \$(System.DefaultWorkingDirectory)/Fabrikam Development
    CI/drop/\_PublishedWebSites/FabrikamFiber.Web

14. Next, set **Target Folder** to the path below.

    c:\\FabrikamRM\\WebSite\\DEV

15. Finally, expand **Advanced** and check **Over Write** to indicate
    that it’s okay to overwrite existing files at the destination.

    ![](media/image29.png){width="3.8867924321959757in"
    height="1.9780304024496937in"}

16. Now that this process has been configured, click **Save**.

    ![](media/image30.png){width="4.773584864391951in"
    height="2.3422167541557304in"}

17. Open a new browser tab and navigate to the Fabrikam Fiber Dev site.
    Note that the “Support” text is still just “Support” because the
    most recent changes were checked in and built, but not deployed.

    ![](media/image31.png){width="4.339622703412074in"
    height="1.7117399387576553in"}

18. Switch to the browser tab open to the builds page (probably the
    second one).

19. Click **Queue build**. Note that you could make another change to
    the source and check it in, but this process cuts to the chase.

    ![](media/image32.png){width="3.6453772965879265in"
    height="1.5831353893263342in"}

20. Accept the defaults and click **OK**.

    ![](media/image33.png){width="3.311321084864392in"
    height="2.7761581364829397in"}

21. Switch to browser tab open to the releases.

22. Click the **Releases** link to view release history.

    ![](media/image34.png){width="3.3867924321959757in"
    height="1.22665135608049in"}

23. If there are no releases in the view, refresh the browser every few
    seconds (or press the **Refresh** button in the UI). The build
    should complete pretty quickly and kick off the new release. When it
    appears, note that there is a single grey bar under
    **Environments**. This represents the **Dev** environment, which
    hasn’t begun yet. If the bar is blue, then that means the deployment
    is in progress. Green means it succeeded and red means it failed.
    Double-click the release to view the details.

    ![](media/image35.png){width="5.603772965879265in"
    height="0.9872462817147857in"}

24. There are many options for reviewing the release. Most of these are
    already familiar since you just went through the process of setting
    them up. But if you consider a scenario where there are many
    different releases occurring at the same time, it’s very useful to
    have easy access to all the settings and details used to define
    a release. Click the **Logs** tab to watch the process unfold.

    ![](media/image36.png){width="5.367924321959755in"
    height="2.212548118985127in"}

25. Return to the **Summary** tab and refresh the view using the inline
    **Refresh** button until the deployment succeeds.

    ![](media/image37.png){width="4.830188101487314in"
    height="2.37587489063867in"}

26. Return to the Fabrikam Fiber Dev browser tab and refresh it to
    confirm the changes have been deployed.

    ![](media/image38.png){width="3.73584864391951in"
    height="1.704569116360455in"}

**Exercise 2: Gated Releases**
------------------------------

1.  While automated releases are great, sometimes you want to gate their
    progress by requiring user approval. In this exercise, you will add
    a second environment to the release process for QA and user
    acceptance testing. In this scenario, you will allow the release to
    reach the QA site, but only if it successfully deploys to Dev. Once
    it’s available on QA, it won’t be considered “success” until
    approved manually. Note that it’s just as easy to also
    (or alternatively) have this human approval gate prior to
    the deployment.

#### Task 1: Adding a QA environment

1.  Return to the tab with all the releases (probably the third).

2.  Click the release name to return to its overview.

    ![](media/image39.png){width="2.632075678040245in"
    height="1.4257075678040245in"}

3.  Click **Edit** to enter edit mode.

    ![](media/image40.png){width="3.047169728783902in"
    height="1.354297900262467in"}

4.  Click the ellipses in the **Dev** environment and select **Clone
    environment**. Your **QA** environment is the same as **Dev**,
    except that it’s copied to a different output folder. Using this
    clone technique saves a lot of configuration time.

    ![](media/image41.png){width="2.664179790026247in" height="2.5in"}

5.  Change the name of the new environment to “QA” and press **Enter**.

    ![](media/image42.png){width="1.6230653980752405in"
    height="1.594339457567804in"}

6.  In the **Copy Files** task, change the final destination folder from
    “DEV” to “UAT” (short for “User Acceptance Testing”).

    ![](media/image43.png){width="3.9339621609798776in"
    height="1.284258530183727in"}

7.  Click the ellipses in the **QA** environment and select **Deployment
    conditions**. These will vary from the **Dev** environment.

    ![](media/image44.png){width="2.3301881014873143in"
    height="2.392603893263342in"}

8.  Instead of being after the release’s creation, this environment will
    be deployed to only after the release has been successfully deployed
    to **Dev** first. Select **After successful deployment on another
    environment** and select the **Dev** option. Click **OK**
    to confirm.

    ![](media/image45.png){width="4.943395669291339in"
    height="3.0711373578302714in"}

9.  Click the ellipses in the **QA** environment and select **Assign
    approvers**.

    ![](media/image46.png){width="2.3962259405074366in"
    height="2.4604101049868765in"}

10. In order for the release to **QA** to be considered successful,
    **Brian Keller** must personally sign off on it. For
    **Post-deployment approver**, select **Specific Users** and type
    Brian’s name in. Click **OK** to complete.

    ![](media/image47.png){width="5.0in" height="3.474892825896763in"}

11. **Save** the release.

    ![](media/image48.png){width="3.6603772965879267in"
    height="1.9312423447069116in"}

12. Open a new browser tab and navigate to the Fabrikam Fiber QA site.
    Note that it still has the original support text.

    ![](media/image49.png){width="4.0188681102362205in"
    height="1.8555019685039371in"}

13. Return to the browser tab open to the code view in TFS (probably the
    first one) and repeat the editing process to change the “Support
    v2.0” text to “Support v3.0”. Save and check in the change
    as before. This will kick off the build, which will hand off to the
    release to Dev, which will hand off to QA.

14. Return to the releases tab and click the link to view
    release history.

    ![](media/image50.png){width="3.358490813648294in"
    height="0.9664720034995625in"}

15. Note now that there are two release bars indicating status.
    Depending on how quickly you get here, these colors may vary by how
    far the release workflow has progressed. Refresh the data until you
    see the “awaiting approval” icon shown below (next to the blue bar).

    ![](media/image51.png){width="3.6226410761154857in"
    height="1.6334558180227472in"}

16. Switch to the QA site tab and refresh to confirm the deployment is
    as expected.

    ![](media/image52.png){width="3.8773589238845143in"
    height="1.3328423009623798in"}

17. Return to the releases tab and click the approval icon. Enter an
    optional message and click **Approve**.

    ![](media/image53.png){width="4.245283245844269in"
    height="2.2049146981627294in"}

18. Both bars are now green, indicating that both environment
    releases succeeded.

    ![](media/image54.png){width="4.339622703412074in"
    height="1.5210159667541556in"}

**Exercise 3: Releasing To Azure (optional)**
---------------------------------------------

The release management tools are incredibly flexible. Not only can you
automate virtually anything, you can even leverage some of the
higher-lever tasks to easily perform complex processes, such as
deploying to an Azure web site.

#### Task 1: Creating an Azure Web site and database

1.  Create an Azure account at <http://azure.com> if you don’t already
    have one.

2.  In a new browser tab, navigate to <https://portal.azure.com>.

<!-- -->

1.  Select **+New | Data + Storage | SQL Database (new database)** to
    create a new database.

    ![](media/image55.png){width="4.858490813648294in"
    height="1.4336701662292213in"}

2.  Enter “fabrikam” as the **Database name**. Select a subscription (it
    doesn’t matter which one, but use the same one for all steps in
    this lab). Select **+New** for **Resource group** and enter
    “fabrikam” as the name. Make sure **Select source** is set to
    **Blank database** and click **Configure required settings**.

    ![](media/image56.png){width="2.336550743657043in"
    height="3.3490562117235347in"}

3.  Enter a unique name for **Server name**, such as by including
    your name. Enter a admin username and password you can remember.
    Note that “P2ssw0rd” meets the password requirements. Click
    **Select** to select these options.

    ![](media/image57.png){width="2.270660542432196in"
    height="3.73584864391951in"}

4.  Click **Create** on the first blade to create the database
    and server. It’ll take some time to complete, but you can move on to
    the next step while it works in the background.

5.  Select **+New | Web + Mobile | Web App** to create a new Azure
    web site.

    ![](media/image58.png){width="4.603772965879265in"
    height="1.291613079615048in"}

6.  For **App name**, enter a unique name, such as by using your name
    as part. Select the same **Subscription** and **Resource group**
    as before. If required to create an **App Service plan**, accept
    the defaults. Click **Create** to create.

    ![](media/image59.png){width="2.448038057742782in"
    height="3.141509186351706in"}

7.  Click the **Resource groups** tab from the left menu. Locate and
    click the **fabrikam** group created earlier.

    ![](media/image60.png){width="3.594339457567804in"
    height="2.3603390201224848in"}

8.  Click the SQL Server (not the database) and click **Show firewall
    settings** in the new blade. There are two SQL icons, and the server
    is the one with the gear. The database is the one without.

    ![](media/image61.png){width="5.320754593175853in"
    height="1.1892115048118985in"}

9.  You need to allow your current IP address to access the database, so
    click **Add client IP** (which will default to your current IP) and
    then click **Save**. No other external IPs will be allowed to
    connect to your database unless you explicitly let them.

    ![](media/image62.png){width="1.7169805336832895in"
    height="1.0796741032370953in"}

10. From the **Resources** group, click your SQL database. In the new
    blade, click **Show database connection strings**.

    ![](media/image63.png){width="5.254716754155731in"
    height="1.2799945319335082in"}

11. This will provide you with a list of connection strings based
    on platform. Copy the **ADO.NET** string to your clipboard so you
    can configure your new web site to use it.

    ![](media/image64.png){width="5.528301618547681in"
    height="0.7607316272965879in"}

12. On the **fabrikam** database blade, click **Delete** and then
    confirm the deletion. You’ll publish an existing database using
    **SQL Server Management Studio** later on to save time.

    ![](media/image65.png){width="2.962263779527559in"
    height="1.2330238407699037in"}

13. In the **Resources** panel, click the web app created earlier. It’s
    the one with the globe icon by itself. In the rightmost blade that
    opens, click **Application settings**. Note that if the web app
    isn’t available yet, you can refresh the view by clicking the
    **fabrikam** link under **Resource group** in the database blade.

    ![](media/image66.png){width="5.641509186351706in"
    height="0.966169072615923in"}

14. On this blade you can configure settings for your app, such as
    connection strings. Locate the **Connection strings** section and
    add a new entry with the key “FabrikamFiber-Express” and the value
    pasted from the clipboard. You’ll need to locate the
    “{your\_password\_here}” section and replace it (including braces)
    with the actual SQL password entered earlier. Press **Enter**
    to complete.

    Server=tcp:
    fabrikam-johndoe.database.windows.net,1433;Database=fabrikam;User
    ID=johndoeadmin@fabrikam-johndoe;Password={your\_password\_here};Encrypt=True;TrustServerCertificate=False;Connection
    Timeout=30;

    ![](media/image67.png){width="4.609337270341207in"
    height="0.9716983814523185in"}

15. Click **Save** from the toolbar to commit.

    ![](media/image68.png){width="2.273584864391951in"
    height="1.169983595800525in"}

16. By now the SQL database should be available for use. From the
    **Start Menu**, enter “SQL Server Management Studio” and launch
    that app.

    ![](media/image69.png){width="2.700513998250219in"
    height="2.320754593175853in"}

17. By default, the settings are in place for the server that hosts the
    database you want to set up in the cloud. Click **Connect**
    to connect.

    ![](media/image70.png){width="3.3989304461942256in"
    height="2.547169728783902in"}

18. Right-click the **FabrikamFiber-Express** database and select
    **Tasks | Deploy Database to SQL Azure**.

    ![](media/image71.png){width="3.8867924321959757in"
    height="3.418419728783902in"}

19. On the **Introduction** page of the wizard, click **Next**.

20. Click **Connect** to set up the SQL Azure database connection.

    ![](media/image72.png){width="3.644051837270341in"
    height="2.367924321959755in"}

21. In the **Connect to Server** dialog, enter the connection details
    for your SQL Azure database. For example, if your database name was
    “fabrikam-johndoe”, then the **Server name**
    is “fabrikam-johndoe.database.windows.net”. Click **Connect**
    when done. Note that if you plan to copy/paste any of this into the
    dialog you’ll want to first paste the current clipboard contents
    (the SQL script) into Notepad for temporary safekeeping.

    ![](media/image73.png){width="3.0672255030621174in"
    height="2.311321084864392in"}

22. Dasads

    ![](media/image74.png){width="3.5754713473315833in"
    height="2.5145417760279964in"}

23. Click **Finish** on the final page of the wizard to deploy
    the database.

    ![](media/image75.png){width="4.292452974628172in"
    height="3.994365704286964in"}

#### Task 2: Configuring the build to produce a Web Deploy package

1.  Return to the browser tabs open to the builds section of the portal.

2.  Click **Edit** to edit the build definition.

    ![](media/image76.png){width="3.5516393263342083in"
    height="1.770612423447069in"}

3.  Select the **Visual Studio Build** step and add the following
    arguments after the existing arguments. Be sure to include a space
    before adding the new arguments.

    /p:DeployOnBuild=true /p:WebPublishMethod=Package
    /p:PackageAsSingleFile=true /p:SkipInvalidConfigurations=true

    ![](media/image77.png){width="5.877358923884515in"
    height="1.9434219160104986in"}

4.  Click **Save** to save the build definition. It will now produce the
    web deploy zip needed for publication to Azure.

    ![](media/image78.png){width="2.962263779527559in"
    height="1.1878379265091863in"}

#### Task 3: Creating a release environment for Azure

1.  Return to the releases tab.

<!-- -->

1.  Everything has been set up for releasing to Azure, so you just need
    to add an environment for it. Click the **Edit** link to enter
    edit mode.

    ![](media/image79.png){width="2.1604768153980753in"
    height="1.5849059492563429in"}

2.  Click **Add environments**.

    ![](media/image80.png){width="2.5566032370953633in"
    height="1.7949015748031496in"}

3.  Select the **Azure Website Deployment** template and click **OK**.

    ![](media/image81.png){width="3.7169805336832895in"
    height="2.9645548993875765in"}

4.  Set the name of the new environment to **Prod-Azure** and press
    **Enter**.

    ![](media/image82.png){width="1.3308825459317586in" height="2.5in"}

5.  Remove the **Visual Studio Test** task from the workflow to keep
    things simple.

    ![](media/image83.png){width="3.188678915135608in"
    height="1.4356266404199476in"}

6.  Since you’re deploying to production, the controls will be a
    little tighter. You will want to have manual approval both before
    and after the release has been deployed. Click the ellipses in the
    **Prod-Azure** environment and select **Assign approvers**.

    ![](media/image84.png){width="2.4041382327209098in"
    height="2.594339457567804in"}

7.  For both **Approvers** options, select **Specific Users** and enter
    **Brian Keller** as both. Click **OK** to confirm.

    ![](media/image85.png){width="5.462263779527559in"
    height="4.243758748906386in"}

8.  You will also need to decide when the release process begins, so
    click the ellipses in **Prod-Azure** and select **Deployment
    conditions**.

    ![](media/image86.png){width="2.6509437882764653in"
    height="2.753509405074366in"}

9.  For **Trigger**, select **After successful deployment on another
    environment** and select **QA**. Note that this simply means that
    this process will begin after that deployment is
    marked “successful”. Any actual deployment will still require the
    manual approval configured earlier. Click **OK** to apply.

    ![](media/image87.png){width="5.641509186351706in"
    height="3.5211209536307964in"}

10. It’s now time to configure the connection to Azure. Click the
    **Manage** link next to the **Azure Subscription** field. This will
    bring you to the Azure connection configuration page.

    ![](media/image88.png){width="4.292452974628172in"
    height="1.0372725284339457in"}

11. Click **New Service Endpoint | Azure**.

    ![](media/image89.png){width="1.9921128608923884in"
    height="3.301887576552931in"}

12. Select **Certificate Based** and click the **publish settings file**
    option at the bottom. This will open a link to download a publish
    settings file that contains the details needed to complete
    this form.

    ![](media/image90.png){width="5.23584864391951in"
    height="2.877516404199475in"}

13. When prompted by the browser, select **Save As**, change the name to
    “creds.txt”, and save it to the desktop for easy access. Note that
    the browser may ask you to log in first.

14. Open “creds.txt” using notepad. It’s XML, but you’ll be able to
    parse out what you need by hand.

15. Locate the three key fields needed to configure the
    Azure connection. Note that if you have multiple Azure
    subscriptions, you’ll need to make sure you’re working with the one
    used to create the SQL server and web site earlier.

    ![](media/image91.png){width="5.433962160979878in"
    height="2.716981627296588in"}

16. Set the **Connection** name to “Fabrikam Azure” and configure the
    remaining details using the data from creds.txt. Note that
    **Management Certificate** is all on the same line, despite the
    appearance with word wrapping. Click **OK** to continue.

    ![](media/image92.png){width="5.386792432195976in"
    height="2.9432053805774276in"}

17. After the connection has been created, you can close this tab.

18. Return to the releases tab. Click the **Refresh** button next to the
    **Manage** link. This will enable you to select the **Azure
    Subscription** connection you just created. Type in the **Web App
    Name** of the Azure web site created earlier and select the **Web
    App Location** used during creation.

    ![](media/image93.png){width="3.773584864391951in"
    height="0.9544083552055993in"}

19. Set the **Web Deploy Package** to the path below. Note that you
    could also specify additional arguments, such as a connection
    string, as part of this workflow if required.

    \$(System.DefaultWorkingDirectory)/Fabrikam Development
    CI/drop/\_PublishedWebsites/FabrikamFiber.Web\_Package/FabrikamFiber.Web.zip

20. Save the release.

    ![](media/image94.png){width="4.528301618547681in"
    height="1.890764435695538in"}

#### Task 4: Checking in a change to kick off the release workflow

1.  Return to the code browser tab and locate the path below.

    \$/FabrikamFiber/Dev/FabrikamFiber.CallCenter/FabrikamFiber.Web/Global.asax.cs

<!-- -->

1.  Click the **Edit** button and comment out the
    **Database.SetInitializer** call in **Application\_Start**. This
    won’t work properly in Azure, so it needs to be commented out. It
    doesn’t matter since the DB was already set up manually.

2.  Save the file to check it in.

    ![](media/image95.png){width="5.207547025371828in"
    height="1.3330435258092739in"}

3.  Return to the releases tab in the browser. If the new release
    process doesn’t show up within a minute, refresh the window or use
    the refresh button. Approve the first two requests to begin the
    Azure deployment. You’ll know the bits have been deployed to
    production when you’re asked for the post-release signoff.

    ![](media/image96.png){width="5.339622703412074in"
    height="1.5751881014873141in"}

4.  Open a browser tab to the Azure site to confirm the deployment
    worked as expected. For example, if you named your site
    fabrikam-johndoe, then the URL would be
    <http://fabrikam-johndoe.azurewebsites.net>.

    ![](media/image97.png){width="4.896225940507437in"
    height="1.7676202974628172in"}

5.  Return to the releases tab and approve the release by clicking the
    icon, optionally entering a message, and clicking **Approve.**

    ![](media/image98.png){width="5.132075678040245in"
    height="2.2539523184601924in"}

6.  Now everyone can easily see that the most recent release made it all
    the way through the release pipeline and is live in the cloud.

    ![](media/image99.png){width="2.197642169728784in"
    height="0.5728455818022747in"}

<!-- -->

1.  

<!-- -->

1.  

<!-- -->

1.  
