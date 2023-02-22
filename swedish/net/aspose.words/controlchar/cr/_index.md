---
title: ControlChar.Cr
second_title: Aspose.Words för .NET API Referens
description: ControlChar fält. Vagnreturtecken x000d eller r. Samma somParagraphBreak .
type: docs
weight: 50
url: /sv/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

Vagnreturtecken: "\x000d" eller "\r". Samma som[`ParagraphBreak`](../paragraphbreak/) .

```csharp
public static readonly string Cr;
```

### Exempel

Visar hur man använder kontrolltecken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga stycken med text med DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Konvertering av dokumentet till textform avslöjar att kontrolltecken
// representerar några av dokumentets strukturella element, såsom sidbrytningar.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// När du konverterar ett dokument till strängform,
// vi kan utelämna några av kontrolltecknen med Trim-metoden.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Se även

* class [ControlChar](../)
* namnutrymme [Aspose.Words](../../controlchar/)
* hopsättning [Aspose.Words](../../../)


