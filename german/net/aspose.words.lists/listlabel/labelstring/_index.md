---
title: ListLabel.LabelString
second_title: Aspose.Words für .NET-API-Referenz
description: ListLabel eigendom. Ruft eine Zeichenfolgendarstellung der Listenbezeichnung ab.
type: docs
weight: 20
url: /de/net/aspose.words.lists/listlabel/labelstring/
---
## ListLabel.LabelString property

Ruft eine Zeichenfolgendarstellung der Listenbezeichnung ab.

```csharp
public string LabelString { get; }
```

### Beispiele

Zeigt, wie die Listenbeschriftungen aller Absätze extrahiert werden, die Listenelemente sind.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Finden Sie heraus, ob wir die Absatzliste haben. In unserem Dokument verwendet unsere Liste einfache arabische Zahlen,
// die um drei beginnen und um sechs enden.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Dies ist der Text, den wir erhalten, wenn wir diesen Knoten im Textformat ausgeben.
    // Diese Textausgabe lässt Listenlabels weg. Trimmen Sie alle Absatzformatierungszeichen. 
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Dadurch wird die Position des Absatzes in der aktuellen Ebene der Liste abgerufen. Wenn wir eine Liste mit mehreren Ebenen haben,
    // dies wird uns sagen, welche Position es auf dieser Ebene ist.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Kombinieren Sie sie, um das Listenlabel mit dem Text in die Ausgabe aufzunehmen.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Siehe auch

* class [ListLabel](../)
* namensraum [Aspose.Words.Lists](../../listlabel/)
* Montage [Aspose.Words](../../../)


