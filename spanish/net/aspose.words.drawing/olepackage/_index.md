---
title: Class OlePackage
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.OlePackage clase. Permite acceder a las propiedades del paquete OLE.
type: docs
weight: 1160
url: /es/net/aspose.words.drawing/olepackage/
---
## OlePackage class

Permite acceder a las propiedades del paquete OLE.

Para obtener más información, visite el[Trabajar con objetos antiguos](https://docs.aspose.com/words/net/working-with-ole-objects/) artículo de documentación.

```csharp
public class OlePackage
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayName](../../aspose.words.drawing/olepackage/displayname/) { get; set; } | Obtiene o establece el nombre para mostrar del paquete OLE. |
| [FileName](../../aspose.words.drawing/olepackage/filename/) { get; set; } | Obtiene o establece el nombre del archivo del paquete OLE. |

### Observaciones

El paquete OLE es una forma heredada e "indocumentada" de almacenar objetos incrustados si se desconoce el controlador OLE. Las primeras versiones de Windows, como Windows 3.1, 95 y 98, tenían la aplicación Packager.exe que podía usarse para incrustar cualquier tipo de datos en un documento. . Ahora esta aplicación está excluida de Windows, pero MS Word y otras aplicaciones aún la usan para incrustar datos si falta el controlador OLE o se desconoce.

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

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)


