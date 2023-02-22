---
title: HtmlFixedSaveOptions.OptimizeOutput
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlFixedSaveOptions propiedad. El indicador indica si es necesario optimizar la salida. Si este indicador se establece se eliminan los lienzos anidados redundantes y los lienzos vacíos también se concatenan los glifos vecinos con el mismo formato. Nota La precisión de la visualización del contenido puede verse afectada si esta propiedad se establece en true. El valor predeterminado es true.
type: docs
weight: 100
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

El indicador indica si es necesario optimizar la salida. Si este indicador se establece, se eliminan los lienzos anidados redundantes y los lienzos vacíos, también se concatenan los glifos vecinos con el mismo formato. Nota: La precisión de la visualización del contenido puede verse afectada si esta propiedad se establece en true. El valor predeterminado es true.

```csharp
public override bool OptimizeOutput { get; set; }
```

### Ejemplos

Muestra cómo simplificar un documento al guardarlo en HTML mediante la eliminación de varios objetos redundantes.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { OptimizeOutput = optimizeOutput };

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// El tamaño de la versión optimizada del documento es casi un tercio del tamaño del documento no optimizado.
Assert.AreEqual(optimizeOutput ? 62521 : 191770,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### Ver también

* class [HtmlFixedSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* asamblea [Aspose.Words](../../../)


