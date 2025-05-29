---
title: FieldOptions.BibliographyStylesProvider
linktitle: BibliographyStylesProvider
articleTitle: BibliographyStylesProvider
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldOptions BibliographyStylesProvider för anpassningsbara bibliografiska stilar, vilket förbättrar dina fält FieldBibliography och FieldCitation.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldoptions/bibliographystylesprovider/
---
## FieldOptions.BibliographyStylesProvider property

Hämtar eller ställer in en leverantör som returnerar en bibliografistil för [`FieldBibliography`](../../fieldbibliography/) och[`FieldCitation`](../../fieldcitation/) fält.

```csharp
public IBibliographyStylesProvider BibliographyStylesProvider { get; set; }
```

## Exempel

Visar hur man åsidosätter inbyggda stilar eller anger en anpassad.

```csharp
public void ChangeBibliographyStyles()
{
    Document doc = new Document(MyDir + "Bibliography.docx");

    // Om dokumentet redan har en stil kan du ändra den med följande kod:
    // doc.Bibliography.BibliographyStyle = "Anpassad bibliografistil.xsl";

    doc.FieldOptions.BibliographyStylesProvider = new BibliographyStylesProvider();
    doc.UpdateFields();

    doc.Save(ArtifactsDir + "Field.ChangeBibliographyStyles.docx");

}

public class BibliographyStylesProvider : IBibliographyStylesProvider
{
    Stream IBibliographyStylesProvider.GetStyle(string styleFileName)
    {
        return File.OpenRead(MyDir + "Bibliography custom style.xsl");
    }
}
```

### Se även

* interface [IBibliographyStylesProvider](../../ibibliographystylesprovider/)
* class [FieldOptions](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
