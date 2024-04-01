---
title: TxtLeadingSpacesOptions Enum
linktitle: TxtLeadingSpacesOptions
articleTitle: TxtLeadingSpacesOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Loading.TxtLeadingSpacesOptions enum. Specifies available options for leading space handling during import from Text file in C#.
type: docs
weight: 3880
url: /net/aspose.words.loading/txtleadingspacesoptions/
---
## TxtLeadingSpacesOptions enumeration

Specifies available options for leading space handling during import from Text file.

```csharp
public enum TxtLeadingSpacesOptions
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| ConvertToIndent | `0` | Leading spaces are removed and converted to left indent. |
| Trim | `1` | Leading spaces are trimmed |
| Preserve | `2` | Leading spaces are preserved. |

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
        Assert.AreEqual(37.8d, paragraphs[0].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(25.2d, paragraphs[1].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(6.3d, paragraphs[2].ParagraphFormat.FirstLineIndent);

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
    case TxtLeadingSpacesOptions.Preserve:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("      Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("    Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith(" Line 3"));
        break;
    case TxtLeadingSpacesOptions.Trim:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
}

switch (txtTrailingSpacesOptions)
{
    case TxtTrailingSpacesOptions.Preserve:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1 \r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2   \r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3       \f"));
        break;
    case TxtTrailingSpacesOptions.Trim:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1\r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2\r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3\f"));
        break;
}
```

### See Also

* namespace [Aspose.Words.Loading](../../aspose.words.loading/)
* assembly [Aspose.Words](../../)
