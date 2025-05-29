---
title: LayoutEnumerator Class
linktitle: LayoutEnumerator
articleTitle: LayoutEnumerator
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Layout.LayoutEnumerator für eine effiziente Dokumentlayout-Aufzählung. Erkunden Sie mühelos Seitengeometrie, Text und Struktur!
type: docs
weight: 3790
url: /de/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

Enumeriert die Seitenlayout-Entitäten eines Dokuments. Mit dieser Klasse können Sie das Seitenlayoutmodell durchlaufen. Verfügbare Eigenschaften sind Typ, Geometrie, Text und Seitenindex, in dem die Entität gerendert wird, sowie die Gesamtstruktur und Beziehungen. Verwenden Sie eine Kombination aus[`GetEntity`](../layoutcollector/getentity/) Und[`Current`](./current/) Wechseln Sie zu der Entität, die einem Dokumentknoten entspricht.

Um mehr zu erfahren, besuchen Sie die[Konvertieren in das Festseitenformat](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) Dokumentationsartikel.

```csharp
public class LayoutEnumerator
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [LayoutEnumerator](layoutenumerator/)(*[Document](../../aspose.words/document/)*) | Initialisiert eine neue Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Current](../../aspose.words.layout/layoutenumerator/current/) { get; set; } | Ruft die aktuelle Position im Seitenlayoutmodell ab oder legt sie fest. Diese Eigenschaft gibt ein undurchsichtiges Objekt zurück, das der aktuellen Layoutentität entspricht. |
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | Ruft das Dokument ab, das diese Instanz aufzählt. |
| [Item](../../aspose.words.layout/layoutenumerator/item/) { get; } | Ruft eine benannte Eigenschaft der Entität ab. |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | Gibt die Art der aktuellen Entität an. Dies kann ein leerer String sein, aber niemals`null` . |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | Ruft den 1-basierten Index einer Seite ab, die die aktuelle Entität enthält. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | Gibt das Begrenzungsrechteck der aktuellen Entität relativ zur oberen linken Ecke der Seite (in Punkten) zurück. |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | Ruft den Text der aktuellen Span-Entität ab. Löst für andere Entitätstypen aus. |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | Ruft den Typ der aktuellen Entität ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | Wechselt zur ersten untergeordneten Entität. |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | Wechselt zur letzten untergeordneten Entität. |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | Wechselt zur nächsten Geschwisterentität in visueller Reihenfolge. Beim Durchlaufen von Zeilen eines Absatzes, der über mehrere Seiten verteilt ist, wechselt diese Methode nicht zur nächsten Seite, sondern zur nächsten Entität auf derselben Seite. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | Wechselt in logischer Reihenfolge zum nächsten Geschwisterelement. Beim Durchlaufen von Zeilen eines Absatzes, der über mehrere Seiten verteilt ist, wechselt diese Methode zur nächsten Zeile, auch wenn sich diese auf einer anderen Seite befindet. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | Wechselt zur übergeordneten Entität. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(*[LayoutEntityType](../layoutentitytype/)*) | Wechselt zur übergeordneten Entität des angegebenen Typs. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | Wechselt zur vorherigen Geschwisterentität. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | Wechselt in logischer Reihenfolge zur vorherigen Geschwisterentität. Beim Durchlaufen von Zeilen eines Absatzes, der über mehrere Seiten verteilt ist, wechselt diese Methode zur vorherigen Zeile, auch wenn diese sich auf einer anderen Seite befindet. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | Verschiebt den Enumerator auf die erste Seite des Dokuments. |

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

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)
