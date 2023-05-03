---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
linktitle: ContinuousSectionPageNumberingRestart
second_title: Aspose.Words for .NET API Reference
description: LayoutOptions ContinuousSectionPageNumberingRestart property. Gets or sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering in C#.
type: docs
weight: 40
url: /net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## ContinuousSectionPageNumberingRestart property

Gets or sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

## Remarks

The default value is Always. It matches the behavior of MS Word 2019 which was the latest version at the moment the option was introduced. Older page numbering logic demonstrated by MS Word 2016 is available via this option. Please [`ContinuousSectionRestart`](../../continuoussectionrestart/) for the behavior description.

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

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* namespace [Aspose.Words.Layout](../../layoutoptions/)
* assembly [Aspose.Words](../../../)
