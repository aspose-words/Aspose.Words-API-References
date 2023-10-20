---
title: ListLabel.LabelValue
linktitle: LabelValue
articleTitle: LabelValue
second_title: Aspose.Words für .NET
description: ListLabel LabelValue eigendom. Ruft einen numerischen Wert für dieses Label ab in C#.
type: docs
weight: 30
url: /de/net/aspose.words.lists/listlabel/labelvalue/
---
## ListLabel.LabelValue property

Ruft einen numerischen Wert für dieses Label ab.

```csharp
public int LabelValue { get; }
```

## Bemerkungen

Verwenden Sie die[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) Methode zum Aktualisieren des Werts dieser Eigenschaft.

## Beispiele

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
     // Bei dieser Textausgabe werden Listenbeschriftungen weggelassen. Schneiden Sie alle Absatzformatierungszeichen ab.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Dadurch wird die Position des Absatzes in der aktuellen Ebene der Liste ermittelt. Wenn wir eine Liste mit mehreren Ebenen haben,
    // das wird uns sagen, welche Position es auf dieser Ebene hat.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Kombinieren Sie sie, um die Listenbeschriftung mit dem Text in die Ausgabe einzuschließen.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Siehe auch

* class [ListLabel](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
