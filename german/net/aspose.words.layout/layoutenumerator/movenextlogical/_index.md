---
title: LayoutEnumerator.MoveNextLogical
linktitle: MoveNextLogical
articleTitle: MoveNextLogical
second_title: Aspose.Words für .NET
description: LayoutEnumerator MoveNextLogical methode. Wechselt in logischer Reihenfolge zur nächsten gleichgeordneten Entität. Wenn Zeilen eines Absatzes über mehrere Seiten hinweg wiederholt werden wechselt diese Methode zur nächsten Zeile auch wenn sie sich auf einer anderen Seite befindet in C#.
type: docs
weight: 130
url: /de/net/aspose.words.layout/layoutenumerator/movenextlogical/
---
## LayoutEnumerator.MoveNextLogical method

Wechselt in logischer Reihenfolge zur nächsten gleichgeordneten Entität. Wenn Zeilen eines Absatzes über mehrere Seiten hinweg wiederholt werden, wechselt diese Methode zur nächsten Zeile, auch wenn sie sich auf einer anderen Seite befindet.

```csharp
public bool MoveNextLogical()
```

## Bemerkungen

Beachten Sie, dass alleSpan Entitäten sind also miteinander verbunden, wenn[`Current`](../current/) Die Entität ist bereichsübergreifend. Durch wiederholtes Aufrufen dieser Methode wird die gesamte Geschichte des Dokuments iteriert.

## Beispiele

Zeigt Möglichkeiten zum Durchlaufen der Layoutelemente eines Dokuments.

```csharp
public void LayoutEnumerator()
{
    // Öffnen Sie ein Dokument, das verschiedene Layout-Entitäten enthält.
    // Layout-Entitäten sind Seiten, Zellen, Zeilen, Linien und andere Objekte, die in der LayoutEntityType-Enumeration enthalten sind.
    // Jede Layout-Entität hat einen rechteckigen Raum, den sie im Dokumentkörper einnimmt.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Erstelle einen Enumerator, der diese Entitäten wie einen Baum durchlaufen kann.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Wir können diese Methode aufrufen, um sicherzustellen, dass sich der Enumerator bei der ersten Layout-Entität befindet.
    layoutEnumerator.Reset();

    // Es gibt zwei Reihenfolgen, die bestimmen, wie der Layout-Enumerator weiterhin Layout-Entitäten durchläuft
    // wenn es auf Entitäten trifft, die sich über mehrere Seiten erstrecken.
    // 1 – In visueller Reihenfolge:
    // Beim Durchlaufen der untergeordneten Elemente einer Entität, die sich über mehrere Seiten erstrecken,
    // Das Seitenlayout hat Vorrang, und wir wechseln zu anderen untergeordneten Elementen auf dieser Seite und vermeiden diejenigen auf der nächsten.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Unser Enumerator ist jetzt am Ende der Sammlung. Wir können die Layout-Entitäten rückwärts durchlaufen, um zum Anfang zurückzukehren.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - In logischer Reihenfolge:
    // Beim Durchlaufen der untergeordneten Elemente einer Entität, die sich über mehrere Seiten erstrecken,
    // Der Enumerator bewegt sich zwischen den Seiten, um alle untergeordneten Entitäten zu durchlaufen.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// Durch die Layout-Entitätssammlung von layoutEnumerator von vorne nach hinten aufzählen,
/// in einer Tiefenrichtung und in der „visuellen“ Reihenfolge.
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
/// Durch die Layout-Entitätssammlung von layoutEnumerator von hinten nach vorne aufzählen,
/// in einer Tiefenrichtung und in der „visuellen“ Reihenfolge.
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
/// Durch die Layout-Entitätssammlung von layoutEnumerator von vorne nach hinten aufzählen,
/// in einer Tiefen-zuerst-Methode und in der „logischen“ Reihenfolge.
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
/// Durch die Layout-Entitätssammlung von layoutEnumerator von hinten nach vorne aufzählen,
/// in einer Tiefen-zuerst-Methode und in der „logischen“ Reihenfolge.
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
/// Informationen über die aktuelle Entität von layoutEnumerator an die Konsole ausgeben und dabei den Text mit Tabulatorzeichen einrücken
/// basierend auf seiner Tiefe relativ zum Stammknoten, den wir in der Konstruktor-LayoutEnumerator-Instanz bereitgestellt haben.
/// Das Rechteck, das wir am Ende verarbeiten, stellt die Fläche und Position dar, die die Entität im Dokument einnimmt.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // Nur Spannen können Text enthalten.
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### Siehe auch

* class [LayoutEnumerator](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
