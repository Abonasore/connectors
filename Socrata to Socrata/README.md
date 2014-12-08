# Socrata to Socrata FME Template

This workflow demonstrates how to extract data from an existing Socrata dataset, perform an example data transformation (filtering out features by attribute value) and the publishing the resulting data to a different Socrata dataset.

[View preview of workflow](#)

## Quickstart

Follow these steps to get the example workflow working to create a new dataset on your data portal.

1. [Download the workflow](#) and open it in FME Desktop.

2. Ensure the CSV Reader is pointing to `https://data.mo.gov/api/views/wu22-kvdm/rows.csv?accessType=DOWNLOAD` by editing the 'Source CSV' under `rows[CSV]` in the Navigator panel in the upper left of FME.
**NOTE:** verify that you can actually download the CSV when you input `https://data.mo.gov/api/views/wu22-kvdm/rows.csv?accessType=DOWNLOAD` into a web browser. 

2. Update your Socrata credentials for the Socrata writer by editing the following under the Socrata writer (look for `<not set> [Socrata]`) in the Navigator panel:
    - Domain (e.g. data.seattle.gov)
    - User
    - Password

3. Run the workflow and ensure a new dataset was created on your domain.


## Adapting the workflow for datasets

1. Obtain the download URL for your source Socrata dataset by navigating to the dataset in a web browser. Click the blue 'Export' button and copy the 'CSV' link under Download As. **Right click > Copy link address**

2. Paste this CSV download link into the 'Source CSV' field under `rows[CSV]` in the Navigator panel in FME.

3. To configure the dataset to publish to and the update method refer to 'Steps 3 and 4' of [this guide](http://dev.socrata.com/publishers/examples/fme-socrata-writer.html#setting-up-the-workflow-in-fme-desktop).

4. Run the workflow!