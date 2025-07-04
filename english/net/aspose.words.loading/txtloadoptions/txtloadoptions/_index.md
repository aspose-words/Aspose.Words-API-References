---
title: TxtLoadOptions
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words for .NET
description: Discover the TxtLoadOptions constructor! Easily initialize with default values and streamline your data loading process for enhanced performance.
type: docs
weight: 10
url: /net/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions constructor

Initializes a new instance of this class with default values.

```csharp
public TxtLoadOptions()
```

## Examples

Shows how to read and display hyperlinks.

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n";

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // Load document with hyperlinks.
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    // Print hyperlinks text.
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.That("https://www.aspose.com/", Is.EqualTo(doc.Range.Fields[0].Result.Trim()));
    Assert.That("https://docs.aspose.com/words/net/", Is.EqualTo(doc.Range.Fields[1].Result.Trim()));
}
```

### See Also

* class [TxtLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
