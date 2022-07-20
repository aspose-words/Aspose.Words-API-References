---
title: DisplayName
second_title: Referencia de API de Aspose.Words para .NET
description: Obtiene o establece el nombre para mostrar del paquete OLE.
type: docs
weight: 10
url: /es/net/aspose.words.drawing/olepackage/displayname/
---
## OlePackage.DisplayName property

Obtiene o establece el nombre para mostrar del paquete OLE.

```csharp
public string DisplayName { get; set; }
```

### Ejemplos

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

* class [OlePackage](../../olepackage)
* espacio de nombres [Aspose.Words.Drawing](../../olepackage)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->