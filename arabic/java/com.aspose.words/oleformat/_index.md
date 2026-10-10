---
title: "OleFormat"
linktitle: "OleFormat"
second_title: "Aspose.Words لـ Java"
description: "يوفر الوصول إلى بيانات كائن OLE أو عنصر تحكم ActiveX في Java."
type: docs
weight: 501
url: /ar/java/com.aspose.words/oleformat/
---

**Inheritance:**
java.lang.Object
```
public class OleFormat
```

يوفر الوصول إلى بيانات كائن OLE أو عنصر تحكم ActiveX.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Ole Objects ][Working with Ole Objects].

 **Remarks:** 

استخدم الخاصية [Shape.getOleFormat()](../../com.aspose.words/shape/\#getOleFormat) للوصول إلى بيانات كائن OLE. لا تقوم بإنشاء مثيلات من الفئة [OleFormat](../../com.aspose.words/oleformat/) مباشرة.

 **Examples:** 

يعرض كيفية استخراج كائنات OLE المضمنة إلى ملفات.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAutoUpdate()](#getAutoUpdate) | يحدد ما إذا كان الارتباط إلى كائن OLE يتم تحديثه تلقائيًا أم لا في Microsoft Word. |
| [getClsid()](#getClsid) | يحصل على CLSID لكائن OLE. |
| [getIconCaption()](#getIconCaption) | يحصل على تسمية أيقونة كائن OLE. |
| [getOleControl()](#getOleControl) | يحصل على كائنات [getOleControl()](../../com.aspose.words/oleformat/\#getOleControl) إذا كان هذا الكائن OLE عنصر تحكم ActiveX. |
| [getOleEntry(String oleEntryName)](#getOleEntry-java.lang.String) |  |
| [getOleIcon()](#getOleIcon) | يحصل على جانب الرسم لكائن OLE. |
| [getOlePackage()](#getOlePackage) | يوفر الوصول إلى [OlePackage](../../com.aspose.words/olepackage/) إذا كان كائن OLE حزمة OLE. |
| [getProgId()](#getProgId) | يحصل على ProgID لكائن OLE. |
| [getRawData()](#getRawData) | يحصل على البيانات الخام لكائن OLE. |
| [getSourceFullName()](#getSourceFullName) | يحصل على المسار والاسم لملف المصدر لكائن OLE المرتبط. |
| [getSourceItem()](#getSourceItem) | يحصل على سلسلة تُستخدم لتحديد الجزء من ملف المصدر الذي يتم ربطه. |
| [getSuggestedExtension()](#getSuggestedExtension) | يحصل على امتداد الملف المقترح للكائن المضمن الحالي إذا كنت تريد حفظه في ملف. |
| [getSuggestedFileName()](#getSuggestedFileName) | يحصل على اسم الملف المقترح للكائن المضمن الحالي إذا كنت تريد حفظه في ملف. |
| [isLink()](#isLink) | يرجع  true  إذا كان كائن OLE مرتبطًا (عند تحديد [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String)). |
| [isLocked()](#isLocked) | يحدد ما إذا كان الارتباط إلى كائن OLE مقفلًا من التحديثات. |
| [isLocked(boolean value)](#isLocked-boolean) | يحدد ما إذا كان الارتباط إلى كائن OLE مقفلًا من التحديثات. |
| [save(OutputStream stream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | يحفظ بيانات الكائن المضمن في ملف بالاسم المحدد. |
| [setAutoUpdate(boolean value)](#setAutoUpdate-boolean) | يحدد ما إذا كان الارتباط إلى كائن OLE يتم تحديثه تلقائيًا أم لا في Microsoft Word. |
| [setProgId(String value)](#setProgId-java.lang.String) | يضبط ProgID لكائن OLE. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String) | يضبط المسار والاسم لملف المصدر لكائن OLE المرتبط. |
| [setSourceItem(String value)](#setSourceItem-java.lang.String) | يضبط سلسلة تُستخدم لتحديد الجزء من ملف المصدر الذي يتم ربطه. |
### getAutoUpdate() {#getAutoUpdate}
```
public boolean getAutoUpdate()
```


يحدد ما إذا كان الارتباط إلى كائن OLE يتم تحديثه تلقائيًا أم لا في Microsoft Word.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية استخراج كائنات OLE المضمنة إلى ملفات.

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
boolean - القيمة المنطقية المقابلة.
### getClsid() {#getClsid}
```
public UUID getClsid()
```


يحصل على CLSID لكائن OLE.

 **Examples:** 

يعرض كيفية الوصول إلى عنصر تحكم OLE مضمّن في مستند وعناصر التحكم التابعة له.

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
java.util.UUID - CLSID لكائن OLE.
### getIconCaption() {#getIconCaption}
```
public String getIconCaption()
```


يحصل على تسمية أيقونة كائن OLE.

في حالة عدم وجود أيقونة لكائن OLE أو عدم إمكانية استرجاع التسمية، يرجع سلسلة فارغة.

 **Examples:** 

يعرض كيفية إدراج كائنات OLE المرتبطة وغير المرتبطة.

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
java.lang.String - تسمية أيقونة كائن OLE.
### getOleControl() {#getOleControl}
```
public OleControl getOleControl()
```


يحصل على كائنات [getOleControl()](../../com.aspose.words/oleformat/\#getOleControl) إذا كان هذا الكائن OLE عنصر تحكم ActiveX. وإلا فإن هذه الخاصية تكون null.

 **Examples:** 

يوضح كيفية التحقق من خصائص عنصر ActiveX.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| oleEntryName | java.lang.String |  |

**Returns:**
byte[]
### getOleIcon() {#getOleIcon}
```
public boolean getOleIcon()
```


يحصل على مظهر الرسم لكائن OLE. عندما يكون  true , يتم عرض كائن OLE كأيقونة. عندما يكون  false , يتم عرض كائن OLE كمحتوى.

 **Remarks:** 

لا يسمح Aspose.Words بتعيين هذه الخاصية لتجنب الالتباس. إذا كنت قادرًا على تغيير مظهر الرسم في Aspose.Words، فإن Microsoft Word سيستمر في عرض كائن OLE بمظهره الأصلي حتى تقوم بتحرير أو تحديث كائن OLE في Microsoft Word.

 **Examples:** 

يعرض كيفية إدراج كائنات OLE المرتبطة وغير المرتبطة.

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
boolean - مظهر الرسم لكائن OLE.
### getOlePackage() {#getOlePackage}
```
public OlePackage getOlePackage()
```


وفر إمكانية الوصول إلى [OlePackage](../../com.aspose.words/olepackage/) إذا كان كائن OLE هو حزمة OLE. يرجع  null  خلاف ذلك.

 **Remarks:** 

حزمة OLE هي تقنية قديمة تسمح بلف أي تنسيق ملف غير موجود في سجل OLE لنظام Windows داخل حزمة عامة تسمح بدمج تقريبًا أي شيء في مستند. راجع نوع [OlePackage](../../com.aspose.words/olepackage/) لمزيد من المعلومات.

 **Examples:** 

يظهر كيفية إدراج كائن OLE في مستند.

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


يحصل على ProgID لكائن OLE.

 **Remarks:** 

خاصية ProgID ليست دائمًا موجودة في مستندات Microsoft Word ولا يمكن الاعتماد عليها.

لا يمكن أن تكون  null .

القيمة الافتراضية هي سلسلة فارغة.

 **Examples:** 

يعرض كيفية استخراج كائنات OLE المضمنة إلى ملفات.

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
java.lang.String - ProgID لكائن OLE.
### getRawData() {#getRawData}
```
public byte[] getRawData()
```


يحصل على البيانات الخام لكائن OLE.

 **Examples:** 

يوضح كيفية الوصول إلى البيانات الخام لكائن OLE المضمّن.

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


يحصل على المسار والاسم لملف المصدر لكائن OLE المرتبط.

 **Remarks:** 

القيمة الافتراضية هي سلسلة فارغة.

إذا لم يكن [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) سلسلة فارغة، فإن كائن OLE مرتبط.

 **Examples:** 

يعرض كيفية إدراج كائنات OLE المرتبطة وغير المرتبطة.

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
java.lang.String - المسار والاسم لملف المصدر لكائن OLE المرتبط.
### getSourceItem() {#getSourceItem}
```
public String getSourceItem()
```


يحصل على سلسلة تُستخدم لتحديد الجزء من ملف المصدر الذي يتم ربطه.

 **Remarks:** 

القيمة الافتراضية هي سلسلة فارغة.

على سبيل المثال، إذا كان ملف المصدر هو مصنف Microsoft Excel، قد تُعيد الخاصية [getSourceItem()](../../com.aspose.words/oleformat/\#getSourceItem) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceItem-java.lang.String) القيمة "Workbook1!R3C1:R4C2" إذا كان كائن OLE يحتوي على عدد قليل فقط من الخلايا من ورقة العمل.

 **Examples:** 

يعرض كيفية إدراج كائنات OLE المرتبطة وغير المرتبطة.

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
java.lang.String - سلسلة تُستخدم لتحديد الجزء من ملف المصدر الذي يتم ربطه.
### getSuggestedExtension() {#getSuggestedExtension}
```
public String getSuggestedExtension()
```


يحصل على امتداد الملف المقترح للكائن المضمن الحالي إذا كنت تريد حفظه في ملف.

 **Examples:** 

يعرض كيفية استخراج كائنات OLE المضمنة إلى ملفات.

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
java.lang.String - امتداد الملف المقترح للكائن المضمّن الحالي إذا أردت حفظه في ملف.
### getSuggestedFileName() {#getSuggestedFileName}
```
public String getSuggestedFileName()
```


يحصل على اسم الملف المقترح للكائن المضمن الحالي إذا كنت تريد حفظه في ملف.

 **Examples:** 

يوضح كيفية الحصول على اسم الملف المقترح لكائن OLE.

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
java.lang.String - اسم الملف المقترح للكائن المضمّن الحالي إذا أردت حفظه في ملف.
### isLink() {#isLink}
```
public boolean isLink()
```


يرجع  true  إذا كان كائن OLE مرتبطًا (عند تحديد [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String)).

 **Examples:** 

يعرض كيفية إدراج كائنات OLE المرتبطة وغير المرتبطة.

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
boolean -  true  إذا كان كائن OLE مرتبطًا (عند تحديد [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String)).
### isLocked() {#isLocked}
```
public boolean isLocked()
```


يحدد ما إذا كان الارتباط إلى كائن OLE مقفلًا من التحديثات.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية استخراج كائنات OLE المضمنة إلى ملفات.

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
boolean - القيمة المنطقية المقابلة.
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


يحدد ما إذا كان الارتباط إلى كائن OLE مقفلًا من التحديثات.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية استخراج كائنات OLE المضمنة إلى ملفات.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### save(OutputStream stream) {#save-java.io.OutputStream}
```
public void save(OutputStream stream)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


يحفظ بيانات الكائن المضمن في ملف بالاسم المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | اسم الملف لحفظ بيانات كائن OLE. |

### setAutoUpdate(boolean value) {#setAutoUpdate-boolean}
```
public void setAutoUpdate(boolean value)
```


يحدد ما إذا كان الارتباط إلى كائن OLE يتم تحديثه تلقائيًا أم لا في Microsoft Word.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية استخراج كائنات OLE المضمنة إلى ملفات.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setProgId(String value) {#setProgId-java.lang.String}
```
public void setProgId(String value)
```


يضبط ProgID لكائن OLE.

 **Remarks:** 

خاصية ProgID ليست دائمًا موجودة في مستندات Microsoft Word ولا يمكن الاعتماد عليها.

لا يمكن أن تكون  null .

القيمة الافتراضية هي سلسلة فارغة.

 **Examples:** 

يعرض كيفية استخراج كائنات OLE المضمنة إلى ملفات.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | ProgID لكائن OLE. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String}
```
public void setSourceFullName(String value)
```


يضبط المسار والاسم لملف المصدر لكائن OLE المرتبط.

 **Remarks:** 

القيمة الافتراضية هي سلسلة فارغة.

إذا لم يكن [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) سلسلة فارغة، فإن كائن OLE مرتبط.

 **Examples:** 

يعرض كيفية إدراج كائنات OLE المرتبطة وغير المرتبطة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | المسار والاسم لملف المصدر لكائن OLE المرتبط. |

### setSourceItem(String value) {#setSourceItem-java.lang.String}
```
public void setSourceItem(String value)
```


يضبط سلسلة تُستخدم لتحديد الجزء من ملف المصدر الذي يتم ربطه.

 **Remarks:** 

القيمة الافتراضية هي سلسلة فارغة.

على سبيل المثال، إذا كان ملف المصدر هو مصنف Microsoft Excel، قد تُعيد الخاصية [getSourceItem()](../../com.aspose.words/oleformat/\#getSourceItem) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceItem-java.lang.String) القيمة "Workbook1!R3C1:R4C2" إذا كان كائن OLE يحتوي على عدد قليل فقط من الخلايا من ورقة العمل.

 **Examples:** 

يعرض كيفية إدراج كائنات OLE المرتبطة وغير المرتبطة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | سلسلة تُستخدم لتحديد الجزء من ملف المصدر الذي يتم ربطه. |

