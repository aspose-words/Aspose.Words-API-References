---
title: ViewType Enum
linktitle: ViewType
articleTitle: ViewType
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Settings.ViewType enum for Microsoft Word. Unlock flexible view modes to enhance document presentation and user experience.
type: docs
weight: 6790
url: /net/aspose.words.settings/viewtype/
---
## ViewType enumeration

Possible values for the view mode in Microsoft Word.

```csharp
public enum ViewType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | The document shall be rendered in the default view of the application. |
| Reading | `0` | The document shall be rendered in the default view of the application. |
| PageLayout | `1` | The document shall be opened in a view that displays the document as it will print. |
| Outline | `3` | The document shall be rendered in a view optimized for outlining or creating long documents. |
| Normal | `4` | The document shall be rendered in a view optimized for outlining or creating long documents. |
| Web | `5` | The document shall be rendered in a view mimicking the way this document would be displayed in a web page. |

## Examples

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.That(doc.ViewOptions.ZoomType, Is.EqualTo(ZoomType.Custom));
Assert.That(doc.ViewOptions.ZoomType, Is.EqualTo(ZoomType.None));

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

### See Also

* class [ViewOptions](../viewoptions/)
* property [ViewType](../viewoptions/viewtype/)
* namespace [Aspose.Words.Settings](../../aspose.words.settings/)
* assembly [Aspose.Words](../../)
