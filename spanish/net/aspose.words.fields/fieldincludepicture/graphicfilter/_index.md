---
title: FieldIncludePicture.GraphicFilter
linktitle: GraphicFilter
articleTitle: GraphicFilter
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldIncludePicture GraphicFilter, administre fácilmente los filtros de formato gráfico para una integración perfecta de imágenes en sus proyectos.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldincludepicture/graphicfilter/
---
## FieldIncludePicture.GraphicFilter property

Obtiene o establece el nombre del filtro para el formato del gráfico que se va a insertar.

```csharp
public string GraphicFilter { get; set; }
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

* class [FieldIncludePicture](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
