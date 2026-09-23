---
title: "OlePackage"
linktitle: "OlePackage"
second_title: "Aspose.Words für Java"
description: "Ermöglicht den Zugriff auf OLE‑Package‑Eigenschaften in Java."
type: docs
weight: 502
url: /de/java/com.aspose.words/olepackage/
---

**Inheritance:**
java.lang.Object
```
public class OlePackage
```

Ermöglicht den Zugriff auf OLE‑Package‑Eigenschaften.

Um mehr zu erfahren, besuchen Sie den [ Working with Ole Objects ][Working with Ole Objects] Dokumentationsartikel.

 **Remarks:** 

OLE‑Package ist ein veraltetes und "undokumentiert" Verfahren, um eingebettete Objekte zu speichern, wenn der OLE‑Handler unbekannt ist. Frühe Windows‑Versionen wie Windows 3.1, 95 und 98 enthielten die Anwendung Packager.exe, die zum Einbetten beliebiger Daten in ein Dokument verwendet werden konnte. Diese Anwendung ist heute nicht mehr in Windows enthalten, aber MS Word und andere Programme nutzen sie weiterhin, um Daten einzubetten, wenn der OLE‑Handler fehlt oder unbekannt ist.

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


[Working with Ole Objects]: https://docs.aspose.com/words/java/working-with-ole-objects/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getDisplayName()](#getDisplayName) | Liest den Anzeigenamen des OLE‑Package. |
| [getFileName()](#getFileName) | Liest den Dateinamen des OLE‑Package. |
| [setDisplayName(String value)](#setDisplayName-java.lang.String) | Setzt den Anzeigenamen des OLE‑Package. |
| [setFileName(String value)](#setFileName-java.lang.String) | Setzt den Dateinamen des OLE‑Package. |
### getDisplayName() {#getDisplayName}
```
public String getDisplayName()
```


Liest den Anzeigenamen des OLE‑Package.

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
java.lang.String - OLE‑Package‑Anzeigename.
### getFileName() {#getFileName}
```
public String getFileName()
```


Liest den Dateinamen des OLE‑Package.

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
java.lang.String - OLE‑Package‑Dateiname.
### setDisplayName(String value) {#setDisplayName-java.lang.String}
```
public void setDisplayName(String value)
```


Setzt den Anzeigenamen des OLE‑Package.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | OLE‑Package‑Anzeigename. |

### setFileName(String value) {#setFileName-java.lang.String}
```
public void setFileName(String value)
```


Setzt den Dateinamen des OLE‑Package.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | OLE‑Package‑Dateiname. |

