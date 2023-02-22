---
title: Enum MathObjectType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Math.MathObjectType uppräkning. Anger typen av ett Office Mathobjekt.
type: docs
weight: 3870
url: /sv/net/aspose.words.math/mathobjecttype/
---
## MathObjectType enumeration

Anger typen av ett Office Math-objekt.

```csharp
public enum MathObjectType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| OMath | `0` | Förekomst av matematisk text. |
| OMathPara | `1` | Matematisk stycke, eller visa matematikzon, som innehåller en eller fleraOMath element som är i visningsläge. |
| Accent | `2` | Accentfunktion, bestående av en bas och ett kombinerat diakritiskt tecken. |
| Bar | `3` | Bar funktion, bestående av ett basargument och en överstreck eller understreck. |
| BorderBox | `4` | Border Box-objekt, som består av en ram som ritas runt en instans av matematisk text (som en formel eller ekvation) |
| Box | `5` | Box-objekt, som används för att gruppera komponenter i en ekvation eller annan instans av matematisk text. |
| Delimiter | `6` | Avgränsningsobjekt, bestående av öppnande och stängda avgränsare (som parenteser, parenteser, parenteser och vertikala streck) och ett element inuti. |
| Degree | `7` | Examen i den matematiska radikalen. |
| Argument | `8` | Argumentobjekt. Omger Office Math-entiteter när de används som argument till andra Office Math-entiteter. |
| Array | `9` | Arrayobjekt som består av en eller flera ekvationer, uttryck eller annan matematisk text körs som kan justeras vertikalt som en enhet med avseende på omgivande text på raden. |
| Fraction | `10` | Bråkobjekt, bestående av en täljare och nämnare separerade av en bråkstapel. |
| Denominator | `11` | Nämnare för ett bråkobjekt. |
| Numerator | `12` | Täljare för bråkobjektet. |
| Function | `13` | Function-Apply-objekt, som består av ett funktionsnamn och ett argumentelement som åtgärdas. |
| FunctionName | `14` | Namn på funktionen. Funktionsnamn är till exempel sin och cos. |
| GroupCharacter | `15` | Grupp-teckenobjekt, som består av ett tecken ritat över eller under text, ofta i syfte att visuellt gruppera objekt |
| Limit | `16` | Nedre gräns förLowerLimit objekt och den övre gränsen förUpperLimit function. |
| LowerLimit | `17` | Lower-Limit-objekt, bestående av text på baslinjen och förminskad text omedelbart under det. |
| UpperLimit | `18` | Upper-Limit-objekt, bestående av text på baslinjen och förminskad text omedelbart ovanför det. |
| Matrix | `19` | Matrisobjekt, bestående av ett eller flera element utlagda i en eller flera rader och en eller flera kolumner. |
| MatrixRow | `20` | Enkel rad i matrisen. |
| NAry | `21` | N-ärt objekt, bestående av ett n-ärt objekt, en bas (eller operand) och valfria övre och nedre gränser. |
| Phantom | `22` | Fantomobjekt. |
| Radical | `23` | Radikalt objekt, bestående av en radikal, ett baselement och en valfri grad . |
| SubscriptPart | `24` | Subscript för objektet som kan ha subscript del. |
| SuperscriptPart | `25` | Upphöjd skrift för objektet upphöjd. |
| PreSubSuperscript | `26` | Pre-Sub-Superscript-objekt, som består av ett baselement och en subscript och superscript placerad till vänster om basen. |
| Subscript | `27` | Subscript-objekt, som består av ett baselement och ett förminskat skript placerat under och till höger. |
| SubSuperscript | `28` | Sub-superscript-objekt, som består av ett baselement, ett reducerat skript placerat under och till höger, och ett reducerat skript placerat ovanför och till höger. |
| Supercript | `29` | Superscript-objekt, som består av ett baselement och ett skript i förminskad storlek placerat ovanför och till höger. |

### Exempel

Visar hur man skriver ut nodstrukturen för varje kontors matematisk nod i ett dokument.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // När vi får en sammansatt nod att acceptera en dokumentbesökare, besöker besökaren den accepterande noden,
    // och sedan korsar alla nodens barn på ett djup-först sätt.
    // Besökaren kan läsa och ändra varje besökt nod.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Går igenom en nods icke-binära träd av underordnade noder.
/// Skapar en karta i form av en sträng av alla påträffade OfficeMath-noder och deras barn.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// Hämtar vanlig text av dokumentet som samlades av besökaren.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Anropas när en körnod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en OfficeMath-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas efter att alla undernoder i en OfficeMath-nod har besökts.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Lägg till en rad i StringBuilder och dra in den beroende på hur djupt besökaren befinner sig i dokumentträdet.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideOfficeMath;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Se även

* namnutrymme [Aspose.Words.Math](../../aspose.words.math/)
* hopsättning [Aspose.Words](../../)


