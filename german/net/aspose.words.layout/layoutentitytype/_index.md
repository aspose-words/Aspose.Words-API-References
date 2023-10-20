---
title: LayoutEntityType Enum
linktitle: LayoutEntityType
articleTitle: LayoutEntityType
second_title: Aspose.Words für .NET
description: Aspose.Words.Layout.LayoutEntityType opsomming. Typen der LayoutEntitäten in C#.
type: docs
weight: 3330
url: /de/net/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enumeration

Typen der Layout-Entitäten.

```csharp
[Flags]
public enum LayoutEntityType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Standardwert. |
| Page | `1` | Stellt die Seite eines Dokuments dar. Seite kann habenColumn ,HeaderFooter UndComment Untergeordnete Entitäten. |
| Column | `2` | Stellt eine Textspalte auf einer Seite dar. Die Spalte kann dieselben untergeordneten Entitäten haben wieCell , PlusFootnote ,Endnote UndNoteSeparator Entitäten. |
| Row | `8` | Stellt eine Tabellenzeile dar. Zeile kann habenCell als untergeordnete Entitäten. |
| Cell | `10` | Stellt eine Tabellenzelle dar. Zelle kann habenLine UndRow Untergeordnete Entitäten. |
| Line | `20` | Stellt eine Zeichenzeile aus Text und Inline-Objekten dar. Zeile kann Folgendes habenSpan Untergeordnete Entitäten. |
| Span | `40` | Stellt ein oder mehrere Zeichen in einer Zeile dar. Dazu gehören Sonderzeichen wie Feldanfangs-/Endmarkierungen, Lesezeichen und Kommentare. Span darf keine untergeordneten Entitäten haben. |
| Footnote | `100` | Stellt einen Platzhalter für den Fußnoteninhalt dar. Fußnote kann Folgendes enthaltenNote Untergeordnete Entitäten. |
| Endnote | `200` | Stellt einen Platzhalter für den Endnoteninhalt dar. Endnote kann Folgendes habenNote Untergeordnete Entitäten. |
| Note | `4000` | Stellt einen Platzhalter für den Notizinhalt dar. Notiz kann vorhanden seinLine UndRow Untergeordnete Entitäten. |
| HeaderFooter | `400` | Stellt einen Platzhalter für Kopf-/Fußzeileninhalte auf einer Seite dar. HeaderFooter kann Folgendes habenLine UndRow Untergeordnete Entitäten. |
| TextBox | `800` | Stellt den Textbereich innerhalb einer Form dar. Textfeld kann habenLine UndRow Untergeordnete Entitäten. |
| Comment | `1000` | Stellt einen Platzhalter für den Kommentarinhalt dar. Kommentar kann vorhanden seinLine UndRow Untergeordnete Entitäten. |
| NoteSeparator | `2000` | Stellt das Fußnoten-/Endnotentrennzeichen dar. NoteSeparator kann vorhanden seinLine UndRow Untergeordnete Entitäten. |

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

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)
