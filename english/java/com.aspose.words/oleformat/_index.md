---
title: OleFormat
linktitle: OleFormat
second_title: Aspose.Words for Java
description: Provides access to the data of an OLE object or ActiveX control in Java.
type: docs
weight: 453
url: /java/com.aspose.words/oleformat/
---

**Inheritance:**
java.lang.Object
```
public class OleFormat
```

Provides access to the data of an OLE object or ActiveX control.

To learn more, visit the [ Working with Ole Objects ][Working with Ole Objects] documentation article.

 **Remarks:** 

Use the [Shape.getOleFormat()](../../com.aspose.words/shape/\#getOleFormat) property to access the data of an OLE object. You do not create instances of the [OleFormat](../../com.aspose.words/oleformat/) class directly.

 **Examples:** 

Shows how to extract embedded OLE objects into files.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```


[Working with Ole Objects]: https://docs.aspose.com/words/java/working-with-ole-objects/
## Methods

| Method | Description |
| --- | --- |
| [getAutoUpdate()](#getAutoUpdate) | Specifies whether the link to the OLE object is automatically updated or not in Microsoft Word. |
| [getClsid()](#getClsid) | Gets the CLSID of the OLE object. |
| [getIconCaption()](#getIconCaption) | Gets icon caption of OLE object. |
| [getOleControl()](#getOleControl) | Gets [getOleControl()](../../com.aspose.words/oleformat/\#getOleControl) objects if this OLE object is an ActiveX control. |
| [getOleEntry(String oleEntryName)](#getOleEntry-java.lang.String) |  |
| [getOleIcon()](#getOleIcon) | Gets the draw aspect of the OLE object. |
| [getOlePackage()](#getOlePackage) | Provide access to [OlePackage](../../com.aspose.words/olepackage/) if OLE object is an OLE Package. |
| [getProgId()](#getProgId) | Gets the ProgID of the OLE object. |
| [getRawData()](#getRawData) | Gets OLE object raw data. |
| [getSourceFullName()](#getSourceFullName) | Gets the path and name of the source file for the linked OLE object. |
| [getSourceItem()](#getSourceItem) | Gets a string that is used to identify the portion of the source file that is being linked. |
| [getSuggestedExtension()](#getSuggestedExtension) | Gets the file extension suggested for the current embedded object if you want to save it into a file. |
| [getSuggestedFileName()](#getSuggestedFileName) | Gets the file name suggested for the current embedded object if you want to save it into a file. |
| [isLink()](#isLink) | Returns  true  if the OLE object is linked (when [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) is specified). |
| [isLocked()](#isLocked) | Specifies whether the link to the OLE object is locked from updates. |
| [isLocked(boolean value)](#isLocked-boolean) | Specifies whether the link to the OLE object is locked from updates. |
| [save(OutputStream stream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | Saves the data of the embedded object into a file with the specified name. |
| [setAutoUpdate(boolean value)](#setAutoUpdate-boolean) | Specifies whether the link to the OLE object is automatically updated or not in Microsoft Word. |
| [setProgId(String value)](#setProgId-java.lang.String) | Sets the ProgID of the OLE object. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String) | Sets the path and name of the source file for the linked OLE object. |
| [setSourceItem(String value)](#setSourceItem-java.lang.String) | Sets a string that is used to identify the portion of the source file that is being linked. |
### getAutoUpdate() {#getAutoUpdate}
```
public boolean getAutoUpdate()
```


Specifies whether the link to the OLE object is automatically updated or not in Microsoft Word.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to extract embedded OLE objects into files.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getClsid() {#getClsid}
```
public UUID getClsid()
```


Gets the CLSID of the OLE object.

 **Examples:** 

Shows how to access an OLE control embedded in a document and its child controls.

```

 Document doc = new Document(getMyDir() + "OLE ActiveX controls.docm");

 // Shapes store and display OLE objects in the document's body.
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 Assert.assertEquals("6e182020-f460-11ce-9bcd-00aa00608e01", shape.getOleFormat().getClsid().toString());

 Forms2OleControl oleControl = (Forms2OleControl) shape.getOleFormat().getOleControl();

 // Some OLE controls may contain child controls, such as the one in this document with three options buttons.
 Forms2OleControlCollection oleControlCollection = oleControl.getChildNodes();

 Assert.assertEquals(3, oleControlCollection.getCount());

 Assert.assertEquals("C#", oleControlCollection.get(0).getCaption());
 Assert.assertEquals("1", oleControlCollection.get(0).getValue());

 Assert.assertEquals("Visual Basic", oleControlCollection.get(1).getCaption());
 Assert.assertEquals("0", oleControlCollection.get(1).getValue());

 Assert.assertEquals("Delphi", oleControlCollection.get(2).getCaption());
 Assert.assertEquals("0", oleControlCollection.get(2).getValue());
 
```

**Returns:**
java.util.UUID - The CLSID of the OLE object.
### getIconCaption() {#getIconCaption}
```
public String getIconCaption()
```


Gets icon caption of OLE object.

In case of OLE object is not embedded as icon or caption couldn't be retrieved returns empty string.

 **Examples:** 

Shows how to insert linked and unlinked OLE objects.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Embed a Microsoft Visio drawing into the document as an OLE object.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", false, false, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Insert a link to the file in the local file system and display it as an icon.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", true, true, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Inserting OLE objects creates shapes that store these objects.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(2, shapeList.size());
 Assert.assertEquals(2, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.OLE_OBJECT));

 // If a shape contains an OLE object, it will have a valid "OleFormat" property,
 // which we can use to verify some aspects of the shape.
 OleFormat oleFormat = shapeList.get(0).getOleFormat();

 Assert.assertEquals(false, oleFormat.isLink());
 Assert.assertEquals(false, oleFormat.getOleIcon());

 oleFormat = shapeList.get(1).getOleFormat();

 Assert.assertEquals(true, oleFormat.isLink());
 Assert.assertEquals(true, oleFormat.getOleIcon());

 Assert.assertTrue(oleFormat.getSourceFullName().endsWith("Images" + File.separator + "Microsoft Visio drawing.vsd"));
 Assert.assertEquals("", oleFormat.getSourceItem());

 Assert.assertEquals("Microsoft Visio drawing.vsd", oleFormat.getIconCaption());

 doc.save(getArtifactsDir() + "Shape.OleLinks.docx");

 // If the object contains OLE data, we can access it using a stream.
 byte[] oleEntryBytes = oleFormat.getOleEntry("CompObj");
 Assert.assertEquals(76, oleEntryBytes.length);
 
```

**Returns:**
java.lang.String - Icon caption of OLE object.
### getOleControl() {#getOleControl}
```
public OleControl getOleControl()
```


Gets [getOleControl()](../../com.aspose.words/oleformat/\#getOleControl) objects if this OLE object is an ActiveX control. Otherwise this property is null.

 **Examples:** 

Shows how to verify the properties of an ActiveX control.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Returns:**
[OleControl](../../com.aspose.words/olecontrol/) - [getOleControl()](../../com.aspose.words/oleformat/\#getOleControl) objects if this OLE object is an ActiveX control.
### getOleEntry(String oleEntryName) {#getOleEntry-java.lang.String}
```
public byte[] getOleEntry(String oleEntryName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| oleEntryName | java.lang.String |  |

**Returns:**
byte[]
### getOleIcon() {#getOleIcon}
```
public boolean getOleIcon()
```


Gets the draw aspect of the OLE object. When  true , the OLE object is displayed as an icon. When  false , the OLE object is displayed as content.

 **Remarks:** 

Aspose.Words does not allow to set this property to avoid confusion. If you were able to change the draw aspect in Aspose.Words, Microsoft Word would still display the OLE object in its original draw aspect until you edit or update the OLE object in Microsoft Word.

 **Examples:** 

Shows how to insert linked and unlinked OLE objects.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Embed a Microsoft Visio drawing into the document as an OLE object.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", false, false, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Insert a link to the file in the local file system and display it as an icon.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", true, true, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Inserting OLE objects creates shapes that store these objects.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(2, shapeList.size());
 Assert.assertEquals(2, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.OLE_OBJECT));

 // If a shape contains an OLE object, it will have a valid "OleFormat" property,
 // which we can use to verify some aspects of the shape.
 OleFormat oleFormat = shapeList.get(0).getOleFormat();

 Assert.assertEquals(false, oleFormat.isLink());
 Assert.assertEquals(false, oleFormat.getOleIcon());

 oleFormat = shapeList.get(1).getOleFormat();

 Assert.assertEquals(true, oleFormat.isLink());
 Assert.assertEquals(true, oleFormat.getOleIcon());

 Assert.assertTrue(oleFormat.getSourceFullName().endsWith("Images" + File.separator + "Microsoft Visio drawing.vsd"));
 Assert.assertEquals("", oleFormat.getSourceItem());

 Assert.assertEquals("Microsoft Visio drawing.vsd", oleFormat.getIconCaption());

 doc.save(getArtifactsDir() + "Shape.OleLinks.docx");

 // If the object contains OLE data, we can access it using a stream.
 byte[] oleEntryBytes = oleFormat.getOleEntry("CompObj");
 Assert.assertEquals(76, oleEntryBytes.length);
 
```

**Returns:**
boolean - The draw aspect of the OLE object.
### getOlePackage() {#getOlePackage}
```
public OlePackage getOlePackage()
```


Provide access to [OlePackage](../../com.aspose.words/olepackage/) if OLE object is an OLE Package. Returns  null  otherwise.

 **Remarks:** 

OLE Package is a legacy technology that allows to wrap any file format not present in the OLE registry of a Windows system into a generic package allowing to embed almost anything into a document. See [OlePackage](../../com.aspose.words/olepackage/) type for more info.

 **Examples:** 

Shows how insert an OLE object into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // OLE objects allow us to open other files in the local file system using another installed application
 // in our operating system by double-clicking on the shape that contains the OLE object in the document body.
 // In this case, our external file will be a ZIP archive.
 byte[] zipFileBytes = DocumentHelper.getBytesFromStream(new FileInputStream(getDatabaseDir() + "cat001.zip"));

 InputStream stream = new ByteArrayInputStream(zipFileBytes);
 InputStream representingImage = new FileInputStream(getImageDir() + "Logo.jpg");
 try {
     Shape shape = builder.insertOleObject(stream, "Package", true, representingImage);

     OlePackage setOlePackage = shape.getOleFormat().getOlePackage();
     setOlePackage.setFileName("Package file name.zip");
     setOlePackage.setDisplayName("Package display name.zip");

     doc.save(getArtifactsDir() + "Shape.InsertOlePackage.docx");
 } finally {
     if (stream != null) {
         stream.close();
     }
 }
 
```

**Returns:**
[OlePackage](../../com.aspose.words/olepackage/) - The corresponding [OlePackage](../../com.aspose.words/olepackage/) value.
### getProgId() {#getProgId}
```
public String getProgId()
```


Gets the ProgID of the OLE object.

 **Remarks:** 

The ProgID property is not always present in Microsoft Word documents and cannot be relied upon.

Cannot be  null .

The default value is an empty string.

 **Examples:** 

Shows how to extract embedded OLE objects into files.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```

**Returns:**
java.lang.String - The ProgID of the OLE object.
### getRawData() {#getRawData}
```
public byte[] getRawData()
```


Gets OLE object raw data.

 **Examples:** 

Shows how to access the raw data of an embedded OLE object.

```

 Document doc = new Document(getMyDir() + "OLE objects.docx");

 for (Node shape : (Iterable) doc.getChildNodes(NodeType.SHAPE, true)) {
     OleFormat oleFormat = ((Shape) shape).getOleFormat();
     if (oleFormat != null) {
         byte[] oleRawData = oleFormat.getRawData();

         Assert.assertEquals(24576, oleRawData.length);
     }
 }
 
```

**Returns:**
byte[]
### getSourceFullName() {#getSourceFullName}
```
public String getSourceFullName()
```


Gets the path and name of the source file for the linked OLE object.

 **Remarks:** 

The default value is an empty string.

If [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) is not an empty string, the OLE object is linked.

 **Examples:** 

Shows how to insert linked and unlinked OLE objects.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Embed a Microsoft Visio drawing into the document as an OLE object.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", false, false, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Insert a link to the file in the local file system and display it as an icon.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", true, true, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Inserting OLE objects creates shapes that store these objects.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(2, shapeList.size());
 Assert.assertEquals(2, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.OLE_OBJECT));

 // If a shape contains an OLE object, it will have a valid "OleFormat" property,
 // which we can use to verify some aspects of the shape.
 OleFormat oleFormat = shapeList.get(0).getOleFormat();

 Assert.assertEquals(false, oleFormat.isLink());
 Assert.assertEquals(false, oleFormat.getOleIcon());

 oleFormat = shapeList.get(1).getOleFormat();

 Assert.assertEquals(true, oleFormat.isLink());
 Assert.assertEquals(true, oleFormat.getOleIcon());

 Assert.assertTrue(oleFormat.getSourceFullName().endsWith("Images" + File.separator + "Microsoft Visio drawing.vsd"));
 Assert.assertEquals("", oleFormat.getSourceItem());

 Assert.assertEquals("Microsoft Visio drawing.vsd", oleFormat.getIconCaption());

 doc.save(getArtifactsDir() + "Shape.OleLinks.docx");

 // If the object contains OLE data, we can access it using a stream.
 byte[] oleEntryBytes = oleFormat.getOleEntry("CompObj");
 Assert.assertEquals(76, oleEntryBytes.length);
 
```

**Returns:**
java.lang.String - The path and name of the source file for the linked OLE object.
### getSourceItem() {#getSourceItem}
```
public String getSourceItem()
```


Gets a string that is used to identify the portion of the source file that is being linked.

 **Remarks:** 

The default value is an empty string.

For example, if the source file is a Microsoft Excel workbook, the [getSourceItem()](../../com.aspose.words/oleformat/\#getSourceItem) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceItem-java.lang.String) property might return "Workbook1!R3C1:R4C2" if the OLE object contains only a few cells from the worksheet.

 **Examples:** 

Shows how to insert linked and unlinked OLE objects.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Embed a Microsoft Visio drawing into the document as an OLE object.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", false, false, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Insert a link to the file in the local file system and display it as an icon.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", true, true, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Inserting OLE objects creates shapes that store these objects.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(2, shapeList.size());
 Assert.assertEquals(2, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.OLE_OBJECT));

 // If a shape contains an OLE object, it will have a valid "OleFormat" property,
 // which we can use to verify some aspects of the shape.
 OleFormat oleFormat = shapeList.get(0).getOleFormat();

 Assert.assertEquals(false, oleFormat.isLink());
 Assert.assertEquals(false, oleFormat.getOleIcon());

 oleFormat = shapeList.get(1).getOleFormat();

 Assert.assertEquals(true, oleFormat.isLink());
 Assert.assertEquals(true, oleFormat.getOleIcon());

 Assert.assertTrue(oleFormat.getSourceFullName().endsWith("Images" + File.separator + "Microsoft Visio drawing.vsd"));
 Assert.assertEquals("", oleFormat.getSourceItem());

 Assert.assertEquals("Microsoft Visio drawing.vsd", oleFormat.getIconCaption());

 doc.save(getArtifactsDir() + "Shape.OleLinks.docx");

 // If the object contains OLE data, we can access it using a stream.
 byte[] oleEntryBytes = oleFormat.getOleEntry("CompObj");
 Assert.assertEquals(76, oleEntryBytes.length);
 
```

**Returns:**
java.lang.String - A string that is used to identify the portion of the source file that is being linked.
### getSuggestedExtension() {#getSuggestedExtension}
```
public String getSuggestedExtension()
```


Gets the file extension suggested for the current embedded object if you want to save it into a file.

 **Examples:** 

Shows how to extract embedded OLE objects into files.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```

**Returns:**
java.lang.String - The file extension suggested for the current embedded object if you want to save it into a file.
### getSuggestedFileName() {#getSuggestedFileName}
```
public String getSuggestedFileName()
```


Gets the file name suggested for the current embedded object if you want to save it into a file.

 **Examples:** 

Shows how to get an OLE object's suggested file name.

```

 Document doc = new Document(getMyDir() + "OLE shape.rtf");

 Shape oleShape = (Shape) doc.getFirstSection().getBody().getChild(NodeType.SHAPE, 0, true);

 // OLE objects can provide a suggested filename and extension,
 // which we can use when saving the object's contents into a file in the local file system.
 String suggestedFileName = oleShape.getOleFormat().getSuggestedFileName();

 Assert.assertEquals("CSV.csv", suggestedFileName);

 OutputStream fileStream = new FileOutputStream(getArtifactsDir() + suggestedFileName);
 try {
     oleShape.getOleFormat().save(fileStream);
 } finally {
     if (fileStream != null) fileStream.close();
 }
 
```

**Returns:**
java.lang.String - The file name suggested for the current embedded object if you want to save it into a file.
### isLink() {#isLink}
```
public boolean isLink()
```


Returns  true  if the OLE object is linked (when [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) is specified).

 **Examples:** 

Shows how to insert linked and unlinked OLE objects.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Embed a Microsoft Visio drawing into the document as an OLE object.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", false, false, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Insert a link to the file in the local file system and display it as an icon.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", true, true, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Inserting OLE objects creates shapes that store these objects.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(2, shapeList.size());
 Assert.assertEquals(2, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.OLE_OBJECT));

 // If a shape contains an OLE object, it will have a valid "OleFormat" property,
 // which we can use to verify some aspects of the shape.
 OleFormat oleFormat = shapeList.get(0).getOleFormat();

 Assert.assertEquals(false, oleFormat.isLink());
 Assert.assertEquals(false, oleFormat.getOleIcon());

 oleFormat = shapeList.get(1).getOleFormat();

 Assert.assertEquals(true, oleFormat.isLink());
 Assert.assertEquals(true, oleFormat.getOleIcon());

 Assert.assertTrue(oleFormat.getSourceFullName().endsWith("Images" + File.separator + "Microsoft Visio drawing.vsd"));
 Assert.assertEquals("", oleFormat.getSourceItem());

 Assert.assertEquals("Microsoft Visio drawing.vsd", oleFormat.getIconCaption());

 doc.save(getArtifactsDir() + "Shape.OleLinks.docx");

 // If the object contains OLE data, we can access it using a stream.
 byte[] oleEntryBytes = oleFormat.getOleEntry("CompObj");
 Assert.assertEquals(76, oleEntryBytes.length);
 
```

**Returns:**
boolean -  true  if the OLE object is linked (when [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) is specified).
### isLocked() {#isLocked}
```
public boolean isLocked()
```


Specifies whether the link to the OLE object is locked from updates.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to extract embedded OLE objects into files.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Specifies whether the link to the OLE object is locked from updates.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to extract embedded OLE objects into files.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### save(OutputStream stream) {#save-java.io.OutputStream}
```
public void save(OutputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


Saves the data of the embedded object into a file with the specified name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Name of the file to save the OLE object data. |

### setAutoUpdate(boolean value) {#setAutoUpdate-boolean}
```
public void setAutoUpdate(boolean value)
```


Specifies whether the link to the OLE object is automatically updated or not in Microsoft Word.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to extract embedded OLE objects into files.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setProgId(String value) {#setProgId-java.lang.String}
```
public void setProgId(String value)
```


Sets the ProgID of the OLE object.

 **Remarks:** 

The ProgID property is not always present in Microsoft Word documents and cannot be relied upon.

Cannot be  null .

The default value is an empty string.

 **Examples:** 

Shows how to extract embedded OLE objects into files.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The ProgID of the OLE object. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String}
```
public void setSourceFullName(String value)
```


Sets the path and name of the source file for the linked OLE object.

 **Remarks:** 

The default value is an empty string.

If [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) is not an empty string, the OLE object is linked.

 **Examples:** 

Shows how to insert linked and unlinked OLE objects.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Embed a Microsoft Visio drawing into the document as an OLE object.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", false, false, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Insert a link to the file in the local file system and display it as an icon.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", true, true, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Inserting OLE objects creates shapes that store these objects.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(2, shapeList.size());
 Assert.assertEquals(2, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.OLE_OBJECT));

 // If a shape contains an OLE object, it will have a valid "OleFormat" property,
 // which we can use to verify some aspects of the shape.
 OleFormat oleFormat = shapeList.get(0).getOleFormat();

 Assert.assertEquals(false, oleFormat.isLink());
 Assert.assertEquals(false, oleFormat.getOleIcon());

 oleFormat = shapeList.get(1).getOleFormat();

 Assert.assertEquals(true, oleFormat.isLink());
 Assert.assertEquals(true, oleFormat.getOleIcon());

 Assert.assertTrue(oleFormat.getSourceFullName().endsWith("Images" + File.separator + "Microsoft Visio drawing.vsd"));
 Assert.assertEquals("", oleFormat.getSourceItem());

 Assert.assertEquals("Microsoft Visio drawing.vsd", oleFormat.getIconCaption());

 doc.save(getArtifactsDir() + "Shape.OleLinks.docx");

 // If the object contains OLE data, we can access it using a stream.
 byte[] oleEntryBytes = oleFormat.getOleEntry("CompObj");
 Assert.assertEquals(76, oleEntryBytes.length);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The path and name of the source file for the linked OLE object. |

### setSourceItem(String value) {#setSourceItem-java.lang.String}
```
public void setSourceItem(String value)
```


Sets a string that is used to identify the portion of the source file that is being linked.

 **Remarks:** 

The default value is an empty string.

For example, if the source file is a Microsoft Excel workbook, the [getSourceItem()](../../com.aspose.words/oleformat/\#getSourceItem) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceItem-java.lang.String) property might return "Workbook1!R3C1:R4C2" if the OLE object contains only a few cells from the worksheet.

 **Examples:** 

Shows how to insert linked and unlinked OLE objects.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Embed a Microsoft Visio drawing into the document as an OLE object.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", false, false, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Insert a link to the file in the local file system and display it as an icon.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", true, true, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Inserting OLE objects creates shapes that store these objects.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(2, shapeList.size());
 Assert.assertEquals(2, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.OLE_OBJECT));

 // If a shape contains an OLE object, it will have a valid "OleFormat" property,
 // which we can use to verify some aspects of the shape.
 OleFormat oleFormat = shapeList.get(0).getOleFormat();

 Assert.assertEquals(false, oleFormat.isLink());
 Assert.assertEquals(false, oleFormat.getOleIcon());

 oleFormat = shapeList.get(1).getOleFormat();

 Assert.assertEquals(true, oleFormat.isLink());
 Assert.assertEquals(true, oleFormat.getOleIcon());

 Assert.assertTrue(oleFormat.getSourceFullName().endsWith("Images" + File.separator + "Microsoft Visio drawing.vsd"));
 Assert.assertEquals("", oleFormat.getSourceItem());

 Assert.assertEquals("Microsoft Visio drawing.vsd", oleFormat.getIconCaption());

 doc.save(getArtifactsDir() + "Shape.OleLinks.docx");

 // If the object contains OLE data, we can access it using a stream.
 byte[] oleEntryBytes = oleFormat.getOleEntry("CompObj");
 Assert.assertEquals(76, oleEntryBytes.length);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A string that is used to identify the portion of the source file that is being linked. |

