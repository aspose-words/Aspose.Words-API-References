---
title: LayoutEnumerator.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „LayoutEnumerator-Typ“, greifen Sie einfach auf den Typ der aktuellen Entität zu, um die Datenverarbeitung zu optimieren und die Anwendungsleistung zu verbessern.
type: docs
weight: 90
url: /de/net/aspose.words.layout/layoutenumerator/type/
---
## LayoutEnumerator.Type property

Ruft den Typ der aktuellen Entität ab.

```csharp
public LayoutEntityType Type { get; }
```

## Beispiele

Zeigt Möglichkeiten zum Durchlaufen der Layout-Entitäten eines Dokuments.

```csharp
public void LayoutEnumerator()
{
    // Öffnen Sie ein Dokument, das verschiedene Layout-Entitäten enthält.
    // Layout-Entitäten sind Seiten, Zellen, Zeilen, Linien und andere Objekte, die in der LayoutEntityType-Aufzählung enthalten sind.
    // Jede Layout-Entität hat einen rechteckigen Platz, den sie im Dokumentkörper einnimmt.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Erstellen Sie einen Enumerator, der diese Entitäten wie einen Baum durchlaufen kann.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Wir können diese Methode aufrufen, um sicherzustellen, dass sich der Enumerator bei der ersten Layout-Entität befindet.
    layoutEnumerator.Reset();

    // Es gibt zwei Reihenfolgen, die bestimmen, wie der Layout-Enumerator die Layout-Entitäten weiter durchläuft
    // wenn es auf Entitäten stößt, die sich über mehrere Seiten erstrecken.
    // 1 – In visueller Reihenfolge:
    // Wenn Sie sich durch die untergeordneten Elemente einer Entität bewegen, die sich über mehrere Seiten erstrecken,
    // Das Seitenlayout hat Vorrang und wir wechseln zu anderen untergeordneten Elementen auf dieser Seite und vermeiden die auf der nächsten.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Unser Enumerator befindet sich nun am Ende der Sammlung. Wir können die Layout-Entitäten rückwärts durchlaufen, um zum Anfang zurückzukehren.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - In logischer Reihenfolge:
    // Wenn Sie sich durch die untergeordneten Elemente einer Entität bewegen, die sich über mehrere Seiten erstrecken,
    // Der Enumerator bewegt sich zwischen den Seiten, um alle untergeordneten Entitäten zu durchlaufen.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// Durchlaufen Sie die Layout-Entity-Sammlung des LayoutEnumerators von vorne nach hinten.
/// in einer Tiefensuche und in der Reihenfolge „Visuell“.
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
/// Durchlaufen Sie die Layout-Entity-Sammlung des LayoutEnumerators von hinten nach vorne,
/// in einer Tiefensuche und in der Reihenfolge „Visuell“.
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
/// Durchlaufen Sie die Layout-Entity-Sammlung des LayoutEnumerators von vorne nach hinten.
/// in einer Tiefensuche und in der „logischen“ Reihenfolge.
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
/// Durchlaufen Sie die Layout-Entity-Sammlung des LayoutEnumerators von hinten nach vorne,
/// in einer Tiefensuche und in der „logischen“ Reihenfolge.
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
/// Informationen zur aktuellen Entität des LayoutEnumerators auf der Konsole ausgeben und dabei den Text mit Tabulatorzeichen einrücken
/// basierend auf seiner Tiefe relativ zum Stammknoten, den wir in der Konstruktor-Instanz LayoutEnumerator bereitgestellt haben.
/// Das Rechteck, das wir am Ende verarbeiten, stellt den Bereich und die Position dar, die die Entität im Dokument einnimmt.
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

* enum [LayoutEntityType](../../layoutentitytype/)
* class [LayoutEnumerator](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
