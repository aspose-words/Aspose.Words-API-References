---
title: HtmlFixedSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words para .NET
description: Optimice su salida HTML con la propiedad HtmlFixedSaveOptions. Mejore el rendimiento eliminando lienzos redundantes y fusionando glifos similares. Valor predeterminado verdadero.
type: docs
weight: 110
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

El indicador indica si es necesario optimizar la salida. Si se establece este indicador, se eliminan los lienzos anidados redundantes y los lienzos vacíos, también se concatenan los glifos vecinos con el mismo formato. Nota: La precisión de la visualización del contenido puede verse afectada si esta propiedad se establece en`verdadero` . El valor predeterminado es`verdadero` .

```csharp
public override bool OptimizeOutput { get; set; }
```

## Ejemplos

Muestra cómo simplificar un documento al guardarlo en HTML eliminando varios objetos redundantes.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { OptimizeOutput = optimizeOutput };

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

//El tamaño de la versión optimizada del documento es casi un tercio del tamaño del documento no optimizado.
Assert.AreEqual(optimizeOutput ? 60385 : 191000,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### Ver también

* class [HtmlFixedSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
