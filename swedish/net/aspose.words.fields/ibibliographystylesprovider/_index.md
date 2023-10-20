---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: Aspose.Words för .NET
description: Aspose.Words.Fields.IBibliographyStylesProvider gränssnitt. Implementera detta gränssnitt för att tillhandahålla bibliografistil för FieldBibliography ochFieldCitation fält när de uppdateras i C#.
type: docs
weight: 2670
url: /sv/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

Implementera detta gränssnitt för att tillhandahålla bibliografistil för [`FieldBibliography`](../fieldbibliography/) och[`FieldCitation`](../fieldcitation/) fält när de uppdateras.

```csharp
public interface IBibliographyStylesProvider
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(*string*) | Returnerar bibliografistil. |

## Exempel

Visar hur man åsidosätter inbyggda stilar eller tillhandahåller en anpassad.

```csharp
public void ChangeBibliographyStyles()
{            
    Document doc = new Document(MyDir + "Bibliography.docx");

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
