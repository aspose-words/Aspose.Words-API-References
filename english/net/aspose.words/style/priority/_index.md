---
title: Style.Priority
linktitle: Priority
articleTitle: Priority
second_title: Aspose.Words for .NET
description: Style Priority property. Gets/sets the integer value that represents the priority for sorting the styles in the Styles task pane in C#.
type: docs
weight: 160
url: /net/aspose.words/style/priority/
---
## Style.Priority property

Gets/sets the integer value that represents the priority for sorting the styles in the Styles task pane.

```csharp
public int Priority { get; set; }
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
