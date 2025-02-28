---
title: OutlineLevel Enum
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.OutlineLevel enum to easily manage paragraph outline levels in your documents for enhanced organization and clarity.
type: docs
weight: 4930
url: /net/aspose.words/outlinelevel/
---
## OutlineLevel enumeration

Specifies the outline level of a paragraph in the document.

```csharp
public enum OutlineLevel
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Level1 | `0` | The paragraph is at the outline level 1 (topmost level). |
| Level2 | `1` | The paragraph is at the outline level 2. |
| Level3 | `2` | The paragraph is at the outline level 3. |
| Level4 | `3` | The paragraph is at the outline level 4. |
| Level5 | `4` | The paragraph is at the outline level 5. |
| Level6 | `5` | The paragraph is at the outline level 6. |
| Level7 | `6` | The paragraph is at the outline level 7. |
| Level8 | `7` | The paragraph is at the outline level 8. |
| Level9 | `8` | The paragraph is at the outline level 9. |
| BodyText | `9` | The paragraph is at the level of the main text. |

## Examples

Shows how to configure paragraph outline levels to create collapsible text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Each paragraph has an OutlineLevel, which could be any number from 1 to 9, or at the default "BodyText" value.
// Setting the property to one of the numbered values will show an arrow to the left
// of the beginning of the paragraph.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Level 1 is the topmost level. If there is a paragraph with a lower level below a paragraph with a higher level,
// collapsing the higher-level paragraph will collapse the lower level paragraph.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Two paragraphs of the same level will not collapse each other,
// and the arrows do not collapse the paragraphs they point to.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// The default "BodyText" value is the lowest, which a paragraph of any level can collapse.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
