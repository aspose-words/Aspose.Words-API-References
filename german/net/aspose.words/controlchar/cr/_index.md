---
title: ControlChar.Cr
linktitle: Cr
articleTitle: Cr
second_title: Aspose.Words für .NET
description: ControlChar Cr veld. Wagenrücklaufzeichen x000d oder r. Gleich wieParagraphBreak  in C#.
type: docs
weight: 50
url: /de/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

Wagenrücklaufzeichen: „\x000d“ oder „\r“. Gleich wie[`ParagraphBreak`](../paragraphbreak/) .

```csharp
public static readonly string Cr;
```

## Beispiele

Zeigt, wie Steuerzeichen verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Mit DocumentBuilder Absätze mit Text einfügen.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Beim Konvertieren des Dokuments in Textform werden die Steuerzeichen sichtbar
// stellen einige der Strukturelemente des Dokuments dar, z. B. Seitenumbrüche.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Beim Konvertieren eines Dokuments in String-Form,
// Mit der Trim-Methode können wir einige Steuerzeichen weglassen.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Siehe auch

* class [ControlChar](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
