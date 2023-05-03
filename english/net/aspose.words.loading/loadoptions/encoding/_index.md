---
title: LoadOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words for .NET API Reference
description: LoadOptions Encoding property. Gets or sets the encoding that will be used to load an HTML TXT or CHM document if the encoding is not specified inside the document. Can be null. Default is null in C#.
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
// A FileFormatInfo object will detect this file as being encoded in something other than UTF-7.
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Encoded in UTF-7.txt");

Assert.AreNotEqual(Encoding.UTF7, fileFormatInfo.Encoding);

// If we load the document with no loading configurations, Aspose.Words will detect its encoding as UTF-8.
Document doc = new Document(MyDir + "Encoded in UTF-7.txt");

// The contents, parsed in UTF-8, create a valid string.
// However, knowing that the file is in UTF-7, we can see that the result is incorrect.
Assert.AreEqual("Hello world+ACE-", doc.ToString(SaveFormat.Text).Trim());

// In cases of ambiguous encoding such as this one, we can set a specific encoding variant
// to parse the file within a LoadOptions object.
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.UTF7
};

// Load the document while passing the LoadOptions object, then verify the document's contents.
doc = new Document(MyDir + "Encoded in UTF-7.txt", loadOptions);

Assert.AreEqual("Hello world!", doc.ToString(SaveFormat.Text).Trim());
```

### See Also

* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../loadoptions/)
* assembly [Aspose.Words](../../../)
