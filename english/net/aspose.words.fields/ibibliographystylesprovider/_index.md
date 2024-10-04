---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.IBibliographyStylesProvider interface. Implement this interface to provide bibliography style for the FieldBibliography and FieldCitation fields when theyre updated in C#.
type: docs
weight: 2940
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
