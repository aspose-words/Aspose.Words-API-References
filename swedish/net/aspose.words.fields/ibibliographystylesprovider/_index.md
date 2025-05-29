---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: Aspose.Words för .NET
description: Förbättra formateringen av ditt dokument med gränssnittet Aspose.Words.IBibliographyStylesProvider, perfekt för att anpassa bibliografiska stilar i källhänvisningar.
type: docs
weight: 3080
url: /sv/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

Implementera detta gränssnitt för att tillhandahålla bibliografisk stil för [`FieldBibliography`](../fieldbibliography/) och[`FieldCitation`](../fieldcitation/) fält när de uppdateras.

```csharp
public interface IBibliographyStylesProvider
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(*string*) | Returnerar bibliografisk stil. |

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

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
