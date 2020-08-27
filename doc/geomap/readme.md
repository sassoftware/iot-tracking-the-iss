# Create the GEO Maps in SAS ESP Streamviewer

You can create the following GEO Maps to view the output using SAS ESP Streamviewer.

>   Ensure the model is executing on the SAS ESP XML Server.

Start SAS ESP Streamviewer.

## iss Window GEO Map

1. Click <img src='../../images/show_model_icon.png'> to open the ESP Model Viewer.
 
    <img src='../../images/model_viewer.png'>

2.  Click the **iss** window to select it and then click <img src='../../images/subscriber_icon.png'>  to add an Updating Subscriber to the dashboard. Click **Close** to close the ESP Model Viewer. A table appears on the dashboard.

3.  In the upper-right corner of the table, click <img src='../../images/dot_icon.png'> and then select **Edit**. The Modify Chart screen appears.
 
    <img src='../../images/modify_chart.png' width='60%'>

4.  Select **GEO Map**.
  
5.  Select the appropriate variables as follows:

    |  |  |
    | ------ | ------ |
    | Latitude | lat |
    | Longitude | long |
    | Size | (blank) |
    | Color | (blank) |
    | Data Label | (blank) |
    
6.  Click **OK**. The GEO Map will appear and automatically adjust the zoom factor as more data appears. You can also manually adjust the zoom factor with the mouse wheel.

    <img src='../../images/iss.png'>
    
## geoCircle Window GEO Map

1. Click <img src='../../images/show_model_icon.png'> to open the ESP Model Viewer.
 
2.  Click the **geoCircle** window to select it and then click <img src='../../images/subscriber_icon.png'>  to add an Updating Subscriber to the dashboard. Click **Close** to close the ESP Model Viewer. A table appears on the dashboard.

3.  In the upper-right corner of the table, click <img src='../../images/dot_icon.png'> and then select **Edit**. The Modify Chart screen appears.
 
    <img src='../../images/modify_chart2.png'>

4.  Select **GEO Map**.
  
5.  Select the appropriate variables as follows:

    |  |  |
    | ------ | ------ |
    | Latitude | lat |
    | Longitude | long |
    | Size | distToCenter |
    | Color | distToCenter |
    | Data Label | cirDesc |
    
6.  Click **OK**. The GEO Map will appear and automatically adjust the zoom factor as more data appears. You can also manually adjust the zoom factor with the mouse wheel.

    <img src='../../images/geocircle.png'>
    
## geoProximityAnalysis Window GEO Map

1. Click <img src='../../images/show_model_icon.png'> to open the ESP Model Viewer.
 
2.  Click the **geoProximityAnalysis** window to select it and then click <img src='../../images/subscriber_icon.png'>  to add an Updating Subscriber to the dashboard. Click **Close** to close the ESP Model Viewer. A table appears on the dashboard.

3.  In the upper-right corner of the table, click <img src='../../images/dot_icon.png'> and then select **Edit**. The Modify Chart screen appears.
 
4.  Select **GEO Map**.
  
5.  Select the appropriate variables as follows:

    |  |  |
    | ------ | ------ |
    | Latitude | lat |
    | Longitude | long |
    | Size | distToEdge |
    | Color | distToEdge |
    | Data Label | polyDesc |
    
6.  Click **OK**. The GEO Map will appear and automatically adjust the zoom factor as more data appears. You can also manually adjust the zoom factor with the mouse wheel.

    <img src='../../images/geoprox.png'>
    
