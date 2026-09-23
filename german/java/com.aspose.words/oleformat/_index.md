---
title: "OleFormat"
linktitle: "OleFormat"
second_title: "Aspose.Words für Java"
description: "Stellt Zugriff auf die Daten eines OLE-Objekts oder ActiveX-Steuerelements in Java bereit."
type: docs
weight: 501
url: /de/java/com.aspose.words/oleformat/
---

**Inheritance:**
java.lang.Object
```
public class OleFormat
```

Bietet Zugriff auf die Daten eines OLE‑Objekts oder ActiveX‑Steuerelements.

Um mehr zu erfahren, besuchen Sie den [ Working with Ole Objects ][Working with Ole Objects] Dokumentationsartikel.

 **Remarks:** 

Verwenden Sie die Eigenschaft [Shape.getOleFormat()](../../com.aspose.words/shape/\#getOleFormat), um auf die Daten eines OLE-Objekts zuzugreifen. Sie erstellen keine Instanzen der Klasse [OleFormat](../../com.aspose.words/oleformat/) direkt.

 **Examples:** 

Zeigt, wie eingebettete OLE-Objekte in Dateien extrahiert werden.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAutoUpdate()](#getAutoUpdate) | Gibt an, ob die Verknüpfung zum OLE-Objekt in Microsoft Word automatisch aktualisiert wird oder nicht. |
| [getClsid()](#getClsid) | Ruft die CLSID des OLE-Objekts ab. |
| [getIconCaption()](#getIconCaption) | Ruft die Symbolbeschriftung des OLE-Objekts ab. |
| [getOleControl()](#getOleControl) | Ruft [getOleControl()](../../com.aspose.words/oleformat/\#getOleControl)-Objekte ab, wenn dieses OLE-Objekt ein ActiveX-Steuerelement ist. |
| [getOleEntry(String oleEntryName)](#getOleEntry-java.lang.String) |  |
| [getOleIcon()](#getOleIcon) | Ruft den Darstellungsaspekt des OLE-Objekts ab. |
| [getOlePackage()](#getOlePackage) | Stellt Zugriff auf [OlePackage](../../com.aspose.words/olepackage/) bereit, wenn das OLE-Objekt ein OLE-Paket ist. |
| [getProgId()](#getProgId) | Ruft die ProgID des OLE-Objekts ab. |
| [getRawData()](#getRawData) | Ruft die Rohdaten des OLE-Objekts ab. |
| [getSourceFullName()](#getSourceFullName) | Ruft den Pfad und den Namen der Quelldatei für das verknüpfte OLE-Objekt ab. |
| [getSourceItem()](#getSourceItem) | Ruft eine Zeichenkette ab, die verwendet wird, um den Teil der Quelldatei zu identifizieren, der verknüpft wird. |
| [getSuggestedExtension()](#getSuggestedExtension) | Ruft die für das aktuelle eingebettete Objekt empfohlene Dateierweiterung ab, wenn Sie es in einer Datei speichern möchten. |
| [getSuggestedFileName()](#getSuggestedFileName) | Ruft den für das aktuelle eingebettete Objekt empfohlenen Dateinamen ab, wenn Sie es in einer Datei speichern möchten. |
| [isLink()](#isLink) | Gibt  true  zurück, wenn das OLE-Objekt verknüpft ist (wenn [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) angegeben ist). |
| [isLocked()](#isLocked) | Gibt an, ob die Verknüpfung zum OLE-Objekt vor Aktualisierungen gesperrt ist. |
| [isLocked(boolean value)](#isLocked-boolean) | Gibt an, ob die Verknüpfung zum OLE-Objekt vor Aktualisierungen gesperrt ist. |
| [save(OutputStream stream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | Speichert die Daten des eingebetteten Objekts in einer Datei mit dem angegebenen Namen. |
| [setAutoUpdate(boolean value)](#setAutoUpdate-boolean) | Gibt an, ob die Verknüpfung zum OLE-Objekt in Microsoft Word automatisch aktualisiert wird oder nicht. |
| [setProgId(String value)](#setProgId-java.lang.String) | Legt die ProgID des OLE-Objekts fest. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String) | Legt den Pfad und den Namen der Quelldatei für das verknüpfte OLE-Objekt fest. |
| [setSourceItem(String value)](#setSourceItem-java.lang.String) | Legt eine Zeichenkette fest, die verwendet wird, um den Teil der Quelldatei zu identifizieren, der verknüpft wird. |
### getAutoUpdate() {#getAutoUpdate}
```
public boolean getAutoUpdate()
```


Gibt an, ob die Verknüpfung zum OLE-Objekt in Microsoft Word automatisch aktualisiert wird oder nicht.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie eingebettete OLE-Objekte in Dateien extrahiert werden.

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
boolean - Der entsprechende  boolean  Wert.
### getClsid() {#getClsid}
```
public UUID getClsid()
```


Ruft die CLSID des OLE-Objekts ab.

 **Examples:** 

Zeigt, wie man auf ein in einem Dokument eingebettetes OLE-Steuerelement und dessen untergeordnete Steuerelemente zugreift.

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
java.util.UUID – Die CLSID des OLE-Objekts.
### getIconCaption() {#getIconCaption}
```
public String getIconCaption()
```


Ruft die Symbolbeschriftung des OLE-Objekts ab.

Falls das OLE-Objekt kein Symbol hat oder eine Beschriftung nicht abgerufen werden kann, gibt es eine leere Zeichenkette zurück.

 **Examples:** 

Zeigt, wie man verknüpfte und nicht verknüpfte OLE-Objekte einfügt.

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
java.lang.String – Symbolbeschriftung des OLE-Objekts.
### getOleControl() {#getOleControl}
```
public OleControl getOleControl()
```


Ruft [getOleControl()](../../com.aspose.words/oleformat/\#getOleControl)-Objekte ab, wenn dieses OLE-Objekt ein ActiveX-Steuerelement ist. Andernfalls ist diese Eigenschaft null.

 **Examples:** 

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| oleEntryName | java.lang.String |  |

**Returns:**
byte[]
### getOleIcon() {#getOleIcon}
```
public boolean getOleIcon()
```


Liest den Darstellungsaspekt des OLE-Objekts. Wenn  true , wird das OLE-Objekt als Symbol angezeigt. Wenn  false , wird das OLE-Objekt als Inhalt angezeigt.

 **Remarks:** 

Aspose.Words erlaubt das Setzen dieser Eigenschaft nicht, um Verwirrungen zu vermeiden. Wenn Sie den Darstellungsaspekt in Aspose.Words ändern könnten, würde Microsoft Word das OLE-Objekt weiterhin in seinem ursprünglichen Darstellungsaspekt anzeigen, bis Sie das OLE-Objekt in Microsoft Word bearbeiten oder aktualisieren.

 **Examples:** 

Zeigt, wie man verknüpfte und nicht verknüpfte OLE-Objekte einfügt.

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
boolean - Der Darstellungsaspekt des OLE-Objekts.
### getOlePackage() {#getOlePackage}
```
public OlePackage getOlePackage()
```


Stellt Zugriff auf [OlePackage](../../com.aspose.words/olepackage/) bereit, wenn das OLE-Objekt ein OLE-Paket ist. Gibt sonst  null  zurück.

 **Remarks:** 

OLE Package ist eine veraltete Technologie, die es ermöglicht, jedes Dateiformat, das nicht im OLE-Register eines Windows-Systems vorhanden ist, in ein generisches Paket zu verpacken, sodass fast alles in ein Dokument eingebettet werden kann. Siehe den Typ [OlePackage](../../com.aspose.words/olepackage/) für weitere Informationen.

 **Examples:** 

Zeigt, wie man ein OLE‑Objekt in ein Dokument einfügt.

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


Ruft die ProgID des OLE-Objekts ab.

 **Remarks:** 

Die ProgID‑Eigenschaft ist in Microsoft‑Word‑Dokumenten nicht immer vorhanden und kann nicht zuverlässig verwendet werden.

Darf nicht  null  sein.

Der Standardwert ist eine leere Zeichenfolge.

 **Examples:** 

Zeigt, wie eingebettete OLE-Objekte in Dateien extrahiert werden.

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
java.lang.String - Die ProgID des OLE-Objekts.
### getRawData() {#getRawData}
```
public byte[] getRawData()
```


Ruft die Rohdaten des OLE-Objekts ab.

 **Examples:** 

Zeigt, wie auf die Rohdaten eines eingebetteten OLE-Objekts zugegriffen wird.

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


Ruft den Pfad und den Namen der Quelldatei für das verknüpfte OLE-Objekt ab.

 **Remarks:** 

Der Standardwert ist eine leere Zeichenfolge.

Wenn [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) kein leerer String ist, ist das OLE-Objekt verknüpft.

 **Examples:** 

Zeigt, wie man verknüpfte und nicht verknüpfte OLE-Objekte einfügt.

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
java.lang.String - Der Pfad und Name der Quelldatei für das verknüpfte OLE-Objekt.
### getSourceItem() {#getSourceItem}
```
public String getSourceItem()
```


Ruft eine Zeichenkette ab, die verwendet wird, um den Teil der Quelldatei zu identifizieren, der verknüpft wird.

 **Remarks:** 

Der Standardwert ist eine leere Zeichenfolge.

Zum Beispiel, wenn die Quelldatei eine Microsoft‑Excel‑Arbeitsmappe ist, könnte die Eigenschaft [getSourceItem()](../../com.aspose.words/oleformat/\#getSourceItem) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceItem-java.lang.String) den Wert "Workbook1!R3C1:R4C2" zurückgeben, wenn das OLE-Objekt nur wenige Zellen aus dem Arbeitsblatt enthält.

 **Examples:** 

Zeigt, wie man verknüpfte und nicht verknüpfte OLE-Objekte einfügt.

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
java.lang.String - Ein String, der verwendet wird, um den Teil der Quelldatei zu identifizieren, der verknüpft wird.
### getSuggestedExtension() {#getSuggestedExtension}
```
public String getSuggestedExtension()
```


Ruft die für das aktuelle eingebettete Objekt empfohlene Dateierweiterung ab, wenn Sie es in einer Datei speichern möchten.

 **Examples:** 

Zeigt, wie eingebettete OLE-Objekte in Dateien extrahiert werden.

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
java.lang.String - Die für das aktuelle eingebettete Objekt empfohlene Dateierweiterung, wenn Sie es in einer Datei speichern möchten.
### getSuggestedFileName() {#getSuggestedFileName}
```
public String getSuggestedFileName()
```


Ruft den für das aktuelle eingebettete Objekt empfohlenen Dateinamen ab, wenn Sie es in einer Datei speichern möchten.

 **Examples:** 

Zeigt, wie der empfohlene Dateiname eines OLE-Objekts ermittelt wird.

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
java.lang.String - Der für das aktuelle eingebettete Objekt empfohlene Dateiname, wenn Sie es in einer Datei speichern möchten.
### isLink() {#isLink}
```
public boolean isLink()
```


Gibt  true  zurück, wenn das OLE-Objekt verknüpft ist (wenn [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) angegeben ist).

 **Examples:** 

Zeigt, wie man verknüpfte und nicht verknüpfte OLE-Objekte einfügt.

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
boolean -  true  wenn das OLE-Objekt verknüpft ist (wenn [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) angegeben ist).
### isLocked() {#isLocked}
```
public boolean isLocked()
```


Gibt an, ob die Verknüpfung zum OLE-Objekt vor Aktualisierungen gesperrt ist.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie eingebettete OLE-Objekte in Dateien extrahiert werden.

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
boolean - Der entsprechende  boolean  Wert.
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Gibt an, ob die Verknüpfung zum OLE-Objekt vor Aktualisierungen gesperrt ist.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie eingebettete OLE-Objekte in Dateien extrahiert werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### save(OutputStream stream) {#save-java.io.OutputStream}
```
public void save(OutputStream stream)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


Speichert die Daten des eingebetteten Objekts in einer Datei mit dem angegebenen Namen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | java.lang.String | Name der Datei, in der die OLE-Objektdaten gespeichert werden. |

### setAutoUpdate(boolean value) {#setAutoUpdate-boolean}
```
public void setAutoUpdate(boolean value)
```


Gibt an, ob die Verknüpfung zum OLE-Objekt in Microsoft Word automatisch aktualisiert wird oder nicht.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie eingebettete OLE-Objekte in Dateien extrahiert werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setProgId(String value) {#setProgId-java.lang.String}
```
public void setProgId(String value)
```


Legt die ProgID des OLE-Objekts fest.

 **Remarks:** 

Die ProgID‑Eigenschaft ist in Microsoft‑Word‑Dokumenten nicht immer vorhanden und kann nicht zuverlässig verwendet werden.

Darf nicht  null  sein.

Der Standardwert ist eine leere Zeichenfolge.

 **Examples:** 

Zeigt, wie eingebettete OLE-Objekte in Dateien extrahiert werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Die ProgID des OLE-Objekts. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String}
```
public void setSourceFullName(String value)
```


Legt den Pfad und den Namen der Quelldatei für das verknüpfte OLE-Objekt fest.

 **Remarks:** 

Der Standardwert ist eine leere Zeichenfolge.

Wenn [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) kein leerer String ist, ist das OLE-Objekt verknüpft.

 **Examples:** 

Zeigt, wie man verknüpfte und nicht verknüpfte OLE-Objekte einfügt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Pfad und Name der Quelldatei für das verknüpfte OLE-Objekt. |

### setSourceItem(String value) {#setSourceItem-java.lang.String}
```
public void setSourceItem(String value)
```


Legt eine Zeichenkette fest, die verwendet wird, um den Teil der Quelldatei zu identifizieren, der verknüpft wird.

 **Remarks:** 

Der Standardwert ist eine leere Zeichenfolge.

Zum Beispiel, wenn die Quelldatei eine Microsoft‑Excel‑Arbeitsmappe ist, könnte die Eigenschaft [getSourceItem()](../../com.aspose.words/oleformat/\#getSourceItem) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceItem-java.lang.String) den Wert "Workbook1!R3C1:R4C2" zurückgeben, wenn das OLE-Objekt nur wenige Zellen aus dem Arbeitsblatt enthält.

 **Examples:** 

Zeigt, wie man verknüpfte und nicht verknüpfte OLE-Objekte einfügt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Ein String, der verwendet wird, um den Teil der Quelldatei zu identifizieren, der verknüpft wird. |

