---
title: FieldImport.IsLinked
linktitle: IsLinked
articleTitle: IsLinked
second_title: Aspose.Words para .NET
description: Optimice sus documentos con la propiedad IsLinked de FieldImport para reducir el tamaño del archivo excluyendo datos gráficos. ¡Mejore la eficiencia y el rendimiento hoy mismo!
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldimport/islinked/
---
## FieldImport.IsLinked property

Obtiene o establece si se debe reducir el tamaño del archivo al no almacenar datos gráficos con el documento.

```csharp
public bool IsLinked { get; set; }
```

## Ejemplos

Muestra cómo insertar imágenes utilizando los campos IMPORT e INCLUDEPICTURE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran dos tipos de campos similares que podemos usar para mostrar imágenes vinculadas desde el sistema de archivos local.
// 1 - El campo INCLUDEPICTURE:
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// Aplicar el filtro PNG32.FLT.
fieldIncludePicture.GraphicFilter = "PNG32";
fieldIncludePicture.IsLinked = true;
fieldIncludePicture.ResizeHorizontally = true;
fieldIncludePicture.ResizeVertically = true;

// 2 - El campo IMPORTACIÓN:
FieldImport fieldImport = (FieldImport)builder.InsertField(FieldType.FieldImport, true);
fieldImport.SourceFullName = ImageDir + "Transparent background logo.png";
fieldImport.GraphicFilter = "PNG32";
fieldImport.IsLinked = true;

Assert.True(Regex.Match(fieldImport.GetFieldCode(), " IMPORT  .* \\\\c PNG32 \\\\d").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IMPORT.INCLUDEPICTURE.docx");
```

### Ver también

* class [FieldImport](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
