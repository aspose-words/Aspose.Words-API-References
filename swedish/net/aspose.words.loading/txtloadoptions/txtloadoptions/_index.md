---
title: TxtLoadOptions
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words för .NET
description: Upptäck TxtLoadOptions-konstruktorn! Initiera enkelt med standardvärden och effektivisera din datainläsningsprocess för förbättrad prestanda.
type: docs
weight: 10
url: /sv/net/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions constructor

Initierar en ny instans av den här klassen med standardvärden.

```csharp
public TxtLoadOptions()
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
