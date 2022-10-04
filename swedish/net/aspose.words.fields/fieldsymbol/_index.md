---
title: FieldSymbol
second_title: Aspose.Words för .NET API Referens
description: Implementerar ett SYMBOLfält.
type: docs
weight: 2310
url: /sv/net/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class

Implementerar ett SYMBOL-fält.

```csharp
public class FieldSymbol : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldSymbol](fieldsymbol/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CharacterCode](../../aspose.words.fields/fieldsymbol/charactercode/) { get; set; } | Hämtar eller ställer in tecknets kodpunktsvärde i decimal eller hexadecimal. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [DontAffectsLineSpacing](../../aspose.words.fields/fieldsymbol/dontaffectslinespacing/) { get; set; } | Hämtar eller ställer in om tecknet som hämtas av fältet påverkar radavståndet i stycket. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [FontName](../../aspose.words.fields/fieldsymbol/fontname/) { get; set; } | Hämtar eller ställer in namnet på teckensnittet för tecknet som hämtas av fältet. |
| [FontSize](../../aspose.words.fields/fieldsymbol/fontsize/) { get; set; } | Hämtar eller ställer in storleken i punkter på teckensnittet för tecknet som hämtas av fältet. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [IsAnsi](../../aspose.words.fields/fieldsymbol/isansi/) { get; set; } | Hämtar eller ställer in om teckenkoden ska tolkas som värdet av ett ANSI-tecken. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [IsShiftJis](../../aspose.words.fields/fieldsymbol/isshiftjis/) { get; set; } | Hämtar eller ställer in om teckenkoden ska tolkas som värdet av ett SHIFT-JIS-tecken. |
| [IsUnicode](../../aspose.words.fields/fieldsymbol/isunicode/) { get; set; } | Hämtar eller ställer in om teckenkoden ska tolkas som värdet av ett Unicode-tecken. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara null. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras **null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Anmärkningar

Hämtar tecknet vars kodpunktsvärde anges i decimal eller hexadecimal.

### Exempel

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

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
