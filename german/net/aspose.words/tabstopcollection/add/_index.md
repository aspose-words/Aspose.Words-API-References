---
title: TabStopCollection.Add
second_title: Aspose.Words für .NET-API-Referenz
description: TabStopCollection methode. Fügt einen Tabstopp in der Sammlung hinzu oder ersetzt ihn.
type: docs
weight: 30
url: /de/net/aspose.words/tabstopcollection/add/
---
## Add(TabStop) {#add}

Fügt einen Tabstopp in der Sammlung hinzu oder ersetzt ihn.

```csharp
public void Add(TabStop tabStop)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tabStop | TabStop | Ein hinzuzufügendes Tabstoppobjekt. |

### Bemerkungen

Wenn an der angegebenen Position bereits ein Tabstopp vorhanden ist, wird dieser ersetzt.

### Beispiele

Zeigt, wie man benutzerdefinierte Tabstopps zu einem Dokument hinzufügt.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Im Folgenden finden Sie zwei Möglichkeiten, Tabstopps über die Eigenschaft „ParagraphFormat“ zur Tabstopp-Sammlung eines Absatzes hinzuzufügen.
// 1 – Erstellen Sie ein „TabStop“-Objekt und fügen Sie es dann der Sammlung hinzu:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 – Übergeben Sie die Werte für Eigenschaften eines neuen Tabstopps an die Methode „Add“:
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Fügen Sie allen Absätzen Tabstopps bei 5 cm hinzu.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Jedes „Tab“-Zeichen bringt den Cursor des Builders an die Position des nächsten Tabstopps.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### Siehe auch

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* namensraum [Aspose.Words](../../tabstopcollection/)
* Montage [Aspose.Words](../../../)

---

## Add(double, TabAlignment, TabLeader) {#add_1}

Fügt einen Tabstopp in der Sammlung hinzu oder ersetzt ihn.

```csharp
public void Add(double position, TabAlignment alignment, TabLeader leader)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| position | Double | Eine Position (in Punkt), an der der Tabstopp hinzugefügt werden soll. |
| alignment | TabAlignment | A[`TabAlignment`](../../tabalignment/) Der Wert that gibt die Ausrichtung des Texts am Tabstopp an. |
| leader | TabLeader | A[`TabLeader`](../../tableader/) Der Wert that gibt den Typ der Führungslinie an, die unter dem Tabulatorzeichen angezeigt wird. |

### Bemerkungen

Wenn an der angegebenen Position bereits ein Tabstopp vorhanden ist, wird dieser ersetzt.

### Beispiele

Zeigt, wie man benutzerdefinierte Tabstopps zu einem Dokument hinzufügt.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Im Folgenden finden Sie zwei Möglichkeiten, Tabstopps über die Eigenschaft „ParagraphFormat“ zur Tabstopp-Sammlung eines Absatzes hinzuzufügen.
// 1 – Erstellen Sie ein „TabStop“-Objekt und fügen Sie es dann der Sammlung hinzu:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 – Übergeben Sie die Werte für Eigenschaften eines neuen Tabstopps an die Methode „Add“:
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Fügen Sie allen Absätzen Tabstopps bei 5 cm hinzu.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Jedes „Tab“-Zeichen bringt den Cursor des Builders an die Position des nächsten Tabstopps.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### Siehe auch

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStopCollection](../)
* namensraum [Aspose.Words](../../tabstopcollection/)
* Montage [Aspose.Words](../../../)


