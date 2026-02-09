---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: Aspose.Words for .NET
description: Enhance your document formatting with the Aspose.Words.IBibliographyStylesProvider interface, perfect for customizing bibliography styles in citations.
type: docs
weight: 3080
url: /net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

Implement this interface to provide bibliography style for the [`FieldBibliography`](../fieldbibliography/) and [`FieldCitation`](../fieldcitation/) fields when they're updated.

```csharp
public interface IBibliographyStylesProvider
```

## Methods

| Name | Description |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(*string*) | Returns bibliography style. |

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

* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
