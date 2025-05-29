---
title: ZoomType Enum
linktitle: ZoomType
articleTitle: ZoomType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Settings.ZoomType para personalizar los tamaños de visualización de documentos en Microsoft Word para una visualización y productividad óptimas.
type: docs
weight: 6810
url: /es/net/aspose.words.settings/zoomtype/
---
## ZoomType enumeration

Valores posibles para determinar qué tan grande o pequeño debe ser el documento que aparece en la pantalla en Microsoft Word.

```csharp
public enum ZoomType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Custom | `0` | El porcentaje de zoom se establece explícitamente. No se recalcula automáticamente al cambiar el tamaño del control. |
| None | `0` | Indica que se debe usar el porcentaje de zoom explícito. Igual queCustom . |
| FullPage | `1` | El porcentaje de zoom se recalcula automáticamente para ajustarse a una página completa. |
| PageWidth | `2` | El porcentaje de zoom se recalcula automáticamente para ajustarse al ancho de la página. |
| TextFit | `3` | El porcentaje de zoom se recalcula automáticamente para ajustar el texto. |

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

### Ver también

* class [ViewOptions](../viewoptions/)
* property [ZoomType](../viewoptions/zoomtype/)
* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)
