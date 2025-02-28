---
title: LoadOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words for .NET
description: Discover the LoadOptions Encoding property to easily manage HTML TXT or CHM document encoding. Customize your content loading for optimal performance!
type: docs
weight: 50
url: /net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be `null`. Default is `null`.

```csharp
public Encoding Encoding { get; set; }
```

## Remarks

This property is used only when loading HTML, TXT, or CHM documents.

If encoding is not specified inside the document and this property is `null`, then the system will try to automatically detect the encoding.

## Examples

Shows how to set the encoding with which to open a document.

```csharp
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.ASCII
};

// Load the document while passing the LoadOptions object, then verify the document's contents.
Document doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.True(doc.ToString(SaveFormat.Text).Contains("This is a sample text in English."));
```

### See Also

* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
