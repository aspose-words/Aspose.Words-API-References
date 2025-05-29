---
title: Document.UpdateListLabels
linktitle: UpdateListLabels
articleTitle: UpdateListLabels
second_title: Aspose.Words für .NET
description: Aktualisieren Sie mühelos alle Listenelementbeschriftungen in Ihrem Dokument mit der Methode UpdateListLabels und sorgen Sie so für Konsistenz und Klarheit Ihres Inhalts.
type: docs
weight: 820
url: /de/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Aktualisiert Listenbeschriftungen für alle Listenelemente im Dokument.

```csharp
public void UpdateListLabels()
```

## Bemerkungen

Diese Methode aktualisiert Listenbezeichnungseigenschaften wie[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) und [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) für jeden[`ListLabel`](../../paragraph/listlabel/) Objekt im Dokument.

Außerdem wird diese Methode manchmal implizit aufgerufen, wenn Felder im Dokument aktualisiert werden. Dies ist erforderlich, da einige Felder, die auf Listennummern verweisen (z. B. TOC oder REF), aktuelle Listennummern benötigen.

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

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
