
#Exercise 4: Work Item Charting

1.  In this exercise, we will demonstrate the work item charting
    capability of Team Foundation Server. Work item charting allows you
    to create visual chart representations of the data returned from TFS
    work item queries. This can be used to help better understand the
    state of projects.

#### <span id="_Toc429723519" class="anchor"><span id="_Toc451341241" class="anchor"></span></span>Task 1: Creating and Sharing Work Item Charts

1.  Navigate to the **Fabrikam Fiber Leadership Team** (if necessary).

<!-- -->

1.  <img src="./media/image119.png" width="624" height="478" />

<!-- -->

1.  Figure

<!-- -->

1.  Navigating to management team

<!-- -->

1.  

<!-- -->

1.  Let’s say that the Fabrikam Fiber management team would like to
    better understand how tasks are broken down by user. Navigate to the
    work item queries section of the web portal.

<!-- -->

1.  <img src="./media/image128.png" width="416" height="95" />

<!-- -->

1.  Figure

<!-- -->

1.  Work item queries view

<!-- -->

1.  

<!-- -->

1.  Since these charts are based on work items, we first need to define
    a query that will return the data that we are interested in. Click
    **New** and select the **New Query** option.

<!-- -->

1.  <img src="./media/image129.png" width="224" height="154" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating a new work item query

<!-- -->

1.  

<!-- -->

1.  The default query will select all work items in any state for the
    current project. We want to select just Tasks, so modify the value
    of clause for **Work Item Type** to be **Task**.

<!-- -->

1.  <img src="./media/image130.png" width="648" height="224" />

<!-- -->

1.  Figure

<!-- -->

1.  Querying for all tasks

<!-- -->

1.  Click the **Save Query As** button.

<!-- -->

1.  <img src="./media/image131.png" width="404" height="72" />

<!-- -->

1.  Figure

<!-- -->

1.  Saving new query

<!-- -->

1.  

<!-- -->

1.  **Note:** Work item charts require the associated query to return a
    flat list of work items.

<!-- -->

1.  Name the query “**All Tasks”**, select the folder “**Shared
    Queries**”, and then click **OK**.

<!-- -->

1.  <img src="./media/image132.png" width="497" height="178" />

<!-- -->

1.  Figure

<!-- -->

1.  Naming new query

<!-- -->

1.  

<!-- -->

1.  Select the **Charts** tab.

<!-- -->

1.  <img src="./media/image133.png" width="225" height="72" />

<!-- -->

1.  Figure

<!-- -->

1.  Charts link

<!-- -->

1.  

<!-- -->

1.  First we will create a pie chart showing tasks by assigned user.
    Click **New Chart**.

<!-- -->

1.  <img src="./media/image134.png" width="220" height="122" />

<!-- -->

1.  Figure

<!-- -->

1.  New Chart button

<!-- -->

1.  

<!-- -->

1.  Title the chart “**Tasks by User**”, group by the **Assigned To**
    field, and then click **OK**.

<!-- -->

1.  <img src="./media/image135.png" width="624" height="335" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating new pie chart

<!-- -->

1.  

<!-- -->

1.  Let’s create one more chart to help visualize the task progress for
    each team member. Click **New Chart** once again.

2.  Select the **Stacked Bar** chart type. Note that this chart type
    requires you to specify two different fields for the rows
    and columns.

<!-- -->

1.  <img src="./media/image136.png" width="193" height="242" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating a new stacked bar chart

<!-- -->

1.  

<!-- -->

1.  Title the chart “**Task State by User**”, select the **Assigned To**
    field for the **Rows**, select the **State** field for the
    **Columns**, and finally click **OK** to create the chart.

<!-- -->

1.  <img src="./media/image137.png" width="624" height="412" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating a new stacked bar chart

<!-- -->

1.  

<!-- -->

1.  <img src="./media/image138.png" width="624" height="426" />

<!-- -->

1.  Figure

<!-- -->

1.  New task charts

<!-- -->

1.  

<!-- -->

1.  You can add to the available grouping options by modifying the work
    item query and adding in additional display columns. Select the
    **Editor** tab for the query.

<!-- -->

1.  <img src="./media/image139.png" width="203" height="75" />

<!-- -->

1.  Figure

<!-- -->

1.  Editor link

<!-- -->

1.  

<!-- -->

1.  Click **Column Options**.

<!-- -->

1.  <img src="./media/image140.png" width="412" height="115" />

<!-- -->

1.  Figure

<!-- -->

1.  Column Options button

<!-- -->

1.  

<!-- -->

1.  Select the **Task** item for the **Work Item Type**.

<!-- -->

1.  <img src="./media/image141.png" width="563" height="176" />

<!-- -->

1.  Figure

<!-- -->

1.  Filtering for Task fields

<!-- -->

1.  

<!-- -->

1.  **Double-click** the **Area Path** option from the Available
    Columns list.

<!-- -->

1.  <img src="./media/image142.png" width="205" height="106" />

<!-- -->

1.  Figure

<!-- -->

1.  Selecting the Area Path field

<!-- -->

1.  

<!-- -->

1.  Click **OK**.

<!-- -->

1.  <img src="./media/image143.png" width="560" height="419" />

<!-- -->

1.  Figure

<!-- -->

1.  Selecting the Area Path field

<!-- -->

1.  

<!-- -->

1.  Click the **Save** button.

<!-- -->

1.  <img src="./media/image144.png" width="292" height="112" />

<!-- -->

1.  Figure

<!-- -->

1.  Saving modified query

<!-- -->

1.  

<!-- -->

1.  Select the **Charts** link to return to the charts view and use your
    charting skills to create a pie chart showing tasks grouped by the
    **Area Path** field. Title the chart “**Tasks by Team**”, select the
    **Area Path** field for the **Group By** field, and finally click
    **OK** to create the chart. This gives the management team an idea
    of how the work is distributed amongst the teams.

<!-- -->

1.  <img src="./media/image145.png" width="618" height="411" />

<!-- -->

1.  Figure

<!-- -->

1.  Creating new pie chart

<!-- -->

1.  

<!-- -->

1.  These lightweight charts can also be pinned to a dashboard. Click
    the **Tasks by Team** chart’s ellipses button and select **Add to
    dashboard | Overview**. This dashboard is used on the project’s
    home page.

<!-- -->

1.  <img src="./media/image146.png" width="580" height="303" />

<!-- -->

1.  Figure

<!-- -->

1.  Task breakdown by team

<!-- -->

1.  

<!-- -->

1.  Click the **Home** link to return to the leadership team’s homepage
    and view the pinned chart.

<!-- -->

1.  <img src="./media/image147.png" width="421" height="93" />

<!-- -->

1.  Figure

<!-- -->

1.  Home link

<!-- -->

1.  

<!-- -->

1.  <img src="./media/image148.png" width="608" height="424" />

<!-- -->

1.  Figure

<!-- -->

1.  Team homepage showing pinned chart

#### Task 2: Customizing Dashboard

1.  You can also customize a dashboard by clicking the **Edit** button
    in the bottom right corner. This will switch the dashboard into
    **edit mode**. You need to be in edit mode in order to rearrange the
    dashboard or make configuration changes, which removes the risk of
    accidental edits during normal usage.

    <img src="./media/image149.png" width="418" height="250" />

2.  Utilize the **Remove** buttons to clean up the dashboard a bit. It
    doesn’t matter which items you remove.

    <img src="./media/image150.png" width="596" height="305" />

3.  You can also easily add new items to the dashboard by clicking the
    **Add Widget** button. Try it now.

    <img src="./media/image151.png" width="218" height="196" />

4.  Select the **Markdown** widget and click **Add**. This widget allows
    you to display any markdown file from your repository on
    the dashboard. Alternatively, you can provide the markdown manually.

    <img src="./media/image152.png" width="593" height="258" />

5.  Locate the Markdown widget on your dashboard and click its
    **Edit** button.

    <img src="./media/image153.png" width="346" height="179" />

6.  This will provide you with access to key settings, such as the size
    of the widget, as well as the source of the Markdown to display.
    Press **Esc** to cancel.

    <img src="./media/image154.png" width="429" height="525" />

7.  Click the **Manage Dashboards** button in the top right corner of
    the view.

    <img src="./media/image155.png" width="347" height="125" />

8.  This dialog provides access to functionality for managing your
    dashboard, including its creation. Note that each dashboard has an
    option to **Auto-refresh dashboard**, which is great for scenarios
    where you want to display information in public team areas, such as
    on large TVs.

    <img src="./media/image156.png" width="445" height="161" />

9.  When satisfied, click the **Close Edit Mode** button to apply
    all changes.

    <img src="./media/image157.png" width="321" height="206" />

10. You can also create additional tabs for your dashboard in orders to
    offer different views into the project. Click the **Add a new
    Dashboard** button to create a new dashboard.

    <img src="./media/image158.png" width="364" height="97" />

11. Enter **“Quality”** as the name and press **Enter**.

    <img src="./media/image159.png" width="426" height="66" />

12. You now have multiple dashboard tabs and can edit and customize each
    using the same process from earlier.

    <img src="./media/image160.png" width="417" height="133" />

<!-- -->

1.  **Note**: After completing this lab, the virtual machine will
    continue to run with the date & time that was set for demonstration
    purposes at the beginning of this lab. Don’t forget to reset the
    virtual machine to its original snapshot/checkpoint after you
    complete this lab.

<!-- -->

1.  1.  2.  

    <!-- -->

    1.  


