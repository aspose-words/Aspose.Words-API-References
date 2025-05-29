---
title: LayoutEnumerator Class
linktitle: LayoutEnumerator
articleTitle: LayoutEnumerator
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Layout.LayoutEnumerator för effektiv uppräkning av dokumentlayout. Utforska sidgeometri, text och struktur utan ansträngning!
type: docs
weight: 3790
url: /sv/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

Räknar upp sidlayoutenheter i ett dokument. Du kan använda den här klassen för att gå igenom sidlayoutmodellen. Tillgängliga egenskaper är typ, geometri, text och sidindex där enheten återges, samt övergripande struktur och relationer. Använd en kombination av[`GetEntity`](../layoutcollector/getentity/) och[`Current`](./current/) flytta till den enhet som motsvarar en dokumentnod.

För att lära dig mer, besök[Konvertera till fast sidformat](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) dokumentationsartikel.

```csharp
public class LayoutEnumerator
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [LayoutEnumerator](layoutenumerator/)(*[Document](../../aspose.words/document/)*) | Initierar en ny instans av den här klassen. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Current](../../aspose.words.layout/layoutenumerator/current/) { get; set; } | Hämtar eller anger aktuell position i sidlayoutmodellen. Den här egenskapen returnerar ett ogenomskinligt objekt som motsvarar den aktuella layoutentiteten. |
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | Hämtar dokument som denna instans räknar upp. |
| [Item](../../aspose.words.layout/layoutenumerator/item/) { get; } | Hämtar en namngiven egenskap för entiteten. |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | Hämtar typen av den aktuella entiteten. Detta kan vara en tom sträng men aldrig`null` . |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | Hämtar det 1-baserade indexet för en sida som innehåller den aktuella entiteten. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | Returnerar den avgränsande rektangeln för den aktuella enheten i förhållande till sidans övre vänstra hörn (i punkter). |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | Hämtar text för den aktuella span-entiteten. Utlöser andra entitetstyper. |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | Hämtar typen för den aktuella entiteten. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | Flyttar till den första underordnade enheten. |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | Flyttar till den sista underordnade enheten. |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | Flyttar till nästa syskonenhet i visuell ordning. När rader i ett stycke itereras över sidor kommer den här metoden inte att flyttas till nästa sida utan snarare till nästa entitet på samma sida. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | Flyttar till nästa syskonenhet i en logisk ordning. När rader i ett stycke itereras som är uppdelade över sidor kommer den här metoden att flyttas till nästa rad även om den finns på en annan sida. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | Flyttar till moderenheten. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(*[LayoutEntityType](../layoutentitytype/)*) | Flyttar till den överordnade enheten av den angivna typen. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | Flyttar till den föregående syskonenheten. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | Flyttar till föregående syskonenhet i en logisk ordning. När rader i ett stycke itereras över sidor kommer den här metoden att flyttas till föregående rad även om den finns på en annan sida. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | Flyttar uppräknaren till dokumentets första sida. |

## Exempel

Visar sätt att navigera genom ett dokuments layoutenheter.

```csharp
public void LayoutEnumerator()
{
    // Öppna ett dokument som innehåller en mängd olika layoutenheter.
    // Layoutentiteter är sidor, celler, rader, linjer och andra objekt som ingår i LayoutEntityType-enum.
    // Varje layoutenhet har ett rektangulärt utrymme som den upptar i dokumentets brödtext.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Skapa en uppräknare som kan tvärförflytta sig mellan dessa entiteter som ett träd.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Vi kan anropa den här metoden för att säkerställa att uppräknaren kommer att finnas vid den första layout-entiteten.
    layoutEnumerator.Reset();

    // Det finns två ordningar som avgör hur layoutuppräknaren fortsätter att gå igenom layoutenheter
    // när den stöter på entiteter som sträcker sig över flera sidor.
    // 1 - I visuell ordning:
    // När man bläddrar igenom en entitets underordnade objekt som sträcker sig över flera sidor,
    // sidlayout har företräde, och vi flyttar till andra underordnade element på den här sidan och undviker de på nästa.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Vår uppräknare är nu i slutet av samlingen. Vi kan bläddra bakåt i layout-entiteterna för att gå tillbaka till början.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - I logisk ordning:
    // När man bläddrar igenom en entitets underordnade objekt som sträcker sig över flera sidor,
    // uppräknaren kommer att flytta mellan sidor för att täcka alla underordnade enheter.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// Räkna upp genom layoutEnumerators layout-entitetssamling framifrån och bakifrån,
/// på ett djupgående sätt och i den "visuella" ordningen.
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
/// Räkna upp genom layoutEnumerators layout-entitetssamling bakifrån och fram,
/// på ett djupgående sätt och i den "visuella" ordningen.
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
/// Räkna upp genom layoutEnumerators layout-entitetssamling framifrån och bakifrån,
/// på ett djupgående sätt och i den "logiska" ordningen.
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
/// Räkna upp genom layoutEnumerators layout-entitetssamling bakifrån och fram,
/// på ett djupgående sätt och i den "logiska" ordningen.
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
/// Skriv ut information om layoutEnumerators aktuella entitet till konsolen, medan texten indenteras med tabbtecken
/// baserat på dess djup i förhållande till rotnoden som vi angav i konstruktorns LayoutEnumerator-instans.
/// Rektangeln som vi bearbetar i slutet representerar det område och den plats som entiteten upptar i dokumentet.
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

* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../)
