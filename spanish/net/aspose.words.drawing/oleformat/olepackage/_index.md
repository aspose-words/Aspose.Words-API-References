---
title: OleFormat.OlePackage
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words para .NET
description: Acceda fácilmente a las propiedades de OlePackage para objetos OLE. Consiga una integración perfecta con OLE Packages y mejore sus capacidades de gestión de datos.
type: docs
weight: 80
url: /es/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

Proporcionar acceso a[`OlePackage`](../../olepackage/) si el objeto OLE es un paquete OLE. Devuelve`nulo` de lo contrario.

```csharp
public OlePackage OlePackage { get; }
```

## Observaciones

El paquete OLE es una tecnología heredada que permite encapsular cualquier formato de archivo que no esté presente en el registro OLE de un sistema Windows en un paquete genérico que permite incrustar casi cualquier cosa en un documento. Ver[`OlePackage`](../../olepackage/) Escribe para más información.

## Ejemplos

Muestra cómo insertar un objeto OLE en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Los objetos OLE nos permiten abrir otros archivos en el sistema de archivos local usando otra aplicación instalada
// en nuestro sistema operativo haciendo doble clic en la forma que contiene el objeto OLE en el cuerpo del documento.
// En este caso, nuestro archivo externo será un archivo ZIP.
byte[] zipFileBytes = File.ReadAllBytes(DatabaseDir + "cat001.zip");

using (MemoryStream stream = new MemoryStream(zipFileBytes))
{
    Shape shape = builder.InsertOleObject(stream, "Package", true, null);

    shape.OleFormat.OlePackage.FileName = "Package file name.zip";
    shape.OleFormat.OlePackage.DisplayName = "Package display name.zip";
}

doc.Save(ArtifactsDir + "Shape.InsertOlePackage.docx");
```

### Ver también

* class [OlePackage](../../olepackage/)
* class [OleFormat](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
