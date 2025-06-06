---
title: ViewOptions.ViewType
linktitle: ViewType
articleTitle: ViewType
second_title: Aspose.Words para .NET
description: Descubra la propiedad ViewOptions ViewType para personalizar fácilmente su modo de vista de Microsoft Word para una mayor productividad y una experiencia de edición personalizada.
type: docs
weight: 40
url: /es/net/aspose.words.settings/viewoptions/viewtype/
---
## ViewOptions.ViewType property

Controla el modo de visualización en Microsoft Word.

```csharp
public ViewType ViewType { get; set; }
```

## Observaciones

Aunque Aspose.Words puede leer y escribir esta opción, su uso es específico de la aplicación. Por ejemplo, MS Word 2013 no respeta el valor de esta opción.

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

* enum [ViewType](../../viewtype/)
* class [ViewOptions](../)
* espacio de nombres [Aspose.Words.Settings](../../../aspose.words.settings/)
* asamblea [Aspose.Words](../../../)
