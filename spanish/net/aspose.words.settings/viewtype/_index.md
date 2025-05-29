---
title: ViewType Enum
linktitle: ViewType
articleTitle: ViewType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Settings.ViewType para Microsoft Word. Desbloquee modos de visualización flexibles para mejorar la presentación de documentos y la experiencia del usuario.
type: docs
weight: 6790
url: /es/net/aspose.words.settings/viewtype/
---
## ViewType enumeration

Valores posibles para el modo de visualización en Microsoft Word.

```csharp
public enum ViewType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | El documento se mostrará en la vista predeterminada de la aplicación. |
| Reading | `0` | El documento se mostrará en la vista predeterminada de la aplicación. |
| PageLayout | `1` | El documento se abrirá en una vista que muestre el documento tal como se imprimirá. |
| Outline | `3` | El documento se deberá representar en una vista optimizada para delinear o crear documentos largos. |
| Normal | `4` | El documento se deberá representar en una vista optimizada para delinear o crear documentos largos. |
| Web | `5` | El documento se representará en una vista que imite la forma en que este documento se mostraría en una página web. |

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
* property [ViewType](../viewoptions/viewtype/)
* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)
