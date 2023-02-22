---
title: Class FieldGreetingLine
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fields.FieldGreetingLine klass. Implementerar fältet GREETINGLINE.
type: docs
weight: 1830
url: /sv/net/aspose.words.fields/fieldgreetingline/
---
## FieldGreetingLine class

Implementerar fältet GREETINGLINE.

```csharp
public class FieldGreetingLine : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldGreetingLine](fieldgreetingline/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AlternateText](../../aspose.words.fields/fieldgreetingline/alternatetext/) { get; set; } | Hämtar eller ställer in texten att inkludera i fältet om namnet är tomt. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LanguageId](../../aspose.words.fields/fieldgreetingline/languageid/) { get; set; } | Hämtar eller ställer in språk-id som används för att formatera namnet. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [NameFormat](../../aspose.words.fields/fieldgreetingline/nameformat/) { get; set; } | Hämtar eller ställer in formatet för namnet som ingår i fältet. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara null. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [GetFieldNames](../../aspose.words.fields/fieldgreetingline/getfieldnames/)() | Returnerar en samling av kopplingsfältnamn som används av fältet. |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras **null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Anmärkningar

Infogar en kopplingshälsningsrad.

### Exempel

Visar hur man infogar ett HÄLSNINGSLINJE-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en allmän hälsning med ett HÄLSNINGSLINJE-fält och lite text efter det.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// Ett GREETINGLINE-fält accepterar värden från en datakälla under en e-postkoppling, som ett MERGEFIELD.
// Det kan också formatera hur källans data skrivs på sin plats när sammanslagningen är klar.
// Fältnamnssamlingen motsvarar kolumnerna från datakällan
// som fältet kommer att ta värden från.
Assert.AreEqual(0, field.GetFieldNames().Length);

// För att fylla den arrayen måste vi ange ett format för vår hälsningsrad.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// Nu kommer vårt fält att acceptera värden från dessa två kolumner i datakällan.
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// Denna sträng kommer att täcka alla fall där datatabellsdata är ogiltiga
// genom att ersätta det felaktiga namnet med en sträng.
field.AlternateText = "Sir or Madam";

// Ställ in ett språk för att formatera resultatet.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// Skapa en datatabell med kolumner vars namn matchar element
// från fältets samling av fältnamn och utför sedan brevkopplingen.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Den här raden har ett ogiltigt värde i kolumnen Courtesy Title, så vår hälsning kommer som standard till den alternativa texten.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.That(doc.Range.Fields, Is.Empty);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)


