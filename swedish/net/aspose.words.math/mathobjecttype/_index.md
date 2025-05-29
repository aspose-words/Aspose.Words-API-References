---
title: MathObjectType Enum
linktitle: MathObjectType
articleTitle: MathObjectType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Math.MathObjectType-enum för att enkelt identifiera och hantera Office Math-objekttyper för förbättrad dokumentbehandling.
type: docs
weight: 4800
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
| OMath | `0` | Instans av matematisk text. |
| OMathPara | `1` | Matematikstycke, eller visningsmattezon, som innehåller en eller fleraOMath element som är i visningsläge. |
| Accent | `2` | Accentfunktion, bestående av en bas och ett kombinerande diakritiskt tecken. |
| Bar | `3` | Stapelfunktion, bestående av ett basargument och ett över- eller understreck. |
| BorderBox | `4` | Border Box-objekt, bestående av en kantlinje ritad runt en förekomst av matematisk text (såsom en formel eller ekvation) |
| Box | `5` | Boxobjekt, som används för att gruppera komponenter i en ekvation eller annan instans av matematisk text. |
| Delimiter | `6` | Avgränsningsteckenobjekt, bestående av inledande och avslutande avgränsare (såsom parenteser, klammerparenteser, hakparenteser och vertikala streck), och ett element inuti. |
| Degree | `7` | Grad i den matematiska radikalen. |
| Argument | `8` | Argumentobjekt. Omsluter Office Math-entiteter när de används som argument till andra Office Math-entiteter. |
| Array | `9` | Arrayobjekt, bestående av en eller flera ekvationer, uttryck eller andra matematiska textkörningar som kan justeras vertikalt som en enhet i förhållande till omgivande text på raden. |
| Fraction | `10` | Bråkobjekt, bestående av en täljare och nämnare separerade med en bråkstreck. |
| Denominator | `11` | Nämnaren i ett bråkobjekt. |
| Numerator | `12` | Täljare för bråkobjektet. |
| Function | `13` | Function-Apply-objekt, som består av ett funktionsnamn och ett argumentelement som påverkas. |
| FunctionName | `14` | Funktionens namn. Till exempel är funktionsnamn sin och cos. |
| GroupCharacter | `15` | Grupp-Teckenobjekt, bestående av ett tecken ritat ovanför eller under text, ofta i syfte att visuellt gruppera objekt |
| Limit | `16` | Nedre gräns förLowerLimit objektet och den övre gränsen förUpperLimit funktion. |
| LowerLimit | `17` | Nedre gränsobjekt, bestående av text på baslinjen och förminskad text omedelbart under den. |
| UpperLimit | `18` | Övre gränsobjekt, bestående av text på baslinjen och förminskad text omedelbart ovanför den. |
| Matrix | `19` | Matrisobjekt, bestående av ett eller flera element utplacerade i en eller flera rader och en eller flera kolumner. |
| MatrixRow | `20` | En rad i matrisen. |
| NAry | `21` | N-ärt objekt, bestående av ett n-ärt objekt, en bas (eller operand) och valfria övre och undre gränser. |
| Phantom | `22` | Fantomobjekt. |
| Radical | `23` | Radikalobjekt, bestående av en radikal, ett baselement och en valfri grad . |
| SubscriptPart | `24` | Subskript för objektet som kan ha en subskriptdel. |
| SuperscriptPart | `25` | Upphöjd skrift för det upphöjda objektet. |
| PreSubSuperscript | `26` | Pre-Sub-Superscript-objekt, som består av ett baselement och ett subscript och ett superscript placerade till vänster om basen. |
| Subscript | `27` | Subscript-objekt, som består av ett baselement och ett skript i reducerad storlek placerat nedanför och till höger. |
| SubSuperscript | `28` | Sub-superscript-objekt, som består av ett baselement, ett skript med reducerad storlek placerat nedanför och till höger, och ett skript med reducerad storlek placerat ovanför och till höger. |
| Supercript | `29` | Superscript-objekt, som består av ett baselement och ett förminskat skript placerat ovanför och till höger. |

## Exempel

Visar hur man skriver ut nodstrukturen för varje kontorsmatematiknod i ett dokument.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // När vi får en sammansatt nod att acceptera en dokumentbesökare, besöker besökaren den accepterande noden,
    // och sedan korsar alla nodens barn på ett djup-först-sätt.
    // Besökaren kan läsa och ändra varje besökt nod.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Går igenom en nods icke-binära träd av undernoder.
/// Skapar en karta i form av en sträng av alla påträffade OfficeMath-noder och deras undernoder.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// Hämtar klartexten från dokumentet som besökaren samlade in.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Anropas när en Run-nod påträffas i dokumentet.
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
    /// Anropas efter att alla undernoder till en OfficeMath-nod har besökts.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Lägg till en rad i StringBuilder och dra in den beroende på hur djupt inne i dokumentträdet besökaren befinner sig.
    /// </summary>
    /// <param namn="text"></param>
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
