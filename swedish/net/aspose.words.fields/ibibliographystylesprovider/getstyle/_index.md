---
title: IBibliographyStylesProvider.GetStyle
linktitle: GetStyle
articleTitle: GetStyle
second_title: Aspose.Words för .NET
description: Upptäck IBibliographyStylesProviders GetStyle-metod för att enkelt hämta och anpassa dina bibliografiska stilar för förbättrat akademiskt skrivande.
type: docs
weight: 10
url: /sv/net/aspose.words.fields/ibibliographystylesprovider/getstyle/
---
## IBibliographyStylesProvider.GetStyle method

Returnerar bibliografisk stil.

```csharp
public Stream GetStyle(string styleFileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| styleFileName | String | Filnamnet för bibliografistilen. |

### Returvärde

DeStream med XSLT-formatmallar för bibliografi.

## Anmärkningar

Implementeringen ska returnera`null` för att indikera att MS Word-versionen av den angivna stilen ska användas.

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

* interface [IBibliographyStylesProvider](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
