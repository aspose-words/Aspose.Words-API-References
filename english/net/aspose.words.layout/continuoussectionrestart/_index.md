---
title: ContinuousSectionRestart Enum
linktitle: ContinuousSectionRestart
articleTitle: ContinuousSectionRestart
second_title: Aspose.Words for .NET
description: Aspose.Words.Layout.ContinuousSectionRestart enum. Represents different behaviors when computing page numbers in a continuous section that restarts page numbering in C#.
type: docs
weight: 3270
url: /net/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enumeration

Represents different behaviors when computing page numbers in a continuous section that restarts page numbering.

```csharp
public enum ContinuousSectionRestart
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Always | `0` | Page numbering always restarts regardless of content flow. |
| FromNewPageOnly | `1` | Page numbering restarts only if there is no other content before the section on the page where the section starts. |

## Examples

Shows how to control page numbering in a continuous section.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// By default Aspose.Words behavior matches the Microsoft Word 2019.
// If you need old Aspose.Words behavior, repetitive Microsoft Word 2016, use 'ContinuousSectionRestart.FromNewPageOnly'.
// Page numbering restarts only if there is no other content before the section on the page where the section starts,
// because of that the numbering will reset to 2 from the second page.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### See Also

* namespace [Aspose.Words.Layout](../../aspose.words.layout/)
* assembly [Aspose.Words](../../)
