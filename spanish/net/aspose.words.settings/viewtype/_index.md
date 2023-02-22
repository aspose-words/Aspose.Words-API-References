---
title: Enum ViewType
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Settings.ViewType enumeración. Valores posibles para el modo de vista en Microsoft Word.
type: docs
weight: 5660
url: /es/net/aspose.words.settings/viewtype/
---
## ViewType enumeration

Valores posibles para el modo de vista en Microsoft Word.

```csharp
public enum ViewType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | El documento se representará en la vista predeterminada de la aplicación. |
| Reading | `0` | El documento se representará en la vista predeterminada de la aplicación. |
| PageLayout | `1` | El documento se abrirá en una vista que muestre el documento tal como se imprimirá. |
| Outline | `3` | El documento se representará en una vista optimizada para delinear o crear documentos extensos. |
| Normal | `4` | El documento se representará en una vista optimizada para delinear o crear documentos extensos. |
| Web | `5` | El documento se representará en una vista que imite la forma en que se mostraría este documento en una página web. |

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

### Ver también

* class [ViewOptions](../viewoptions/)
* property [ViewType](../viewoptions/viewtype/)
* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)


