---
title: FieldOptions.BibliographyStylesProvider
linktitle: BibliographyStylesProvider
articleTitle: BibliographyStylesProvider
second_title: Aspose.Words for .NET
description: Discover the FieldOptions BibliographyStylesProvider property for customizable bibliography styles, enhancing your FieldBibliography and FieldCitation fields.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldoptions/bibliographystylesprovider/
---
## FieldOptions.BibliographyStylesProvider property

Gets or sets a provider that returns a bibliography style for the [`FieldBibliography`](../../fieldbibliography/) and [`FieldCitation`](../../fieldcitation/) fields.

```csharp
public IBibliographyStylesProvider BibliographyStylesProvider { get; set; }
```

## Examples

Shows how to override built-in styles or provide custom one.

```csharp
public void ChangeBibliographyStyles()
{
    Document doc = new Document(MyDir + "Bibliography.docx");

    // If the document already has a style you can change it with the following code:
    // doc.Bibliography.BibliographyStyle = "Bibliography custom style.xsl";

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

### See Also

* interface [IBibliographyStylesProvider](../../ibibliographystylesprovider/)
* class [FieldOptions](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
