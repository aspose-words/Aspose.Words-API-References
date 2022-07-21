---
title: LayoutEnumerator
second_title: Aspose.Words för .NET API Referens
description: Räknar upp sidlayoutenheter för ett dokument. Du kan använda den här klassen för att gå över sidlayoutmodellen. Tillgängliga egenskaper är typ geometri text och sidindex där entitet renderas samt övergripande struktur och relationer. Använd kombination avGetEntity./layoutcollector/getentity ochCurrent./layoutenumerator/current flytta till den enhet som motsvarar en dokumentnod.
type: docs
weight: 3140
url: /sv/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

Räknar upp sidlayoutenheter för ett dokument. Du kan använda den här klassen för att gå över sidlayoutmodellen. Tillgängliga egenskaper är typ, geometri, text och sidindex där entitet renderas, samt övergripande struktur och relationer. Använd kombination av[`GetEntity`](../layoutcollector/getentity) och[`Current`](./current) flytta till den enhet som motsvarar en dokumentnod.

```csharp
public class LayoutEnumerator
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [LayoutEnumerator](layoutenumerator)(Document) | Initierar ny instans av denna klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Current](../../aspose.words.layout/layoutenumerator/current) { get; set; } | Hämtar eller ställer in aktuell position i sidlayoutmodellen. Denna egenskap returnerar ett ogenomskinligt objekt som motsvarar den aktuella layoutentiteten. |
| [Document](../../aspose.words.layout/layoutenumerator/document) { get; } | Hämtar dokument som denna instans räknar upp. |
| [Kind](../../aspose.words.layout/layoutenumerator/kind) { get; } | Hämtar typen av den aktuella enheten. Detta kan vara en tom sträng men aldrig null. |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex) { get; } | Hämtar det 1-baserade indexet för en sida som innehåller den aktuella enheten. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle) { get; } | Returnerar den avgränsande rektangeln för den aktuella enheten i förhållande till sidans övre vänstra hörn (i punkter). |
| [Text](../../aspose.words.layout/layoutenumerator/text) { get; } | Hämtar text från den aktuella span-entiteten. Kaster för andra entitetstyper. |
| [Type](../../aspose.words.layout/layoutenumerator/type) { get; } | Hämtar typen av den aktuella enheten. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild)() | Flyttar till den första underordnade enheten. |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild)() | Flyttar till den sista underordnade enheten. |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext)() | Flyttar till nästa syskonenhet i visuell ordning. När rader i ett stycke uppdelade över sidor itereras kommer denna metod inte att flytta till nästa sida utan istället flyttas till nästa enhet på samma sida. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical)() | Flyttar till nästa syskonentitet i en logisk ordning. När man itererar rader i ett stycke uppdelade över sidor kommer denna metod att flyttas till nästa rad även om den finns på en annan sida. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent#moveparent)() | Flyttar till den överordnade enheten. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent#moveparent_1)(LayoutEntityType) | Flyttar till den överordnade entiteten av den angivna typen. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious)() | Flyttar till föregående syskonenhet. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical)() | Flyttar till föregående syskonentitet i en logisk ordning. När rader i ett stycke uppdelat över sidorna upprepas kommer denna metod att flyttas till föregående rad även om den finns på en annan sida. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset)() | Flyttar räknaren till dokumentets första sida. |

### Exempel

Visar sätt att gå igenom ett dokuments layoutenheter.

```csharp
public void LayoutEnumerator()
{
    // Öppna ett dokument som innehåller en mängd olika layoutenheter.
    // Layoutentiteter är sidor, celler, rader, linjer och andra objekt som ingår i LayoutEntityType enum.
    // Varje layoutenhet har ett rektangulärt utrymme som det upptar i dokumentets brödtext.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Skapa en enumerator som kan passera dessa enheter som ett träd.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Vi kan anropa den här metoden för att säkerställa att enumeratorn kommer att vara på den första layoutentiteten.
    layoutEnumerator.Reset();

    // Det finns två order som bestämmer hur layoutuppräknaren fortsätter att korsa layoutentiteter
    // när den stöter på enheter som sträcker sig över flera sidor.
    // 1 - I visuell ordning:
    // När du går igenom en enhets underordnade som sträcker sig över flera sidor,
    // sidlayout har företräde, och vi flyttar till andra underordnade element på den här sidan och undviker de på nästa.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Vår enumerator är nu i slutet av samlingen. Vi kan korsa layoutentiteterna bakåt för att gå tillbaka till början.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - I logisk ordning:
    // När du går igenom en enhets underordnade som sträcker sig över flera sidor,
    // uppräknaren kommer att flytta mellan sidor för att gå igenom alla underordnade enheter.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// Räkna upp genom layoutEnumerators layoutentitetssamling framifrån till baksida,
/// på ett djupt-först sätt, och i "Visuell" ordning.
/// </summary>
private static void TraverseLayoutForward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNext());
}

/// <summary>
/// Räkna upp genom layoutEnumerators layoutentitetssamling bakifrån,
/// på ett djupt-först sätt, och i "Visuell" ordning.
/// </summary>
private static void TraverseLayoutBackward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePrevious());
}

/// <summary>
/// Räkna upp genom layoutEnumerators layoutentitetssamling framifrån till baksida,
/// på ett djupt-först sätt, och i den "logiska" ordningen.
/// </summary>
private static void TraverseLayoutForwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNextLogical());
}

/// <summary>
/// Räkna upp genom layoutEnumerators layoutentitetssamling bakifrån,
/// på ett djupt-först sätt, och i den "logiska" ordningen.
/// </summary>
private static void TraverseLayoutBackwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePreviousLogical());
}

/// <summary>
/// Skriv ut information om layoutEnumerators nuvarande enhet till konsolen, samtidigt som texten indrages med tabbtecken
/// baserat på dess djup i förhållande till rotnoden som vi angav i konstruktorn LayoutEnumerator-instansen.
/// Rektangeln som vi bearbetar i slutet representerar området och platsen som enheten tar upp i dokumentet.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // Endast spann kan innehålla text.
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### Se även

* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
