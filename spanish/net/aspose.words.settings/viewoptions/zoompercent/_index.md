---
title: ViewOptions.ZoomPercent
second_title: Referencia de API de Aspose.Words para .NET
description: ViewOptions propiedad. Obtiene o establece el porcentaje entre 10 y 500 en el que desea ver su documento.
type: docs
weight: 50
url: /es/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

Obtiene o establece el porcentaje (entre 10 y 500) en el que desea ver su documento.

```csharp
public int ZoomPercent { get; set; }
```

### Observaciones

Si el valor es 0, entonces esta propiedad usa 100; de lo contrario, si el valor es menor que 10 o mayor que 500, esta propiedad arroja.

Aunque Aspose.Words puede leer y escribir esta opción, su uso es específico de la aplicación. Por ejemplo MS Word 2013 no respeta el valor de esta opción.

### Ejemplos

Muestra cómo configurar un factor de zoom personalizado, que las versiones anteriores de Microsoft Word se aplicarán a un documento al cargarlo.

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
* espacio de nombres [Aspose.Words.Settings](../../viewoptions/)
* asamblea [Aspose.Words](../../../)


