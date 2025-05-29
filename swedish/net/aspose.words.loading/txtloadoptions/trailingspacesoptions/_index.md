---
title: TxtLoadOptions.TrailingSpacesOptions
linktitle: TrailingSpacesOptions
articleTitle: TrailingSpacesOptions
second_title: Aspose.Words för .NET
description: Upptäck egenskapen TrailingSpacesOptions i TxtLoadOptions för att enkelt hantera efterföljande mellanslag. Anpassa hanteringen med standardalternativet Trim för optimala resultat.
type: docs
weight: 70
url: /sv/net/aspose.words.loading/txtloadoptions/trailingspacesoptions/
---
## TxtLoadOptions.TrailingSpacesOptions property

Hämtar eller ställer in önskat alternativ för hantering av efterföljande blanksteg. Standardvärdet ärTrim .

```csharp
public TxtTrailingSpacesOptions TrailingSpacesOptions { get; set; }
```

## Exempel

Visar hur man tar bort blanksteg när man laddar dokument i klartext.

```csharp
string textDoc = "      Line 1 \n" +
                 "    Line 2   \n" +
                 " Line 3       ";

// Skapa ett "TxtLoadOptions"-objekt, som vi kan skicka till ett dokuments konstruktor
// för att ändra hur vi laddar ett klartextdokument.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Ställ in egenskapen "LeadingSpacesOptions" till "TxtLeadingSpacesOptions.Preserve"
// för att bevara alla blanksteg i början av varje rad.
// Ställ in egenskapen "LeadingSpacesOptions" till "TxtLeadingSpacesOptions.ConvertToIndent"
// för att ta bort alla blanksteg från början av varje rad,
// och applicera sedan ett vänsterindrag på första raden i stycket för att simulera effekten av mellanslag.
// Ställ in egenskapen "LeadingSpacesOptions" till "TxtLeadingSpacesOptions.Trim"
// för att ta bort alla blanksteg från början av varje rad.
loadOptions.LeadingSpacesOptions = txtLeadingSpacesOptions;

// Ställ in egenskapen "TrailingSpacesOptions" till "TxtTrailingSpacesOptions.Preserve"
 // för att bevara alla blankstegstecken i slutet av varje rad.
 // Ställ in egenskapen "TrailingSpacesOptions" till "TxtTrailingSpacesOptions.Trim" till
// ta bort alla blanksteg från slutet av varje rad.
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

### Se även

* enum [TxtTrailingSpacesOptions](../../txttrailingspacesoptions/)
* class [TxtLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
