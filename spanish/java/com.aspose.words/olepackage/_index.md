---
title: "OlePackage"
linktitle: "OlePackage"
second_title: "Aspose.Words para Java"
description: "Permite acceder a las propiedades del paquete OLE en Java."
type: docs
weight: 502
url: /es/java/com.aspose.words/olepackage/
---

**Inheritance:**
java.lang.Object
```
public class OlePackage
```

Permite acceder a las propiedades del paquete OLE.

Para obtener más información, visite el artículo de documentación [ Working with Ole Objects ][Working with Ole Objects].

 **Remarks:** 

OLE package es un método heredado y "no documentado" para almacenar objetos incrustados si el controlador OLE es desconocido. Las versiones tempranas de Windows, como Windows 3.1, 95 y 98, tenían la aplicación Packager.exe que podía usarse para incrustar cualquier tipo de datos en un documento. Ahora esta aplicación está excluida de Windows, pero MS Word y otras aplicaciones aún la utilizan para incrustar datos si el controlador OLE falta o es desconocido.

 **Examples:** 

Muestra cómo insertar un objeto OLE en un documento.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getDisplayName()](#getDisplayName) | Obtiene el nombre para mostrar del paquete OLE. |
| [getFileName()](#getFileName) | Obtiene el nombre de archivo del paquete OLE. |
| [setDisplayName(String value)](#setDisplayName-java.lang.String) | Establece el nombre para mostrar del paquete OLE. |
| [setFileName(String value)](#setFileName-java.lang.String) | Establece el nombre de archivo del paquete OLE. |
### getDisplayName() {#getDisplayName}
```
public String getDisplayName()
```


Obtiene el nombre para mostrar del paquete OLE.

 **Examples:** 

Muestra cómo insertar un objeto OLE en un documento.

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
java.lang.String - Nombre para mostrar del paquete OLE.
### getFileName() {#getFileName}
```
public String getFileName()
```


Obtiene el nombre de archivo del paquete OLE.

 **Examples:** 

Muestra cómo insertar un objeto OLE en un documento.

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
java.lang.String - Nombre de archivo del paquete OLE.
### setDisplayName(String value) {#setDisplayName-java.lang.String}
```
public void setDisplayName(String value)
```


Establece el nombre para mostrar del paquete OLE.

 **Examples:** 

Muestra cómo insertar un objeto OLE en un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Nombre para mostrar del paquete OLE. |

### setFileName(String value) {#setFileName-java.lang.String}
```
public void setFileName(String value)
```


Establece el nombre de archivo del paquete OLE.

 **Examples:** 

Muestra cómo insertar un objeto OLE en un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Nombre de archivo del paquete OLE. |

