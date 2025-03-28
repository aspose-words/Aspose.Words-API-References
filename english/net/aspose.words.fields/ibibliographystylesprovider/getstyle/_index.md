---
title: IBibliographyStylesProvider.GetStyle
linktitle: GetStyle
articleTitle: GetStyle
second_title: Aspose.Words for .NET
description: Discover the IBibliographyStylesProvider GetStyle method to effortlessly retrieve and customize your bibliography styles for enhanced academic writing.
type: docs
weight: 10
url: /net/aspose.words.fields/ibibliographystylesprovider/getstyle/
---
## IBibliographyStylesProvider.GetStyle method

Returns bibliography style.

```csharp
public Stream GetStyle(string styleFileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| styleFileName | String | The bibliography style file name. |

### Return Value

The Stream with bibliography style XSLT stylesheet.

## Remarks

The implementation should return `null` to indicate that the MS Word version of specified style should be used.

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

* interface [IBibliographyStylesProvider](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
