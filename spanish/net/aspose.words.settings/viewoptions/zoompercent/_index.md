---
title: ViewOptions.ZoomPercent
linktitle: ZoomPercent
articleTitle: ZoomPercent
second_title: Aspose.Words para .NET
description: Ajuste la propiedad ViewOptions ZoomPercent para establecer el nivel de zoom de su documento entre 10 y 500 %. ¡Mejore la legibilidad y optimice su experiencia de visualización!
type: docs
weight: 50
url: /es/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

Obtiene o establece el porcentaje en el que desea ver su documento.

```csharp
public int ZoomPercent { get; set; }
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

* class [ViewOptions](../)
* espacio de nombres [Aspose.Words.Settings](../../../aspose.words.settings/)
* asamblea [Aspose.Words](../../../)
