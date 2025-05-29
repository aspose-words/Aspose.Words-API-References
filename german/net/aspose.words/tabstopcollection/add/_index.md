---
title: TabStopCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Add-Methode der TabStopCollection effizient Tabstopps hinzufügt oder aktualisiert und so das Layout und die Formatierung Ihres Dokuments verbessert.
type: docs
weight: 30
url: /de/net/aspose.words/tabstopcollection/add/
---
## Add(*[TabStop](../../tabstop/)*) {#add}

Fügt einen Tabulator in der Sammlung hinzu oder ersetzt ihn.

```csharp
public void Add(TabStop tabStop)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tabStop | TabStop | Ein hinzuzufügendes Tabstoppobjekt. |

## Bemerkungen

Wenn an der angegebenen Position bereits ein Tabulator vorhanden ist, wird dieser ersetzt.

## Beispiele

Zeigt, wie einem Dokument benutzerdefinierte Tabstopps hinzugefügt werden.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Nachfolgend finden Sie zwei Möglichkeiten zum Hinzufügen von Tabstopps zur Tabstopp-Sammlung eines Absatzes über die Eigenschaft „ParagraphFormat“.
// 1 - Erstellen Sie ein „TabStop“-Objekt und fügen Sie es dann der Sammlung hinzu:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - Übergeben Sie die Werte für die Eigenschaften eines neuen Tabstopps an die Methode „Add“:
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Fügen Sie allen Absätzen Tabstopps im Abstand von 5 cm hinzu.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Jedes „Tabulator“-Zeichen bringt den Cursor des Builders an die Position des nächsten Tabulatorstopps.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### Siehe auch

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Add(*double, [TabAlignment](../../tabalignment/), [TabLeader](../../tableader/)*) {#add_1}

Fügt einen Tabulator in der Sammlung hinzu oder ersetzt ihn.

```csharp
public void Add(double position, TabAlignment alignment, TabLeader leader)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| position | Double | Eine Position (in Punkten), an der der Tabulator hinzugefügt werden soll. |
| alignment | TabAlignment | A[`TabAlignment`](../../tabalignment/) Wert that gibt die Ausrichtung des Textes am Tabulatorstopp an. |
| leader | TabLeader | A[`TabLeader`](../../tableader/)Der Wert that gibt den Typ der Führungslinie an, die unter dem Tabulatorzeichen angezeigt wird. |

## Bemerkungen

Wenn an der angegebenen Position bereits ein Tabulator vorhanden ist, wird dieser ersetzt.

## Beispiele

Zeigt, wie einem Dokument benutzerdefinierte Tabstopps hinzugefügt werden.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Nachfolgend finden Sie zwei Möglichkeiten zum Hinzufügen von Tabstopps zur Tabstopp-Sammlung eines Absatzes über die Eigenschaft „ParagraphFormat“.
// 1 - Erstellen Sie ein „TabStop“-Objekt und fügen Sie es dann der Sammlung hinzu:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - Übergeben Sie die Werte für die Eigenschaften eines neuen Tabstopps an die Methode „Add“:
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Fügen Sie allen Absätzen Tabstopps im Abstand von 5 cm hinzu.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Jedes „Tabulator“-Zeichen bringt den Cursor des Builders an die Position des nächsten Tabulatorstopps.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### Siehe auch

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStopCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
