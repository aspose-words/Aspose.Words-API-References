---
title: SaveOptions.ExportGeneratorName
linktitle: ExportGeneratorName
articleTitle: ExportGeneratorName
second_title: Aspose.Words para .NET
description: Mejore sus documentos con la propiedad SaveOptions ExportGeneratorName. Incorpore el nombre y la versión de Aspose.Words para una mejor trazabilidad. Valor predeterminado verdadero.
type: docs
weight: 80
url: /es/net/aspose.words.saving/saveoptions/exportgeneratorname/
---
## SaveOptions.ExportGeneratorName property

Cuando`verdadero` , hace que el nombre y la versión de Aspose.Words se incrusten en los archivos producidos. El valor predeterminado es`verdadero` .

```csharp
public bool ExportGeneratorName { get; set; }
```

## Ejemplos

Muestra cómo deshabilitar la adición de nombre y versión de Aspose.Words en los archivos producidos.

```csharp
Document doc = new Document();

// Utilice https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ para saber cómo comprobar el resultado.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { ExportGeneratorName = false };

doc.Save(ArtifactsDir + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
