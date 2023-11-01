# Adding New Assets

## Web Portal 

 1. Find the Add form: select Assets in the sidebar, then Create New.
 2. Fill out the form.
    a. Fields marked with an * are required--all others are optional.
    b. Categories/asset groups/locations/asset types should be configured prior to adding assets (see [setup instructions](https://github.com/TEC-RFID/rfid-asset-documentation/blob/main/users/setup.md)).
    c. Any custom fields you’ve configured that are specific to asset types will appear once you’ve selected the correct type.
    d. On the web, just type placeholder text into the EPC field and add the tag data in the app later. 
 3. When you’re ready, press Save.

## Android App

 1. Find the Add form: from the main menu, press View Assets, then press Add (green button, top right corner).
 2. Fill out the form.
    a. Fields marked with an * are required--all others are optional.
    b. Categories/asset groups/locations/asset types should be configured prior to adding assets (see [setup instructions](https://github.com/TEC-RFID/rfid-asset-documentation/blob/main/users/setup.md)).
    c. Any custom fields you’ve configured that are specific to asset types will appear once you’ve selected the correct type.
    d. If you have the tag handy, see below for how to add the EPC (skip to step 3). If you don't have the tag yet, just type a placeholder in the EPC field and come back to it later. 
 4. When you’re ready, press Save.

## Adding EPC Data In The App

‘EPC’ stands for Electronic Product Code: it’s the unique identification code encoded into each RFID tag. In order to track your assets using RFID, you will need to record the EPC for each asset.

If you’re adding a large quantity of assets, the simplest way is to import them on the web portal ([click here](https://github.com/TEC-RFID/rfid-asset-documentation/blob/main/users/importingassets.md)), then add the EPCs to the asset records as you tag your assets.

 1. Find and select the correct asset record.
    a. From the app’s main menu, select View Assets.
    b. Find the asset you’re looking for, either by scrolling or using the search box, and press the asset name to open the record.
 2. Once you have the right asset selected, press Edit.
 3. Find the ‘EPC RFID Code’ field and press the magnifying glass symbol to the right.
 4. Using the slider, set the reader’s power level to low. (This is to avoid accidentally scanning the wrong tag.)
 5. Hold the reader to the correct tag and press Start Scan. The app will automatically detect the nearest tag and add it to the EPC field in the edit form.
 6. Press Done, then Update.
