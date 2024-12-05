---
title: ZoomType Enum
linktitle: ZoomType
articleTitle: ZoomType
second_title: Aspose.Words for .NET
description: Aspose.Words.Settings.ZoomType enum. Possible values for how large or small the document appears on the screen in Microsoft Word in C#.
type: docs
weight: 6610
url: /net/aspose.words.settings/zoomtype/
---
## ZoomType enumeration

Possible values for how large or small the document appears on the screen in Microsoft Word.

```csharp
public enum ZoomType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Custom | `0` | Zoom percentage is set explicitly. It is not recalculated automatically when control size changes. |
| None | `0` | Indicates to use the explicit zoom percentage. Same as Custom. |
| FullPage | `1` | Zoom percentage is automatically recalculated to fit one full page. |
| PageWidth | `2` | Zoom percentage is automatically recalculated to fit page width. |
| TextFit | `3` | Zoom percentage is automatically recalculated to fit text. |

## Examples

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

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

### See Also

* class [ViewOptions](../viewoptions/)
* property [ZoomType](../viewoptions/zoomtype/)
* namespace [Aspose.Words.Settings](../../aspose.words.settings/)
* assembly [Aspose.Words](../../)
