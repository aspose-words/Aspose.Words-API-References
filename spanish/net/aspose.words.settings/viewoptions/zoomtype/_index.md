---
title: ViewOptions.ZoomType
linktitle: ZoomType
articleTitle: ZoomType
second_title: Aspose.Words para .NET
description: Descubra la propiedad ViewOptions ZoomType para ajustar fácilmente los niveles de zoom según el tamaño de la ventana, mejorando la experiencia del usuario y la flexibilidad de la interfaz.
type: docs
weight: 60
url: /es/net/aspose.words.settings/viewoptions/zoomtype/
---
## ViewOptions.ZoomType property

Obtiene o establece un valor de zoom basado en el tamaño de la ventana.

```csharp
public ZoomType ZoomType { get; set; }
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

* enum [ZoomType](../../zoomtype/)
* class [ViewOptions](../)
* espacio de nombres [Aspose.Words.Settings](../../../aspose.words.settings/)
* asamblea [Aspose.Words](../../../)
