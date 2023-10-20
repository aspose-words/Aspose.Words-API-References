---
title: FieldSymbol.IsAnsi
linktitle: IsAnsi
articleTitle: IsAnsi
second_title: Aspose.Words för .NET
description: FieldSymbol IsAnsi fast egendom. Hämtar eller ställer in om teckenkoden ska tolkas som värdet av ett ANSItecken i C#.
type: docs
weight: 60
url: /sv/net/aspose.words.fields/fieldsymbol/isansi/
---
## FieldSymbol.IsAnsi property

Hämtar eller ställer in om teckenkoden ska tolkas som värdet av ett ANSI-tecken.

```csharp
public bool IsAnsi { get; set; }
```

## Exempel

Visar hur man använder SYMBOL-fältet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan finns tre sätt att använda ett SYMBOL-fält för att visa ett enstaka tecken.
// 1 - Lägg till ett SYMBOL-fält som visar © (Copyright)-symbolen, specificerad av en ANSI-teckenkod:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// ANSI-teckenkoden "U+00A9", eller "169" i heltalsform, är reserverad för copyright-symbolen.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - Lägg till ett SYMBOL-fält som visar symbolen ∞ (oändlighet) och ändra dess utseende:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// I Unicode upptar oändlighetssymbolen "221E"-koden.
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// Ändra teckensnittet för vår symbol efter att ha använt Windows Teckenkarta
// för att säkerställa att teckensnittet kan representera den symbolen.
field.FontName = "Calibri";
field.FontSize = "24";

// Vi kan ställa in den här flaggan för höga symboler så att de inte trycker ner resten av texten på sin rad.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - Lägg till ett SYMBOL-fält som visar tecknet あ,
// med ett teckensnitt som stöder Shift-JIS (Windows-932) teckentabell:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);
field.FontName = "MS Gothic";
field.CharacterCode = 0x82A0.ToString();
field.IsShiftJis = true;

Assert.AreEqual(" SYMBOL  33440 \\f \"MS Gothic\" \\j", field.GetFieldCode());

builder.Write("Line 3");

doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### Se även

* class [FieldSymbol](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
