---
title: ViewOptions.ViewType
linktitle: ViewType
articleTitle: ViewType
second_title: Aspose.Words for .NET
description: Discover the ViewOptions ViewType property to easily customize your Microsoft Word view mode for enhanced productivity and a tailored editing experience.
type: docs
weight: 40
url: /net/aspose.words.settings/viewoptions/viewtype/
---
## ViewOptions.ViewType property

Controls the view mode in Microsoft Word.

```csharp
public ViewType ViewType { get; set; }
```

## Remarks

Although Aspose.Words is able to read and write this option, its usage is application-specific. For example MS Word 2013 does not respect the value of this option.

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

* enum [ViewType](../../viewtype/)
* class [ViewOptions](../)
* namespace [Aspose.Words.Settings](../../../aspose.words.settings/)
* assembly [Aspose.Words](../../../)
