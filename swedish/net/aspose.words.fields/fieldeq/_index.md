---
title: FieldEQ Class
linktitle: FieldEQ
articleTitle: FieldEQ
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldEQ för sömlös implementering av EQ-fält. Förbättra dokumentautomationen med kraftfulla funktioner och flexibilitet.
type: docs
weight: 2240
url: /sv/net/aspose.words.fields/fieldeq/
---
## FieldEQ class

Implementerar EQ-fältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldEQ : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldEQ](fieldeq/)() | Default_Constructor |

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
| [AsOfficeMath](../../aspose.words.fields/fieldeq/asofficemath/)() | Returnerar Office Math-objektet som motsvarade EQ-fältet. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista undernoden till dess överordnade nod, returneras dess överordnade stycke. Om fältet redan är borttaget returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavkopplingen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Körs om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Utför en fältuppdatering. Körs om fältet redan uppdateras. |

## Exempel

Visar hur man ersätter EQ-fältet med Office Math.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

Visar hur man använder EQ-fältet för att visa en mängd olika matematiska ekvationer.

```csharp
public void FieldEQ()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Ett EQ-fält visar en matematisk ekvation som består av ett eller flera element.
    // Varje element har följande form: [switch][options][arguments].
    // Det kan finnas en brytare och flera möjliga alternativ.
    // Argumenten är en uppsättning kommaseparerade värden omgivna av klammerparenteser.

    // Här använder vi en dokumentbyggare för att infoga ett EQ-fält, med en "\f"-växel, vilket motsvarar "Bråk".
    // Vi skickar värdena 1 och 4 som argument, och vi använder inga alternativ.
    // Det här fältet visar ett bråk med 1 som täljare och 4 som nämnare.
    FieldEQ field = InsertFieldEQ(builder, @"\f(1,4)");

    Assert.AreEqual(@" EQ \f(1,4)", field.GetFieldCode());

    // Ett EQ-fält kan innehålla flera element placerade i följd.
    // Vi kan också nästla element inuti varandra genom att placera de inre elementen
    // innanför argumentparenteserna för yttre element.
    // Vi hittar hela listan över switchar, tillsammans med deras användningsområden, här:
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

     // Nedan följer tillämpningar av nio olika EQ-fältomkopplare som vi kan använda för att skapa olika typer av objekt.
    // 1 - Array-växel "\a", vänsterjusterad, 2 kolumner, 3 punkter med horisontellt och vertikalt avstånd:
    InsertFieldEQ(builder, @"\a \al \co2 \vs3 \hs3(4x,- 4y,-4x,+ y)");

    // 2 - Hakparentesbrytare "\b", hakparentes tecken "[", för att omsluta innehållet inom en uppsättning hakparenteser:
    // Observera att vi kapslar en array inom parenteserna, vilket sammantaget kommer att se ut som en matris i utdata.
    InsertFieldEQ(builder, @"\b \bc\[ (\a \al \co3 \vs3 \hs3(1,0,0,0,1,0,0,0,1))");

    // 3 - Förskjutningsbrytaren "\d", förskjuter texten "B" 30 mellanslag till höger om "A", visar mellanrummet som en understrykning:
    InsertFieldEQ(builder, @"A \d \fo30 \li() B");

    // 4 - Formel bestående av flera bråk:
    InsertFieldEQ(builder, @"\f(d,dx)(u + v) = \f(du,dx) + \f(dv,dx)");

    // 5 - Integralomkopplare "\i", med en summeringssymbol:
    InsertFieldEQ(builder, @"\i \su(n=1,5,n)");

    // 6 - Listväxel "\l":
    InsertFieldEQ(builder, @"\l(1,1,2,3,n,8,13)");

    // 7 - Radikalbrytaren "\r", som visar en kubikrot av x:
    InsertFieldEQ(builder, @"\r (3,x)");

    // 8 - Växla mellan subskript/superskript "/s", först som superskript och sedan som subskript:
    InsertFieldEQ(builder, @"\s \up8(Superscript) Text \s \do8(Subscript)");

    // 9 - Boxväxel "\x", med linjer högst upp, längst ner, till vänster och höger om ingången:
    InsertFieldEQ(builder, @"\x \to \bo \le \ri(5)");

    // Några mer komplexa kombinationer.
    InsertFieldEQ(builder, @"\a \ac \vs1 \co1(lim,n→∞) \b (\f(n,n2 + 12) + \f(n,n2 + 22) + ... + \f(n,n2 + n2))");
    InsertFieldEQ(builder, @"\i (,,  \b(\f(x,x2 + 3x + 2))) \s \up10(2)");
    InsertFieldEQ(builder, @"\i \in( tan x, \s \up2(sec x), \b(\r(3) )\s \up4(t) \s \up7(2)  dt)");

    doc.Save(ArtifactsDir + "Field.EQ.docx");
}

/// <summary>
/// Använd en dokumentbyggare för att infoga ett EQ-fält, ange dess argument och börja ett nytt stycke.
/// </summary>
private static FieldEQ InsertFieldEQ(DocumentBuilder builder, string args)
{
    FieldEQ field = (FieldEQ)builder.InsertField(FieldType.FieldEquation, true);
    builder.MoveTo(field.Separator);
    builder.Write(args);
    builder.MoveTo(field.Start.ParentNode);

    builder.InsertParagraph();
    return field;
}
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
