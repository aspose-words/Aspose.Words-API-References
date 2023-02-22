---
title: Class Field
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fields.Field klass. Representerar ett Microsoft Worddokumentfält.
type: docs
weight: 1360
url: /sv/net/aspose.words.fields/field/
---
## Field class

Representerar ett Microsoft Word-dokumentfält.

```csharp
public class Field
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara null. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras **null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update/#update)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/#update_1)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Anmärkningar

Ett fält i ett Word-dokument är en komplex struktur som består av flera noder som inkluderar fältstart, fältkod, fältseparator, fältresultat och fältslut. Fält kan kapslas, innehålla rikt innehåll och span flera stycken eller avsnitt i ett dokument. De`Field`class är ett "fasad"-objekt som ger egenskaper och metoder som gör det möjligt att arbeta med ett fält som ett enda objekt.

De[`Start`](./start/) ,[`Separator`](./separator/) och[`End`](./end/) egenskaper pekar på fältets start-, separator- och slutnod för fältet.

Innehållet mellan fältstart och separator är fältkoden. Innehållet mellan fältavgränsaren och fältslutet är fältresultatet. Fältkoden består vanligtvis av en eller flera [`Run`](../../aspose.words/run/) objekt som anger instruktioner. Bearbetningsapplikationen förväntas exekvera fältkoden för att beräkna fältresultatet.

Processen att beräkna fältresultat kallas fältuppdatering. Aspose.Words kan uppdatera field resultat för de flesta fälttyper på exakt samma sätt som Microsoft Word gör det. Framför allt kan Aspose.Words beräkna resultaten av även de mest komplexa formelfälten. För att beräkna field -resultatet för ett enskilt fält använd[`Update`](./update/) metod. För att uppdatera fält i hela document använd[`UpdateFields`](../../aspose.words/document/updatefields/).

Du kan få en vanlig textversion av fältkoden med hjälp av[`GetFieldCode`](./getfieldcode/) method. Du kan hämta och ställa in oformaterad textversion av fältresultatet med hjälp av[`Result`](./result/) property. Både fältkoden och fältresultatet kan innehålla komplext innehåll, såsom kapslade fält, stycken, former, tabeller och i det här fallet kanske du vill arbeta med fältnoderna direkt om du behöver mer kontroll.

Du skapar inte instanser av`Field` class direct. För att skapa ett nytt fält använd[`InsertField`](../../aspose.words/documentbuilder/insertfield/) metod.

### Exempel

Visar hur man infogar ett fält i ett dokument med hjälp av en fältkod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Denna överbelastning av InsertField-metoden uppdaterar automatiskt infogade fält.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### Se även

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)


