---
title: ControlChar.Cr
second_title: Aspose.Words für .NET-API-Referenz
description: ControlChar veld. Wagenrücklaufzeichen x000d oder r. Gleich wieParagraphBreak .
type: docs
weight: 50
url: /de/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

Wagenrücklaufzeichen: "\x000d" oder "\r". Gleich wie[`ParagraphBreak`](../paragraphbreak/) .

```csharp
public static readonly string Cr;
```

### Beispiele

Zeigt, wie Steuerzeichen verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Absätze mit Text mit DocumentBuilder einfügen.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Das Konvertieren des Dokuments in Textform zeigt diese Steuerzeichen
// stellen einige der Strukturelemente des Dokuments dar, wie z. B. Seitenumbrüche.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Beim Konvertieren eines Dokuments in eine Zeichenkette,
// Mit der Trim-Methode können wir einige der Steuerzeichen weglassen.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Siehe auch

* class [ControlChar](../)
* namensraum [Aspose.Words](../../controlchar/)
* Montage [Aspose.Words](../../../)


