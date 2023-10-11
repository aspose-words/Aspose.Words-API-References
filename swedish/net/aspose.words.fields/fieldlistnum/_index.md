---
title: Class FieldListNum
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fields.FieldListNum klass. Implementerar fältet LISTNUM.
type: docs
weight: 2120
url: /sv/net/aspose.words.fields/fieldlistnum/
---
## FieldListNum class

Implementerar fältet LISTNUM.

För att lära dig mer, besök[Arbeta med Fields](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldListNum : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldListNum](fieldlistnum/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [HasListName](../../aspose.words.fields/fieldlistnum/haslistname/) { get; } | Returnerar ett värde som anger om namnet på en abstrakt numreringsdefinition tillhandahålls av fältets kod. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [ListLevel](../../aspose.words.fields/fieldlistnum/listlevel/) { get; set; } | Hämtar eller ställer in nivån i listan och åsidosätter fältets standardbeteende. |
| [ListName](../../aspose.words.fields/fieldlistnum/listname/) { get; set; } | Hämtar eller ställer in namnet på den abstrakta numreringsdefinitionen som används för numreringen. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| [StartingNumber](../../aspose.words.fields/fieldlistnum/startingnumber/) { get; set; } | Hämtar eller ställer in startvärdet för detta fält. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Exempel

Visar hur man numrerar stycken med LISTNUM-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// LISTNUM-fält visar ett tal som ökar vid varje LISTNUM-fält.
// Dessa fält har också en mängd olika alternativ som gör att vi kan använda dem för att efterlikna numrerade listor.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Listor börjar räknas vid 1 som standard, men vi kan ställa in detta nummer till ett annat värde, till exempel 0.
// Detta fält kommer att visa "0)".
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

 // LISTNUM-fält upprätthåller separata räkningar för varje listnivå.
// Infoga ett LISTNUM-fält i samma stycke som ett annat LISTNUM-fält
// ökar listnivån istället för antalet.
// Nästa fält kommer att fortsätta räkningen vi startade ovan och visa värdet "1" på listnivå 1.
builder.InsertField(FieldType.FieldListNum, true);

// Detta fält kommer att starta en räkning på listnivå 2. Det kommer att visa värdet "1".
builder.InsertField(FieldType.FieldListNum, true);

// Detta fält startar en räkning på listnivå 3. Det kommer att visa värdet "1".
// Olika listnivåer har olika formatering,
// så dessa fält kombinerade kommer att visa värdet "1)a)i)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Nästa LISTNUM-fält som vi infogar fortsätter räkningen på listnivå
// att det tidigare LISTNUM-fältet var på.
// Vi kan använda egenskapen "ListLevel" för att hoppa till en annan listnivå.
// Om detta LISTNUM-fält stannade på listnivå 3, skulle det visa "ii)",
// men eftersom vi har flyttat den till listnivå 2 fortsätter den räkningen på den nivån och visar "b)".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Vi kan ställa in egenskapen ListName för att få fältet att emulera en annan AUTONUM-fälttyp.
// "NumberDefault" emulerar AUTONUM, "OutlineDefault" emulerar AUTONUMOUT,
// och "LegalDefault" emulerar AUTONUMLGL-fält.
// Listnamnet "OutlineDefault" med 1 som startnummer kommer att resultera i att "I." visas.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// Listnamnet överförs inte från föregående fält, så vi måste ställa in det för varje nytt fält.
// Detta fält fortsätter räkningen med det olika listnamnet och visar "II.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)


