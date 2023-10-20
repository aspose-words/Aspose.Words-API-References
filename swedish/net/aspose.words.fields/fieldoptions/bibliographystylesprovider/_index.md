---
title: FieldOptions.BibliographyStylesProvider
linktitle: BibliographyStylesProvider
articleTitle: BibliographyStylesProvider
second_title: Aspose.Words för .NET
description: FieldOptions BibliographyStylesProvider fast egendom. Hämtar eller ställer in en leverantör som returnerar en bibliografistil för FieldBibliography ochFieldCitation fields i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldoptions/bibliographystylesprovider/
---
## FieldOptions.BibliographyStylesProvider property

Hämtar eller ställer in en leverantör som returnerar en bibliografistil för [`FieldBibliography`](../../fieldbibliography/) och[`FieldCitation`](../../fieldcitation/) fields.

```csharp
public IBibliographyStylesProvider BibliographyStylesProvider { get; set; }
```

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

* interface [IBibliographyStylesProvider](../../ibibliographystylesprovider/)
* class [FieldOptions](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
