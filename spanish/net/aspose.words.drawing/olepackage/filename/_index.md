---
title: OlePackage.FileName
linktitle: FileName
articleTitle: FileName
second_title: Aspose.Words para .NET
description: Descubra la propiedad OlePackage FileName para gestionar fácilmente los nombres de archivo de paquetes OLE. Mejore la gestión de datos con una integración y flexibilidad perfectas.
type: docs
weight: 20
url: /es/net/aspose.words.drawing/olepackage/filename/
---
## OlePackage.FileName property

Obtiene o establece el nombre del archivo del paquete OLE.

```csharp
public string FileName { get; set; }
```

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

* class [OlePackage](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
