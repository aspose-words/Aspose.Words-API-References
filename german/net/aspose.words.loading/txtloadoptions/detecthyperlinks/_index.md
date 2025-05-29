---
title: TxtLoadOptions.DetectHyperlinks
linktitle: DetectHyperlinks
articleTitle: DetectHyperlinks
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die DetectHyperlinks-Eigenschaft von TxtLoadOptions die Textverarbeitung durch die Erkennung von Hyperlinks verbessert und so die Datengenauigkeit steigert. Der Standardwert ist „false“.
type: docs
weight: 30
url: /de/net/aspose.words.loading/txtloadoptions/detecthyperlinks/
---
## TxtLoadOptions.DetectHyperlinks property

Gibt an, ob Hyperlinks im Text erkannt werden sollen. Der Standardwert ist`FALSCH` .

```csharp
public bool DetectHyperlinks { get; set; }
```

## Beispiele

Zeigt, wie Hyperlinks gelesen und angezeigt werden.

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n";

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // Dokument mit Hyperlinks laden.
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    // Hyperlinktext drucken.
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/");
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/");
}
```

### Siehe auch

* class [TxtLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
