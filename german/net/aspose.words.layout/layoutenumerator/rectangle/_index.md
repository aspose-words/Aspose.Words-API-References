---
title: Rectangle
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt das Begrenzungsrechteck des aktuellen Objekts relativ zur linken oberen Ecke der Seite zurück in Punkt.
type: docs
weight: 60
url: /de/net/aspose.words.layout/layoutenumerator/rectangle/
---
## LayoutEnumerator.Rectangle property

Gibt das Begrenzungsrechteck des aktuellen Objekts relativ zur linken oberen Ecke der Seite zurück (in Punkt).

```csharp
public RectangleF Rectangle { get; }
```

### Beispiele

Zeigt Möglichkeiten zum Durchlaufen der Layout-Elemente eines Dokuments.

```csharp
public void LayoutEnumerator()
{
    // Öffnen Sie ein Dokument, das eine Vielzahl von Layout-Entitäten enthält.
    // Layoutentitäten sind Seiten, Zellen, Zeilen, Zeilen und andere Objekte, die in der Aufzählung LayoutEntityType enthalten sind.
    // Jedes Layoutobjekt hat einen rechteckigen Platz, den es im Dokumentkörper einnimmt.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Erstellen Sie einen Enumerator, der diese Entitäten wie einen Baum durchlaufen kann.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Wir können diese Methode aufrufen, um sicherzustellen, dass sich der Enumerator an der ersten Layout-Entität befindet.
    layoutEnumerator.Reset();

    // Es gibt zwei Befehle, die bestimmen, wie der Layout-Enumerator weiterhin Layout-Entitäten durchläuft
    // wenn Entitäten gefunden werden, die sich über mehrere Seiten erstrecken.
    // 1 - In visueller Reihenfolge:
    // Wenn Sie sich durch die Kinder einer Entität bewegen, die sich über mehrere Seiten erstrecken,
    // Das Seitenlayout hat Vorrang, und wir wechseln zu anderen untergeordneten Elementen auf dieser Seite und vermeiden die auf der nächsten.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Unser Enumerator ist jetzt am Ende der Sammlung. Wir können die Layout-Elemente rückwärts durchlaufen, um zum Anfang zurückzukehren.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - In logischer Reihenfolge:
    // Wenn Sie sich durch die Kinder einer Entität bewegen, die sich über mehrere Seiten erstrecken,
    // Der Enumerator bewegt sich zwischen den Seiten, um alle untergeordneten Entitäten zu durchlaufen.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// Von vorne nach hinten durch die Layout-Entity-Sammlung von layoutEnumerator aufzählen,
/// in einer Tiefe-zuerst-Weise und in der "visuellen" Reihenfolge.
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
/// Von hinten nach vorne durch die Layout-Entity-Sammlung von layoutEnumerator aufzählen,
/// in einer Tiefe-zuerst-Weise und in der "visuellen" Reihenfolge.
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
/// Von vorne nach hinten durch die Layout-Entity-Sammlung von layoutEnumerator aufzählen,
/// in einer Tiefe-zuerst-Weise und in der "logischen" Reihenfolge.
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
/// Von hinten nach vorne durch die Layout-Entity-Sammlung von layoutEnumerator aufzählen,
/// in einer Tiefe-zuerst-Weise und in der "logischen" Reihenfolge.
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
/// Gibt Informationen über die aktuelle Entität von layoutEnumerator an die Konsole aus, während der Text mit Tabulatorzeichen eingerückt wird
/// basierend auf seiner Tiefe relativ zum Stammknoten, den wir in der LayoutEnumerator-Instanz des Konstruktors bereitgestellt haben.
/// Das Rechteck, das wir am Ende verarbeiten, stellt den Bereich und die Position dar, die die Entität im Dokument einnimmt.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // Nur Spans können Text enthalten.
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### Siehe auch

* class [LayoutEnumerator](../../layoutenumerator)
* namensraum [Aspose.Words.Layout](../../layoutenumerator)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
