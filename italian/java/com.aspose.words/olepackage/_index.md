---
title: "OlePackage"
linktitle: "OlePackage"
second_title: "Aspose.Words per Java"
description: "Consente di accedere alle proprietà OLE Package in Java."
type: docs
weight: 502
url: /it/java/com.aspose.words/olepackage/
---

**Inheritance:**
java.lang.Object
```
public class OlePackage
```

Consente di accedere alle proprietà del pacchetto OLE.

Per saperne di più, visita l'articolo della documentazione [ Working with Ole Objects ][Working with Ole Objects].

 **Remarks:** 

OLE package è un metodo legacy e "undocumented" per memorizzare oggetti incorporati se il gestore OLE è sconosciuto. Le prime versioni di Windows, come Windows 3.1, 95 e 98, includevano l'applicazione Packager.exe che poteva essere usata per incorporare qualsiasi tipo di dato in un documento. Ora questa applicazione è esclusa da Windows, ma MS Word e altre applicazioni la usano ancora per incorporare dati se il gestore OLE è mancante o sconosciuto.

 **Examples:** 

Mostra come inserire un oggetto OLE in un documento.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getDisplayName()](#getDisplayName) | Ottiene il nome visualizzato del pacchetto OLE. |
| [getFileName()](#getFileName) | Ottiene il nome file del pacchetto OLE. |
| [setDisplayName(String value)](#setDisplayName-java.lang.String) | Imposta il nome visualizzato del pacchetto OLE. |
| [setFileName(String value)](#setFileName-java.lang.String) | Imposta il nome file del pacchetto OLE. |
### getDisplayName() {#getDisplayName}
```
public String getDisplayName()
```


Ottiene il nome visualizzato del pacchetto OLE.

 **Examples:** 

Mostra come inserire un oggetto OLE in un documento.

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
java.lang.String - Nome visualizzato del pacchetto OLE.
### getFileName() {#getFileName}
```
public String getFileName()
```


Ottiene il nome file del pacchetto OLE.

 **Examples:** 

Mostra come inserire un oggetto OLE in un documento.

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
java.lang.String - Nome file del pacchetto OLE.
### setDisplayName(String value) {#setDisplayName-java.lang.String}
```
public void setDisplayName(String value)
```


Imposta il nome visualizzato del pacchetto OLE.

 **Examples:** 

Mostra come inserire un oggetto OLE in un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Nome visualizzato del pacchetto OLE. |

### setFileName(String value) {#setFileName-java.lang.String}
```
public void setFileName(String value)
```


Imposta il nome file del pacchetto OLE.

 **Examples:** 

Mostra come inserire un oggetto OLE in un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Nome file del pacchetto OLE. |

