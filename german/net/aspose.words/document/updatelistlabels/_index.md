---
title: Document.UpdateListLabels
linktitle: UpdateListLabels
articleTitle: UpdateListLabels
second_title: Aspose.Words für .NET
description: Document UpdateListLabels methode. Aktualisiert Listenbezeichnungen für alle Listenelemente im Dokument in C#.
type: docs
weight: 760
url: /de/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Aktualisiert Listenbezeichnungen für alle Listenelemente im Dokument.

```csharp
public void UpdateListLabels()
```

## Bemerkungen

Diese Methode aktualisiert Eigenschaften von Listenbezeichnungen, z[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) and [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) für jede[`ListLabel`](../../paragraph/listlabel/)Objekt im Dokument.

Außerdem wird diese Methode manchmal implizit aufgerufen, wenn Felder im Dokument aktualisiert werden. Dies ist erforderlich , da einige Felder, die möglicherweise auf Listennummern verweisen (z. B. TOC oder REF), aktuell sein müssen.

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

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
