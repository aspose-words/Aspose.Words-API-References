---
title: RevisionColor Enum
linktitle: RevisionColor
articleTitle: RevisionColor
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Layout.RevisionColor enum to customize document revision colors, enhancing clarity and improving collaboration in your documents.
type: docs
weight: 3830
url: /net/aspose.words.layout/revisioncolor/
---
## RevisionColor enumeration

Allows to specify color of document revisions.

```csharp
public enum RevisionColor
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Auto | `0` | Default. |
| Black | `1` | Represents 000000 color. |
| Blue | `2` | Represents 2e97d3 color. |
| BrightGreen | `3` | Represents 84a35b color. |
| ClassicBlue | `4` | Represents 0000ff color. |
| ClassicRed | `5` | Represents ff0000 color. |
| DarkBlue | `6` | Represents 376e96 color. |
| DarkRed | `7` | Represents 881824 color. |
| DarkYellow | `8` | Represents e09a2b color. |
| Gray25 | `9` | Represents a0a3a9 color. |
| Gray50 | `10` | Represents 50565e color. |
| Green | `11` | Represents 2c6234 color. |
| Pink | `12` | Represents ce338f color. |
| Red | `13` | Represents b5082e color. |
| Teal | `14` | Represents 1b9cab color. |
| Turquoise | `15` | Represents 3eafc2 color. |
| Violet | `16` | Represents 633277 color. |
| White | `17` | Represents ffffff color. |
| Yellow | `18` | Represents fad272 color. |
| LightPink | `19` | Represents fce6f4 color. |
| LightBlue | `20` | Represents e1f2fa color. |
| LightYellow | `21` | Represents fef4de color. |
| LightPurple | `22` | Represents eadfef color. |
| LightOrange | `23` | Represents fce3d0 color. |
| LightGreen | `24` | Represents e9f8ce color. |
| Gray | `25` | Represents efeded color. |
| NoHighlight | `26` | No color is used to highlight revision changes. |
| ByAuthor | `27` | Revisions of each author receive their own color for highlighting from a predefined set of hi-contrast colors. |

## Examples

Shows how to alter the appearance of revisions in a rendered output document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a revision, then change the color of all revisions to green.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Remove the bar that appears to the left of every revised line.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### See Also

* namespace [Aspose.Words.Layout](../../aspose.words.layout/)
* assembly [Aspose.Words](../../)
