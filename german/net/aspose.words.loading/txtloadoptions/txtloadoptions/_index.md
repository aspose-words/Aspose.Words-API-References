---
title: TxtLoadOptions
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie den TxtLoadOptions-Konstruktor! Initialisieren Sie einfach mit Standardwerten und optimieren Sie Ihren Datenladeprozess für eine verbesserte Leistung.
type: docs
weight: 10
url: /de/net/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions constructor

Initialisiert eine neue Instanz dieser Klasse mit Standardwerten.

```csharp
public TxtLoadOptions()
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
