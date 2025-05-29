---
title: Bibliography.BibliographyStyle
linktitle: BibliographyStyle
articleTitle: BibliographyStyle
second_title: Aspose.Words för .NET
description: Upptäck egenskapen BibliographyStyle som enkelt hanterar och anpassar din bibliografis aktiva stil för förbättrad organisation och presentation.
type: docs
weight: 10
url: /sv/net/aspose.words.bibliography/bibliography/bibliographystyle/
---
## Bibliography.BibliographyStyle property

Hämtar eller anger en sträng som representerar namnet på den aktiva stilen som ska användas för en bibliografi.

```csharp
public string BibliographyStyle { get; set; }
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

* class [Bibliography](../)
* namnutrymme [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* hopsättning [Aspose.Words](../../../)
