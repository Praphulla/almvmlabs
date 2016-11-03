#Exercise 2: Agile Portfolio Management

1.  In this exercise, you will learn about some of the agile portfolio
    management capabilities provided by Team Foundation Server. These
    capabilities allow larger organizations to understand the scope of
    work across several teams and see how that work rolls up into
    broader initiatives. In this exercise, you will explore how multiple
    teams at Fabrikam Fiber can collaborate together to work
    on features.

###Task 1: Configuring Team Hierarchy and Area Paths

1.  Let’s start out by taking a look at the Fabrikam Fiber project from
    the top-down, in a manner that would typically be associated with a
    management role.

2.  Click the gear icon in the top-right corner of the web portal. This
    opens the administration pages in a new tab.

  <img src="./media/image45.png" width="221" height="67" />

   <b>Figure 40:</b> Loading administration site

1.  Navigate to the **FabrikamFiber** project node.

  <img src="./media/image46.png" width="624" height="70" />

   <b>Figure 41:</b> Navigate to project node

1.  The FabrikamFiber project has five teams, with the **Fabrikam Fiber
    Leadership Team** assigned as the project default.

  <img src="./media/image47.png" width="624" height="287" />

   <b>Figure 42:</b> Fabrikam Fiber teams

1.  Select the **Areas** tab.

  <img src="./media/image48.png" width="571" height="76" />
   
   <b>Figure 43:</b>  Areas tab

1.  The management team currently owns the **Development** area and
    all sub-areas. This gives them visibility into the backlog of all
    teams, even for work items that are not mapped to features.
    Optionally, the management team could also choose to not include
    sub-areas, thereby removing work items from their product backlog
    view as soon as they are assigned to one of the teams.

  <img src="./media/image49.png" width="484" height="355" />
   
   <b>Figure 44:</b> Area configuration for management team

1.  Select the **Overview** tab.

  <img src="./media/image50.png" width="562" height="71" />

   <b>Figure 45:</b> Overview tab

1.  Click **Fabrikam Fiber Database Team**.

  <img src="./media/image51.png" width="335" height="271" />

   <b>Figure 46:</b>  Fabrikam Fiber Database Team link

1.  Select the **Areas** tab.

  <img src="./media/image52.png" width="568" height="72" />

   <b>Figure 47:</b>  Areas tab


1.  The Database team is currently configured to see work items from
    just the root Development area and the Database Team sub-area. This
    allows them to see backlog items created by the management team and
    ones specifically assigned to their team. With this kind of
    structure, each team can work independently on its own backlog,
    defined by its area path, unrelated to the other team’s work.

  <img src="./media/image53.png" width="490" height="350" />

   <b>Figure 48:</b>  Area configuration for Database team

1.  Close the administration tab in Internet Explorer to return to the
    web portal browser tab.

2.  From the top navigation, select **FabrikamFiber | Browse all**.

    <img src="./media/image54.png" width="563" height="284" />

3.  Select the **Fabrikam Fiber Leadership Team** and click
    **Navigate**.

   <img src="./media/image55.png" width="569" height="434" />

   <b>Figure 49:</b>  Navigating to management team

###Task 2: Portfolio Management

1.  Switch to the **Backlog** view if necessary.

  <img src="./media/image56.png" width="580" height="134" />

   <b>Figure 50:</b> Returning to Backlog view

1.  The leadership team can see backlog items across all teams,
    including status and scheduled iteration.

  <img src="./media/image57.png" width="580" height="304" />

   <b>Figure 51:</b>  Backlog items for leadership team

1.  The backlog view also includes the ability to toggle the display of
    in-progress work items. Toggle the “**In progress items**” link in
    the top-right corner of the backlog view and note that the Committed
    work items are no longer displayed. Toggle the link once again to
    view in-progress items before moving on.

  <img src="./media/image58.png" width="430" height="78" />

   <b>Figure 52:</b>  Location of link to show/hide in-progress items

1.  Note that the in-progress work items are no longer displayed. Toggle
    the link once again to view in-progress items as before.

  <img src="./media/image59.png" width="577" height="225" />

   <b>Figure 53:</b> Location of link to show/hide in-progress items

1.  Click **Features** to view the feature backlog.

   <img src="./media/image60.png" width="183" height="169" />

    <b>Figure 54:</b>  Viewing features backlog

1.  This view shows the top-level features for the project. It is
    possible to drill down into backlog items and even individual tasks
    if desired. Click the **Expand** button to expand one level.

   <img src="./media/image61.png" width="423" height="110" />

    <b>Figure 55:</b>  Expand button

   <img src="./media/image62.png" width="586" height="161" />

    <b>Figure 56:</b>Expanded view

1.  Click the **Expand** button once again to drill down into tasks.

   <img src="./media/image63.png" width="544" height="264" />

   <b>Figure 57:</b>  Expanded view

1.  It is also possible to re-parent work items using drag-and-drop
    operations in the portfolio backlog view. Try this out by dragging
    and dropping one of the Product Backlog Items from one feature
    to another.

   <img src="./media/image64.png" width="576" height="185" />

   <b>Figure 58:</b>  Re-parent work items using drag and drop

1.  Note that this moved the Product Backlog Item as well as all of the
    child tasks. Drag the Product Backlog Item back to its
    original feature.

2.  The child work items are always shown for the leadership team,
    regardless of which team they are assigned to. To see this more
    clearly, let’s add the **Area Path** column to the view.

3.  Click **Column Options**.

    <img src="./media/image65.png" width="475" height="111" />

     <b>Figure 59:</b>  Column Options button

1.  **Double-click** **Area Path** from the available columns and then
    click **OK**.

    <img src="./media/image66.png" width="210" height="261" />

      <b>Figure 60:</b> Add Area Path column

    <img src="./media/image67.png" width="485" height="300" />

      <b>Figure 61:</b> Add Area Path column

1.  If you look at the area path column for different product backlog
    items, you can see that they are assigned to different teams. The
    ability to drill down into the various backlogs gives the management
    team the desired level of visibility into the breakdown and
    implementation of features.

   <img src="./media/image68.png" width="592" height="151" />

    <b>Figure 62:</b>  Area path column showing assigned teams

1.  Now let’s take a look at how to create a new feature and then link
    it to a work item that will be assigned to one of the agile teams.
    Create a new feature titled “**Reporting for technicians and
    services**” and then click the **Add** button.

   <img src="./media/image69.png" width="551" height="162" />

   <b>Figure 63:</b>  Creating new feature

1.  Click the green ‘**+**’ button that is on the left-hand side of the
    new Feature.

   <img src="./media/image70.png" width="567" height="60" />

   <b>Figure 64:</b> Adding new PBI


1.  Create a new Product Backlog Item named “**Modify databases to
    support on-demand reporting for technician activity**”. Assign it to
    the database team lead, **Adam Barr**. Set the Area to the
    **Database** team so that it shows up on their backlog. Finally,
    click **Save and Close**.

   <img src="./media/image71.png" width="576" height="390" />

    <b>Figure 65:</b>  Adding new PBI

1.  **Note:** In the event that you create items within the backlog, you
    can also easily map them to parent Features by enabling the Mapping
    feature and then dragging and dropping.

    <img src="./media/image72.png" width="566" height="264" />

1.  Now let’s load the web portal for the database team. Navigate to the
    **Fabrikam Fiber Database Team** using the top navigation as before.

1.  <img src="./media/image73.png" width="530" height="408" />

1.  Navigate to database team

1.  You should now be looking at the backlog for the database team.

1.  <img src="./media/image74.png" width="624" height="188" />

1.  Backlog Items link

1.  Although this team may normally only want to view their backlog
    items, they may also want to see how those backlog items fit in to
    the bigger picture. Toggle the **Parents** option that is currently
    set to Hide.

1.  <img src="./media/image75.png" width="624" height="59" />

1.  Toggle display of parent nodes

1.  Note that the backlog view now shows parent Feature items.

1.  <img src="./media/image76.png" width="624" height="283" />

1.  Backlog showing parent features

1.  To get a more complete view of their organization’s overall work,
    the database team can also view the Features backlog. Click
    **Features**.

1.  <img src="./media/image77.png" width="192" height="134" />

1.  Features backlog

1.  Click the **Expand** button twice in order to expand the features
    backlog two levels. Note that it is easy to distinguish between work
    that the database team is contributing to or is assigned, and work
    that is assigned to other teams by looking at the colored bar. If
    the bar is hollow (not filled in), this means that the work is
    assigned to a different team.

1.  <img src="./media/image78.png" width="624" height="249" />

1.  Viewing work assigned to team vs. other teams
