# smartdrawing.kapsel

> Integrate SAP Fiori apps with Smart Drawing app in order to be able to show drawings, interact with them as well as call from drawings fiori app

## Installation

This requires phonegap/cordova CLI 5.0+ ( current stable v1.3.0 )

```
phonegap plugin add com.keel.smartdrawing.cordova
```
or 

```
cordova plugin add com.keel.smartdrawing.cordova
```

It is also possible to install via repo url directly ( unstable )

```
phonegap plugin add https://github.com/...
```

or 

```
cordova plugin add https://github.com/...
```

## Supported Platforms

- Android

## Quick Example


```javascript
var sEquipmentId = this.getView().getBindingContext().getProperty("equipmentId");
var sDrawingId = this.getView().getBindingContext().getProperty("drawingId");

//prepare JSON data for single equipment
var equipment = {
  equipmentId: sEquipmentId,
  color: "#ff0000", //red
  status: "Active"
  };
		
//keep it as single element in array of equipments to be shown on drawing
var equipmentArr = [];
equipmentArr.push(equipment);
		
//Show on drawing
SmartDrawing.showData("Equipment from Fiori", sDrawingId, equipmentArr,
  //success
  null,
  //failure
  function(err) {
  	MessageToast.show("SmartDrawing plugin call failed " + err);
  });
```

## API

...
