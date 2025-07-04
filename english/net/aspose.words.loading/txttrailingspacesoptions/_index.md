---
title: TxtTrailingSpacesOptions Enum
linktitle: TxtTrailingSpacesOptions
articleTitle: TxtTrailingSpacesOptions
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.TxtTrailingSpacesOptions enum for efficient trailing space management when importing text files. Enhance your document processing today!
type: docs
weight: 4190
url: /net/aspose.words.loading/txttrailingspacesoptions/
---
## TxtTrailingSpacesOptions enumeration

Specifies available options for trailing spaces handling during import from Text file.

```csharp
public enum TxtTrailingSpacesOptions
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Trim | `0` | Trailing spaces are trimmed. |
| Preserve | `1` | Trailing spaces are preserved. |

## Examples

Shows how to trim whitespace when loading plaintext documents.

```csharp
string textDoc = "      Line 1 \n" +
                 "    Line 2   \n" +
                 " Line 3       ";

// Create a "TxtLoadOptions" object, which we can pass to a document's constructor
// to modify how we load a plaintext document.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Preserve"
// to preserve all whitespace characters at the start of every line.
// Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.ConvertToIndent"
// to remove all whitespace characters from the start of every line,
// and then apply a left first line indent to the paragraph to simulate the effect of the whitespaces.
// Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Trim"
// to remove all whitespace characters from every line's start.
loadOptions.LeadingSpacesOptions = txtLeadingSpacesOptions;

// Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Preserve"
// to preserve all whitespace characters at the end of every line. 
// Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Trim" to 
// remove all whitespace characters from the end of every line.
loadOptions.TrailingSpacesOptions = txtTrailingSpacesOptions;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

switch (txtLeadingSpacesOptions)
{
    case TxtLeadingSpacesOptions.ConvertToIndent:
        Assert.That(paragraphs[0].ParagraphFormat.FirstLineIndent, Is.EqualTo(37.8d));
        Assert.That(paragraphs[1].ParagraphFormat.FirstLineIndent, Is.EqualTo(25.2d));
        Assert.That(paragraphs[2].ParagraphFormat.FirstLineIndent, Is.EqualTo(6.3d));

        Assert.That(paragraphs[0].GetText().StartsWith("Line 1"), Is.True);
        Assert.That(paragraphs[1].GetText().StartsWith("Line 2"), Is.True);
        Assert.That(paragraphs[2].GetText().StartsWith("Line 3"), Is.True);
        break;
    case TxtLeadingSpacesOptions.Preserve:
        Assert.That(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d), Is.True);

        Assert.That(paragraphs[0].GetText().StartsWith("      Line 1"), Is.True);
        Assert.That(paragraphs[1].GetText().StartsWith("    Line 2"), Is.True);
        Assert.That(paragraphs[2].GetText().StartsWith(" Line 3"), Is.True);
        break;
    case TxtLeadingSpacesOptions.Trim:
        Assert.That(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d), Is.True);

        Assert.That(paragraphs[0].GetText().StartsWith("Line 1"), Is.True);
        Assert.That(paragraphs[1].GetText().StartsWith("Line 2"), Is.True);
        Assert.That(paragraphs[2].GetText().StartsWith("Line 3"), Is.True);
        break;
}

switch (txtTrailingSpacesOptions)
{
    case TxtTrailingSpacesOptions.Preserve:
        Assert.That(paragraphs[0].GetText().EndsWith("Line 1 \r"), Is.True);
        Assert.That(paragraphs[1].GetText().EndsWith("Line 2   \r"), Is.True);
        Assert.That(paragraphs[2].GetText().EndsWith("Line 3       \f"), Is.True);
        break;
    case TxtTrailingSpacesOptions.Trim:
        Assert.That(paragraphs[0].GetText().EndsWith("Line 1\r"), Is.True);
        Assert.That(paragraphs[1].GetText().EndsWith("Line 2\r"), Is.True);
        Assert.That(paragraphs[2].GetText().EndsWith("Line 3\f"), Is.True);
        break;
}
```

### See Also

* namespace [Aspose.Words.Loading](../../aspose.words.loading/)
* assembly [Aspose.Words](../../)
