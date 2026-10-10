---
title: "OlePackage"
linktitle: "OlePackage"
second_title: "Aspose.Words Java için"
description: "Java'da OLE Package özelliklerine erişim sağlar."
type: docs
weight: 502
url: /tr/java/com.aspose.words/olepackage/
---

**Inheritance:**
java.lang.Object
```
public class OlePackage
```

OLE Paket özelliklerine erişim sağlar.

Daha fazla bilgi edinmek için, [ Working with Ole Objects ][Working with Ole Objects] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

OLE paketi, OLE işleyicisi bilinmiyorsa gömülü nesneyi depolamanın eski ve "belgelendirilmemiş" bir yoludur. Windows 3.1, 95 ve 98 gibi erken Windows sürümlerinde, belgeye herhangi bir veri türü gömmek için kullanılabilen Packager.exe uygulaması bulunuyordu. Şimdi bu uygulama Windows'tan çıkarılmış olsa da, MS Word ve diğer uygulamalar OLE işleyicisi eksik veya bilinmiyorsa veriyi gömmek için hâlâ kullanıyor.

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


[Working with Ole Objects]: https://docs.aspose.com/words/java/working-with-ole-objects/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getDisplayName()](#getDisplayName) | OLE Package görüntüleme adını alır. |
| [getFileName()](#getFileName) | OLE Package dosya adını alır. |
| [setDisplayName(String value)](#setDisplayName-java.lang.String) | OLE Package görüntüleme adını ayarlar. |
| [setFileName(String value)](#setFileName-java.lang.String) | OLE Package dosya adını ayarlar. |
### getDisplayName() {#getDisplayName}
```
public String getDisplayName()
```


OLE Package görüntüleme adını alır.

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
java.lang.String - OLE Package görüntüleme adı.
### getFileName() {#getFileName}
```
public String getFileName()
```


OLE Package dosya adını alır.

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
java.lang.String - OLE Package dosya adı.
### setDisplayName(String value) {#setDisplayName-java.lang.String}
```
public void setDisplayName(String value)
```


OLE Package görüntüleme adını ayarlar.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | OLE Package görüntüleme adı. |

### setFileName(String value) {#setFileName-java.lang.String}
```
public void setFileName(String value)
```


OLE Package dosya adını ayarlar.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | OLE Package dosya adı. |

