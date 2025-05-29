---
title: LayoutEnumerator.MovePrevious
linktitle: MovePrevious
articleTitle: MovePrevious
second_title: Aspose.Words för .NET
description: Upptäck hur LayoutEnumerator MovePrevious-metoden effektivt navigerar till den föregående syskonentiteten, vilket förbättrar ditt kodningsarbetsflöde.
type: docs
weight: 150
url: /sv/net/aspose.words.layout/layoutenumerator/moveprevious/
---
## LayoutEnumerator.MovePrevious method

Flyttar till den föregående syskonenheten.

```csharp
public bool MovePrevious()
```

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

* class [LayoutEnumerator](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
