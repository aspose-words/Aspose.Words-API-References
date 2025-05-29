---
title: TxtLoadOptions.DetectHyperlinks
linktitle: DetectHyperlinks
articleTitle: DetectHyperlinks
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen DetectHyperlinks i TxtLoadOptions förbättrar textbehandling genom att upptäcka hyperlänkar, vilket förbättrar datanoggrannheten. Standardvärdet är falskt.
type: docs
weight: 30
url: /sv/net/aspose.words.loading/txtloadoptions/detecthyperlinks/
---
## TxtLoadOptions.DetectHyperlinks property

Anger att antingen hyperlänkar i text ska detekteras. Standardvärdet är`falsk` .

```csharp
public bool DetectHyperlinks { get; set; }
```

## Exempel

Visar hur man läser och visar hyperlänkar.

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n";

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // Ladda dokument med hyperlänkar.
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    // Skriv ut hyperlänkstext.
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/");
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/");
}
```

### Se även

* class [TxtLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
