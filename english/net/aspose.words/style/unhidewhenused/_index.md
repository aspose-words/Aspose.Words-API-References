---
title: Style.UnhideWhenUsed
linktitle: UnhideWhenUsed
articleTitle: UnhideWhenUsed
second_title: Aspose.Words for .NET
description: Discover how to manage the UnhideWhenUsed property for styles. Control visibility in the Styles gallery and task pane to enhance your document's design.
type: docs
weight: 210
url: /net/aspose.words/style/unhidewhenused/
---
## Style.UnhideWhenUsed property

Gets/sets whether the style used in the current document unhides from the Styles gallery and from the Styles task pane. True when the used style should be shown in the Styles gallery.

```csharp
public bool UnhideWhenUsed { get; set; }
```

## Examples

Shows how to prioritize and hide a style.

```csharp
Document doc = new Document();
Style styleTitle = doc.Styles[StyleIdentifier.Subtitle];

if (styleTitle.Priority == 9)
    styleTitle.Priority = 10;

if (!styleTitle.UnhideWhenUsed)
    styleTitle.UnhideWhenUsed = true;

if (styleTitle.SemiHidden)
    styleTitle.SemiHidden = true;

doc.Save(ArtifactsDir + "Styles.StylePriority.docx");
```

### See Also

* class [Style](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
