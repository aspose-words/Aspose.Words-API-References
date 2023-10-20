---
title: LayoutEnumerator.MoveLastChild
linktitle: MoveLastChild
articleTitle: MoveLastChild
second_title: Aspose.Words för .NET
description: LayoutEnumerator MoveLastChild metod. Flyttar till den sista underordnade enheten i C#.
type: docs
weight: 110
url: /sv/net/aspose.words.layout/layoutenumerator/movelastchild/
---
## LayoutEnumerator.MoveLastChild method

Flyttar till den sista underordnade enheten.

```csharp
public bool MoveLastChild()
```

## Exempel

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

* class [LayoutEnumerator](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
