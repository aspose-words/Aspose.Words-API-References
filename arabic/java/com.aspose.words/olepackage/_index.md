---
title: "OlePackage"
linktitle: "OlePackage"
second_title: "Aspose.Words لـ Java"
description: "يسمح بالوصول إلى خصائص OLE Package في Java."
type: docs
weight: 502
url: /ar/java/com.aspose.words/olepackage/
---

**Inheritance:**
java.lang.Object
```
public class OlePackage
```

يسمح بالوصول إلى خصائص حزمة OLE.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Ole Objects ][Working with Ole Objects].

 **Remarks:** 

حزمة OLE هي طريقة قديمة و "غير موثقة" لتخزين الكائن المدمج إذا كان معالج OLE غير معروف. إصدارات Windows المبكرة مثل Windows 3.1 و 95 و 98 كان لديها تطبيق Packager.exe الذي يمكن استخدامه لتضمين أي نوع من البيانات في المستند. الآن تم استبعاد هذا التطبيق من Windows لكن MS Word وغيرها من التطبيقات لا تزال تستخدمه لتضمين البيانات إذا كان معالج OLE مفقودًا أو غير معروف.

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


[Working with Ole Objects]: https://docs.aspose.com/words/java/working-with-ole-objects/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getDisplayName()](#getDisplayName) | يحصل على اسم العرض لحزمة OLE. |
| [getFileName()](#getFileName) | يحصل على اسم ملف حزمة OLE. |
| [setDisplayName(String value)](#setDisplayName-java.lang.String) | يضبط اسم العرض لحزمة OLE. |
| [setFileName(String value)](#setFileName-java.lang.String) | يضبط اسم ملف حزمة OLE. |
### getDisplayName() {#getDisplayName}
```
public String getDisplayName()
```


يحصل على اسم العرض لحزمة OLE.

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
java.lang.String - اسم عرض حزمة OLE.
### getFileName() {#getFileName}
```
public String getFileName()
```


يحصل على اسم ملف حزمة OLE.

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
java.lang.String - اسم ملف حزمة OLE.
### setDisplayName(String value) {#setDisplayName-java.lang.String}
```
public void setDisplayName(String value)
```


يضبط اسم العرض لحزمة OLE.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم عرض حزمة OLE. |

### setFileName(String value) {#setFileName-java.lang.String}
```
public void setFileName(String value)
```


يضبط اسم ملف حزمة OLE.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم ملف حزمة OLE. |

