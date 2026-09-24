---
title: "OleFormat"
linktitle: "OleFormat"
second_title: "Aspose.Words Java için"
description: "Java'da bir OLE nesnesi veya ActiveX kontrolünün verilerine erişim sağlar."
type: docs
weight: 501
url: /tr/java/com.aspose.words/oleformat/
---

**Inheritance:**
java.lang.Object
```
public class OleFormat
```

Bir OLE nesnesi veya ActiveX denetiminin verilerine erişim sağlar.

Daha fazla bilgi edinmek için, [ Working with Ole Objects ][Working with Ole Objects] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

[Shape.getOleFormat()](../../com.aspose.words/shape/\#getOleFormat) özelliğini kullanarak bir OLE nesnesinin verilerine erişin. [OleFormat](../../com.aspose.words/oleformat/) sınıfının örneklerini doğrudan oluşturmazsınız.

 **Examples:** 

Gömülü OLE nesnelerinin dosyalara nasıl çıkarılacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAutoUpdate()](#getAutoUpdate) | Microsoft Word'de OLE nesnesine olan bağlantının otomatik olarak güncellenip güncellenmeyeceğini belirtir. |
| [getClsid()](#getClsid) | OLE nesnesinin CLSID'sini alır. |
| [getIconCaption()](#getIconCaption) | OLE nesnesinin simge başlığını alır. |
| [getOleControl()](#getOleControl) | Bu OLE nesnesi bir ActiveX denetimi ise [getOleControl()](../../com.aspose.words/oleformat/\#getOleControl) nesnelerini alır. |
| [getOleEntry(String oleEntryName)](#getOleEntry-java.lang.String) |  |
| [getOleIcon()](#getOleIcon) | OLE nesnesinin çizim yönünü alır. |
| [getOlePackage()](#getOlePackage) | OLE nesnesi bir OLE Paketi ise [OlePackage](../../com.aspose.words/olepackage/) erişimi sağlar. |
| [getProgId()](#getProgId) | OLE nesnesinin ProgID'sini alır. |
| [getRawData()](#getRawData) | OLE nesnesinin ham verisini alır. |
| [getSourceFullName()](#getSourceFullName) | Bağlantılı OLE nesnesi için kaynak dosyanın yolunu ve adını alır. |
| [getSourceItem()](#getSourceItem) | Bağlantı verilen kaynak dosyanın bölümünü tanımlamak için kullanılan bir dizeyi alır. |
| [getSuggestedExtension()](#getSuggestedExtension) | Mevcut gömülü nesneyi bir dosyaya kaydetmek isterseniz önerilen dosya uzantısını alır. |
| [getSuggestedFileName()](#getSuggestedFileName) | Mevcut gömülü nesneyi bir dosyaya kaydetmek isterseniz önerilen dosya adını alır. |
| [isLink()](#isLink) | OLE nesnesi bağlantılıysa ( [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) belirtildiğinde) true döndürür. |
| [isLocked()](#isLocked) | OLE nesnesine olan bağlantının güncellemelerden kilitli olup olmadığını belirtir. |
| [isLocked(boolean value)](#isLocked-boolean) | OLE nesnesine olan bağlantının güncellemelerden kilitli olup olmadığını belirtir. |
| [save(OutputStream stream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | Gömülü nesnenin verilerini belirtilen adla bir dosyaya kaydeder. |
| [setAutoUpdate(boolean value)](#setAutoUpdate-boolean) | Microsoft Word'de OLE nesnesine olan bağlantının otomatik olarak güncellenip güncellenmeyeceğini belirtir. |
| [setProgId(String value)](#setProgId-java.lang.String) | OLE nesnesinin ProgID'sini ayarlar. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String) | Bağlantılı OLE nesnesi için kaynak dosyanın yolunu ve adını ayarlar. |
| [setSourceItem(String value)](#setSourceItem-java.lang.String) | Bağlantı verilen kaynak dosyanın bölümünü tanımlamak için kullanılan bir dizeyi ayarlar. |
### getAutoUpdate() {#getAutoUpdate}
```
public boolean getAutoUpdate()
```


Microsoft Word'de OLE nesnesine olan bağlantının otomatik olarak güncellenip güncellenmeyeceğini belirtir.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Gömülü OLE nesnelerinin dosyalara nasıl çıkarılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getClsid() {#getClsid}
```
public UUID getClsid()
```


OLE nesnesinin CLSID'sini alır.

 **Examples:** 

Bir belgede gömülü OLE denetimine ve onun alt denetimlerine nasıl erişileceğini gösterir.

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
java.util.UUID - OLE nesnesinin CLSID'si.
### getIconCaption() {#getIconCaption}
```
public String getIconCaption()
```


OLE nesnesinin simge başlığını alır.

OLE nesnesinin bir simgesi yoksa veya başlık alınamıyorsa, boş bir dize döndürür.

 **Examples:** 

Bağlantılı ve bağlantısız OLE nesnelerinin nasıl ekleneceğini gösterir.

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
java.lang.String - OLE nesnesinin simge başlığı.
### getOleControl() {#getOleControl}
```
public OleControl getOleControl()
```


Bu OLE nesnesi bir ActiveX denetimi ise [getOleControl()](../../com.aspose.words/oleformat/\#getOleControl) nesnelerini alır. Aksi takdirde bu özellik null'dur.

 **Examples:** 

ActiveX kontrolünün özelliklerinin nasıl doğrulanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| oleEntryName | java.lang.String |  |

**Returns:**
byte[]
### getOleIcon() {#getOleIcon}
```
public boolean getOleIcon()
```


OLE nesnesinin çizim görünümünü alır. true olduğunda, OLE nesnesi bir simge olarak görüntülenir. false olduğunda, OLE nesnesi içerik olarak görüntülenir.

 **Remarks:** 

Aspose.Words bu özelliğin ayarlanmasına izin vermez, karışıklığı önlemek için. Aspose.Words içinde çizim görünümünü değiştirebilseydiniz, Microsoft Word OLE nesnesini hâlâ orijinal çizim görünümünde gösterirdi, OLE nesnesini Microsoft Word'de düzenleyene veya güncelleyinceye kadar.

 **Examples:** 

Bağlantılı ve bağlantısız OLE nesnelerinin nasıl ekleneceğini gösterir.

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
boolean - OLE nesnesinin çizim görünümü.
### getOlePackage() {#getOlePackage}
```
public OlePackage getOlePackage()
```


OLE nesnesi bir OLE Paketi ise [OlePackage](../../com.aspose.words/olepackage/) erişimini sağlar. Aksi takdirde null döndürür.

 **Remarks:** 

OLE Paketi, Windows sisteminin OLE kayıt defterinde bulunmayan herhangi bir dosya biçimini genel bir paket içine sarmalayarak neredeyse her şeyi bir belgeye gömmeyi sağlayan eski bir teknolojidir. Daha fazla bilgi için [OlePackage](../../com.aspose.words/olepackage/) tipine bakın.

 **Examples:** 

Bir OLE nesnesinin belgeye nasıl ekleneceğini gösterir.

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


OLE nesnesinin ProgID'sini alır.

 **Remarks:** 

ProgID özelliği Microsoft Word belgelerinde her zaman bulunmaz ve güvenilir değildir.

null olamaz.

Varsayılan değer boş bir dizedir.

 **Examples:** 

Gömülü OLE nesnelerinin dosyalara nasıl çıkarılacağını gösterir.

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
java.lang.String - OLE nesnesinin ProgID'si.
### getRawData() {#getRawData}
```
public byte[] getRawData()
```


OLE nesnesinin ham verisini alır.

 **Examples:** 

Gömülü bir OLE nesnesinin ham verilerine nasıl erişileceğini gösterir.

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


Bağlantılı OLE nesnesi için kaynak dosyanın yolunu ve adını alır.

 **Remarks:** 

Varsayılan değer boş bir dizedir.

Eğer [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) boş bir dize değilse, OLE nesnesi bağlantılıdır.

 **Examples:** 

Bağlantılı ve bağlantısız OLE nesnelerinin nasıl ekleneceğini gösterir.

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
java.lang.String - Bağlantılı OLE nesnesi için kaynak dosyanın yolu ve adı.
### getSourceItem() {#getSourceItem}
```
public String getSourceItem()
```


Bağlantı verilen kaynak dosyanın bölümünü tanımlamak için kullanılan bir dizeyi alır.

 **Remarks:** 

Varsayılan değer boş bir dizedir.

Örneğin, kaynak dosya bir Microsoft Excel çalışma kitabı ise, [getSourceItem()](../../com.aspose.words/oleformat/\#getSourceItem) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceItem-java.lang.String) özelliği, OLE nesnesi yalnızca çalışma sayfasından birkaç hücre içeriyorsa "Workbook1!R3C1:R4C2" döndürebilir.

 **Examples:** 

Bağlantılı ve bağlantısız OLE nesnelerinin nasıl ekleneceğini gösterir.

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
java.lang.String - Bağlantılı olan kaynak dosyanın bölümünü tanımlamak için kullanılan bir dize.
### getSuggestedExtension() {#getSuggestedExtension}
```
public String getSuggestedExtension()
```


Mevcut gömülü nesneyi bir dosyaya kaydetmek isterseniz önerilen dosya uzantısını alır.

 **Examples:** 

Gömülü OLE nesnelerinin dosyalara nasıl çıkarılacağını gösterir.

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
java.lang.String - Mevcut gömülü nesneyi bir dosyaya kaydetmek istediğinizde önerilen dosya uzantısı.
### getSuggestedFileName() {#getSuggestedFileName}
```
public String getSuggestedFileName()
```


Mevcut gömülü nesneyi bir dosyaya kaydetmek isterseniz önerilen dosya adını alır.

 **Examples:** 

Bir OLE nesnesinin önerilen dosya adının nasıl alınacağını gösterir.

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
java.lang.String - Mevcut gömülü nesneyi bir dosyaya kaydetmek istediğinizde önerilen dosya adı.
### isLink() {#isLink}
```
public boolean isLink()
```


OLE nesnesi bağlantılıysa ( [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) belirtildiğinde) true döndürür.

 **Examples:** 

Bağlantılı ve bağlantısız OLE nesnelerinin nasıl ekleneceğini gösterir.

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
boolean - OLE nesnesi bağlantılıysa true ( [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) belirtildiğinde).
### isLocked() {#isLocked}
```
public boolean isLocked()
```


OLE nesnesine olan bağlantının güncellemelerden kilitli olup olmadığını belirtir.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Gömülü OLE nesnelerinin dosyalara nasıl çıkarılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


OLE nesnesine olan bağlantının güncellemelerden kilitli olup olmadığını belirtir.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Gömülü OLE nesnelerinin dosyalara nasıl çıkarılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### save(OutputStream stream) {#save-java.io.OutputStream}
```
public void save(OutputStream stream)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


Gömülü nesnenin verilerini belirtilen adla bir dosyaya kaydeder.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | OLE nesnesi verilerini kaydetmek için dosyanın adı. |

### setAutoUpdate(boolean value) {#setAutoUpdate-boolean}
```
public void setAutoUpdate(boolean value)
```


Microsoft Word'de OLE nesnesine olan bağlantının otomatik olarak güncellenip güncellenmeyeceğini belirtir.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Gömülü OLE nesnelerinin dosyalara nasıl çıkarılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setProgId(String value) {#setProgId-java.lang.String}
```
public void setProgId(String value)
```


OLE nesnesinin ProgID'sini ayarlar.

 **Remarks:** 

ProgID özelliği Microsoft Word belgelerinde her zaman bulunmaz ve güvenilir değildir.

null olamaz.

Varsayılan değer boş bir dizedir.

 **Examples:** 

Gömülü OLE nesnelerinin dosyalara nasıl çıkarılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | OLE nesnesinin ProgID'si. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String}
```
public void setSourceFullName(String value)
```


Bağlantılı OLE nesnesi için kaynak dosyanın yolunu ve adını ayarlar.

 **Remarks:** 

Varsayılan değer boş bir dizedir.

Eğer [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) boş bir dize değilse, OLE nesnesi bağlantılıdır.

 **Examples:** 

Bağlantılı ve bağlantısız OLE nesnelerinin nasıl ekleneceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Bağlantılı OLE nesnesi için kaynak dosyanın yolu ve adı. |

### setSourceItem(String value) {#setSourceItem-java.lang.String}
```
public void setSourceItem(String value)
```


Bağlantı verilen kaynak dosyanın bölümünü tanımlamak için kullanılan bir dizeyi ayarlar.

 **Remarks:** 

Varsayılan değer boş bir dizedir.

Örneğin, kaynak dosya bir Microsoft Excel çalışma kitabı ise, [getSourceItem()](../../com.aspose.words/oleformat/\#getSourceItem) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceItem-java.lang.String) özelliği, OLE nesnesi yalnızca çalışma sayfasından birkaç hücre içeriyorsa "Workbook1!R3C1:R4C2" döndürebilir.

 **Examples:** 

Bağlantılı ve bağlantısız OLE nesnelerinin nasıl ekleneceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Bağlantılı olan kaynak dosyanın bölümünü tanımlamak için kullanılan bir dize. |

