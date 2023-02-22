---
title: Class ViewOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Settings.ViewOptions clase. Proporciona varias opciones que controlan cómo se muestra un documento en Microsoft Word.
type: docs
weight: 5650
url: /es/net/aspose.words.settings/viewoptions/
---
## ViewOptions class

Proporciona varias opciones que controlan cómo se muestra un documento en Microsoft Word.

```csharp
public class ViewOptions
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayBackgroundShape](../../aspose.words.settings/viewoptions/displaybackgroundshape/) { get; set; } | Controla la visualización de la forma de fondo en la vista de diseño de impresión. |
| [DoNotDisplayPageBoundaries](../../aspose.words.settings/viewoptions/donotdisplaypageboundaries/) { get; set; } | Desactiva la visualización del espacio entre la parte superior del texto y el borde superior de la página. |
| [FormsDesign](../../aspose.words.settings/viewoptions/formsdesign/) { get; set; } | Especifica si el documento está en modo de diseño de formularios. |
| [ViewType](../../aspose.words.settings/viewoptions/viewtype/) { get; set; } | Controla el modo de vista en Microsoft Word. |
| [ZoomPercent](../../aspose.words.settings/viewoptions/zoompercent/) { get; set; } | Obtiene o establece el porcentaje (entre 10 y 500) en el que desea ver su documento. |
| [ZoomType](../../aspose.words.settings/viewoptions/zoomtype/) { get; set; } | Obtiene o establece un valor de zoom basado en el tamaño de la ventana. |

### Ejemplos

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

Muestra cómo establecer un tipo de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Establecer la propiedad "ZoomType" en "ZoomType.PageWidth" para obtener Microsoft Word
// para hacer zoom automáticamente en el documento para que se ajuste al ancho de la página.
// Establezca la propiedad "ZoomType" en "ZoomType.FullPage" para obtener Microsoft Word
// para ampliar automáticamente el documento y hacer visible toda la primera página.
// Establezca la propiedad "ZoomType" en "ZoomType.TextFit" para obtener Microsoft Word
// para hacer zoom automáticamente en el documento para que se ajuste a los márgenes de texto internos de la primera página.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Ver también

* class [Document](../../aspose.words/document/)
* property [ViewOptions](../../aspose.words/document/viewoptions/)
* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)


