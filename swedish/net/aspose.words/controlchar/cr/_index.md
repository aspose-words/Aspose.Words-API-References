---
title: ControlChar.Cr
linktitle: Cr
articleTitle: Cr
second_title: Aspose.Words för .NET
description: Upptäck ControlChar Cr, vagnreturtecknet (x000d eller r) som förbättrar textformatering. Förenkla din kodning med våra unika lösningar!
type: docs
weight: 50
url: /sv/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

Vagnreturtecken: "\x000d" eller "\r". Samma som[`ParagraphBreak`](../paragraphbreak/) .

```csharp
public static readonly string Cr;
```

## Exempel

Visar hur man använder kontrolltecken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga stycken med text med DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Att konvertera dokumentet till textformat visar att kontrolltecknen
// representerar några av dokumentets strukturella element, såsom sidbrytningar.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// När man konverterar ett dokument till strängformat,
// vi kan utelämna några av kontrolltecknen med Trim-metoden.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Se även

* class [ControlChar](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
