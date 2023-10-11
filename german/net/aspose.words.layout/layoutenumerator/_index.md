---
title: Class LayoutEnumerator
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Layout.LayoutEnumerator klas. Zählt SeitenlayoutEntitäten eines Dokuments auf. Mit dieser Klasse können Sie das Seitenlayoutmodell durchgehen. Verfügbare Eigenschaften sind Typ Geometrie Text und Seitenindex in dem die Entität gerendert wird sowie die Gesamtstruktur und Beziehungen. Verwenden Sie eine Kombination davonGetEntity UndCurrent Gehen Sie zu der Entität die einem Dokumentknoten entspricht.
type: docs
weight: 3340
url: /de/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

Zählt Seitenlayout-Entitäten eines Dokuments auf. Mit dieser Klasse können Sie das Seitenlayoutmodell durchgehen. Verfügbare Eigenschaften sind Typ, Geometrie, Text und Seitenindex, in dem die Entität gerendert wird, sowie die Gesamtstruktur und Beziehungen. Verwenden Sie eine Kombination davon[`GetEntity`](../layoutcollector/getentity/) Und[`Current`](./current/) Gehen Sie zu der Entität, die einem Dokumentknoten entspricht.

Um mehr zu erfahren, besuchen Sie die[Konvertieren in das Fixed-Page-Format](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) Dokumentationsartikel.

```csharp
public class LayoutEnumerator
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [LayoutEnumerator](layoutenumerator/)(Document) | Initialisiert eine neue Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Current](../../aspose.words.layout/layoutenumerator/current/) { get; set; } | Ruft die aktuelle Position im Seitenlayoutmodell ab oder legt diese fest. Diese Eigenschaft gibt ein undurchsichtiges Objekt zurück, das der aktuellen Layout-Entität entspricht. |
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | Ruft das Dokument ab, das diese Instanz auflistet. |
| [Item](../../aspose.words.layout/layoutenumerator/item/) { get; } | Ruft eine benannte Eigenschaft der Entität ab. |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | Ruft die Art der aktuellen Entität ab. Dies kann eine leere Zeichenfolge sein, jedoch niemals`Null` . |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | Ruft den 1-basierten Index einer Seite ab, die die aktuelle Entität enthält. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | Gibt das umschließende Rechteck des aktuellen Elements relativ zur oberen linken Ecke der Seite zurück (in Punkten). |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | Ruft Text der aktuellen Span-Entität ab. Auslöser für andere Entitätstypen. |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | Ruft den Typ der aktuellen Entität ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | Wechselt zur ersten untergeordneten Entität. |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | Wechselt zur letzten untergeordneten Entität. |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | Wechselt in visueller Reihenfolge zur nächsten gleichgeordneten Entität. Beim Iterieren von Zeilen eines Absatzes, die über Seiten hinweg unterbrochen sind, wechselt diese Methode nicht zur nächsten Seite, sondern zur nächsten Entität auf derselben Seite. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | Wechselt in logischer Reihenfolge zur nächsten gleichgeordneten Entität. Wenn Zeilen eines Absatzes über mehrere Seiten hinweg wiederholt werden, wechselt diese Methode zur nächsten Zeile, auch wenn sie sich auf einer anderen Seite befindet. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | Verschiebt sich zur übergeordneten Entität. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(LayoutEntityType) | Verschiebt sich zur übergeordneten Entität des angegebenen Typs. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | Wechselt zur vorherigen Geschwisterentität. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | Wechselt in einer logischen Reihenfolge zur vorherigen gleichgeordneten Entität. Beim Iterieren von Zeilen eines Absatzes, die über Seiten hinweg unterbrochen sind, wechselt diese Methode zur vorherigen Zeile, auch wenn sie sich auf einer anderen Seite befindet. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | Verschiebt den Enumerator auf die erste Seite des Dokuments. |

### Beispiele

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

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)


