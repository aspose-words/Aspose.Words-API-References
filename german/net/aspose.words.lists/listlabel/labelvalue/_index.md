---
title: ListLabel.LabelValue
linktitle: LabelValue
articleTitle: LabelValue
second_title: Aspose.Words für .NET
description: Entdecken Sie die LabelValue-Eigenschaft von ListLabel, um einfach numerische Werte für Beschriftungen abzurufen und so Ihre Datenverwaltung und Berichtseffizienz zu verbessern.
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

// Prüfen, ob die Absatzliste vorliegt. In unserem Dokument werden einfache arabische Zahlen verwendet.
// die um drei beginnen und um sechs enden.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Dies ist der Text, den wir erhalten, wenn wir diesen Knoten im Textformat ausgeben.
        // In dieser Textausgabe werden Listenbeschriftungen weggelassen. Entfernen Sie alle Absatzformatierungszeichen.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Hiermit wird die Position des Absatzes in der aktuellen Ebene der Liste ermittelt. Bei einer Liste mit mehreren Ebenen:
    // Dadurch erfahren wir, welche Position es auf dieser Ebene hat.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Kombinieren Sie sie, um die Listenbezeichnung mit dem Text in die Ausgabe einzuschließen.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Siehe auch

* class [ListLabel](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
