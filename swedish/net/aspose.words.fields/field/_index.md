---
title: Field Class
linktitle: Field
articleTitle: Field
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.Field, din nyckel till att förbättra Microsoft Word-dokument med dynamiska fält för förbättrad funktionalitet och effektivitet.
type: docs
weight: 1920
url: /sv/net/aspose.words.fields/field/
---
## Field class

Representerar ett fält i ett Microsoft Word-dokument.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class Field
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(*bool*) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista undernoden till dess överordnade nod, returneras dess överordnade stycke. Om fältet redan är borttaget returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavkopplingen. |
| [Update](../../aspose.words.fields/field/update/#update)() | Utför fältuppdateringen. Körs om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/#update_1)(*bool*) | Utför en fältuppdatering. Körs om fältet redan uppdateras. |

## Anmärkningar

Ett fält i ett Word-dokument är en komplex struktur som består av flera noder som inkluderar fältstart, fältkod, fältavgränsare, fältresultat och fältslut. Fält kan kapslas, innehålla rikt innehåll och spänna över flera stycken eller avsnitt i ett dokument.`Field` klassen är ett "fasad"-objekt som tillhandahåller egenskaper och metoder som gör det möjligt att arbeta med ett fält som ett enda objekt.

De[`Start`](./start/) ,[`Separator`](./separator/) och[`End`](./end/) Egenskaperna pekar på fältets start-, separator- respektive slutnoder för fältet .

Innehållet mellan fältets början och avgränsare är fältkoden. Innehållet mellan fältavgränsaren och fältets slut är fältresultatet. Fältkoden består vanligtvis av en eller flera [`Run`](../../aspose.words/run/) objekt som anger instruktioner. Bearbetningsapplikationen förväntas exekvera fältkoden för att beräkna fältresultatet.

Processen att beräkna fältresultat kallas fältuppdatering. Aspose.Words kan uppdatera field -resultat för de flesta fälttyper på exakt samma sätt som Microsoft Word gör det. Framför allt kan Aspose.Words beräkna resultat även för de mest komplexa formelfälten. För att beräkna field -resultatet för ett enskilt fält, använd[`Update`](./update/) metod. För att uppdatera fält i hela dokumentet använd[`UpdateFields`](../../aspose.words/document/updatefields/).

Du kan få den oformaterade textversionen av fältkoden med hjälp av[`GetFieldCode`](./getfieldcode/)metod. Du kan hämta och ställa in den oformaterade textversionen av fältresultatet med hjälp av[`Result`](./result/) property. Både fältkoden och fältresultatet kan innehålla komplext innehåll, såsom kapslade fält, stycken, former, tabeller, och i det här fallet kanske du vill arbeta direkt med fältnoderna om du behöver mer kontroll.

Du skapar inte instanser av`Field` klass direkt. För att skapa ett nytt fält, använd[`InsertField`](../../aspose.words/documentbuilder/insertfield/) metod.

## Exempel

Visar hur man infogar ett fält i ett dokument med hjälp av en fältkod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Denna överbelastning av InsertField-metoden uppdaterar automatiskt infogade fält.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### Se även

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
