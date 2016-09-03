# alfresco-google-map-apikey
Share Override to support API KEY 
##
Installation
* Copy `google-map-share-amp-1.0-SNAPSHOT.amp` into INSTALL_DIR/amps_share/
* Configure Share Custom Config with your [Google Map API KEY]
* Stop Alfresco
* Use the Alfresco [apply-amp] -force command. Force is needed since this is a simple override of existing module.
* Start Alfresco, then browse items with geolocations properties on them, and click: "View on Map."

## Configurations
Edit `tomcat/shared/classes/alfresco/web-extension/share-config-custom.xml` to add the following
```xml
 <config evaluator="string-compare" condition="GoogleMap">
        <apikey>YOUR_GOOGLE_API_KEY</apikey>
  </config>
```


[apply-amps]:http://docs.alfresco.com/5.1/tasks/amp-install.html
[Google Map API KEY]:https://developers.google.com/maps/documentation/javascript/get-api-key
