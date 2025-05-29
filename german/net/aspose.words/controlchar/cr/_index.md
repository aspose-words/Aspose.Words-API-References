---
title: ControlChar.Cr
linktitle: Cr
articleTitle: Cr
second_title: Aspose.Words für .NET
description: Entdecken Sie ControlChar Cr, das Wagenrücklaufzeichen (x000d oder r), das die Textformatierung verbessert. Vereinfachen Sie Ihre Programmierung mit unseren einzigartigen Lösungen!
type: docs
weight: 50
url: /de/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

Wagenrücklaufzeichen: "\x000d" oder "\r". Dasselbe wie[`ParagraphBreak`](../paragraphbreak/) .

```csharp
public static readonly string Cr;
```

## Beispiele

Zeigt, wie Steuerzeichen verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie mit DocumentBuilder Absätze mit Text ein.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Die Konvertierung des Dokuments in Textform zeigt, dass Steuerzeichen
// stellen einige Strukturelemente des Dokuments dar, beispielsweise Seitenumbrüche.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Beim Konvertieren eines Dokuments in die Zeichenfolgenform,
// Wir können einige der Steuerzeichen mit der Trim-Methode weglassen.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Siehe auch

* class [ControlChar](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
