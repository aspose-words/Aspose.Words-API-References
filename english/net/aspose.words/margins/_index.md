---
title: Margins Enum
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words for .NET
description: Aspose.Words.Margins enum. Specifies preset margins in C#.
type: docs
weight: 4290
url: /net/aspose.words/margins/
---
## Margins enumeration

Specifies preset margins.

```csharp
public enum Margins
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Normal | `0` | Normal margins. |
| Narrow | `1` | Narrow margins. |
| Moderate | `2` | Moderate margins. |
| Wide | `3` | Wide margins. |
| Mirrored | `4` | Mirrored margins. |
| Custom | `5` | Custom margins. |

## Examples

Shows when to recalculate the page layout of the document.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Saving a document to PDF, to an image, or printing for the first time will automatically
// cache the layout of the document within its pages.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modify the document in some way.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// In the current version of Aspose.Words, modifying the document does not automatically rebuild
// the cached page layout. If we wish for the cached layout
// to stay up to date, we will need to update it manually.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
