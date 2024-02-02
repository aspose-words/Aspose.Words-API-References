---
title: Style.SemiHidden
linktitle: SemiHidden
articleTitle: SemiHidden
second_title: Aspose.Words for .NET
description: Style SemiHidden property. Gets/sets whether the style hides from the Styles gallery and from the Styles task pane in C#.
type: docs
weight: 170
url: /net/aspose.words/style/semihidden/
---
## Style.SemiHidden property

Gets/sets whether the style hides from the Styles gallery and from the Styles task pane.

```csharp
public bool SemiHidden { get; set; }
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
