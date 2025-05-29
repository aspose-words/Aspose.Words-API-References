---
title: Document.ViewOptions
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words para .NET
description: Descubra la propiedad Document ViewOptions para personalizar la configuración de visualización de Microsoft Word para una experiencia de visualización personalizada.
type: docs
weight: 490
url: /es/net/aspose.words/document/viewoptions/
---
## Document.ViewOptions property

Proporciona opciones para controlar cómo se muestra el documento en Microsoft Word.

```csharp
public ViewOptions ViewOptions { get; }
```

## Ejemplos

Muestra cómo establecer un factor de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

Muestra cómo configurar un tipo de zoom personalizado que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Establezca la propiedad "ZoomType" en "ZoomType.PageWidth" para obtener Microsoft Word
// para ampliar automáticamente el documento para que se ajuste al ancho de la página.
// Establezca la propiedad "ZoomType" en "ZoomType.FullPage" para obtener Microsoft Word
// para ampliar automáticamente el documento y hacer visible toda la primera página.
// Establezca la propiedad "ZoomType" en "ZoomType.TextFit" para obtener Microsoft Word
// para ampliar automáticamente el documento para que se ajuste a los márgenes de texto internos de la primera página.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Ver también

* class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
