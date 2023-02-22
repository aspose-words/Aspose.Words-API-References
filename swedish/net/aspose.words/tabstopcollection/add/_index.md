---
title: TabStopCollection.Add
second_title: Aspose.Words för .NET API Referens
description: TabStopCollection metod. Lägger till eller ersätter ett tabbstopp i samlingen.
type: docs
weight: 30
url: /sv/net/aspose.words/tabstopcollection/add/
---
## Add(TabStop) {#add}

Lägger till eller ersätter ett tabbstopp i samlingen.

```csharp
public void Add(TabStop tabStop)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| tabStop | TabStop | Ett tabbstoppobjekt att lägga till. |

### Anmärkningar

Om ett tabbstopp redan finns på den angivna positionen ersätts det.

### Exempel

Visar hur man lägger till anpassade tabbstopp i ett dokument.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Nedan finns två sätt att lägga till tabbstopp till ett styckes samling av tabbstopp via egenskapen "ParagraphFormat".
// 1 - Skapa ett "TabStop"-objekt och lägg sedan till det i samlingen:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - Skicka värdena för egenskaper för ett nytt tabbstopp till metoden "Lägg till":
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Lägg till tabbstopp vid 5 cm till alla stycken.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Varje "tab"-tecken tar byggarens markör till platsen för nästa tabbstopp.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### Se även

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* namnutrymme [Aspose.Words](../../tabstopcollection/)
* hopsättning [Aspose.Words](../../../)

---

## Add(double, TabAlignment, TabLeader) {#add_1}

Lägger till eller ersätter ett tabbstopp i samlingen.

```csharp
public void Add(double position, TabAlignment alignment, TabLeader leader)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| position | Double | En position (i punkter) där tabbstoppet ska läggas till. |
| alignment | TabAlignment | A[`TabAlignment`](../../tabalignment/)värde that anger justeringen av text vid tabbstoppet. |
| leader | TabLeader | A[`TabLeader`](../../tableader/) värde that anger typen av ledarraden som visas under tabbtecknet. |

### Anmärkningar

Om ett tabbstopp redan finns på den angivna positionen ersätts det.

### Exempel

Visar hur man lägger till anpassade tabbstopp i ett dokument.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Nedan finns två sätt att lägga till tabbstopp till ett styckes samling av tabbstopp via egenskapen "ParagraphFormat".
// 1 - Skapa ett "TabStop"-objekt och lägg sedan till det i samlingen:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - Skicka värdena för egenskaper för ett nytt tabbstopp till metoden "Lägg till":
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Lägg till tabbstopp vid 5 cm till alla stycken.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Varje "tab"-tecken tar byggarens markör till platsen för nästa tabbstopp.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### Se även

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStopCollection](../)
* namnutrymme [Aspose.Words](../../tabstopcollection/)
* hopsättning [Aspose.Words](../../../)


