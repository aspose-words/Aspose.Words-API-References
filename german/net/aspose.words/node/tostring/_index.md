---
title: Node.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words für .NET
description: Node ToString methode. Exportiert den Inhalt des Knotens in einen String im angegebenen Format in C#.
type: docs
weight: 160
url: /de/net/aspose.words/node/tostring/
---
## ToString(*[SaveFormat](../../saveformat/)*) {#tostring_1}

Exportiert den Inhalt des Knotens in einen String im angegebenen Format.

```csharp
public string ToString(SaveFormat saveFormat)
```

### Rückgabewert

Der Inhalt des Knotens im angegebenen Format.

## Beispiele

Zeigt den Unterschied zwischen dem Aufruf der GetText- und ToString-Methoden auf einem Knoten.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText ruft den sichtbaren Text sowie Feldcodes und Sonderzeichen ab.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString gibt uns das Aussehen des Dokuments, wenn es in einem übergebenen Speicherformat gespeichert wird.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

Exportiert den Inhalt eines Knotens als String im HTML-Format.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Wenn wir die ToString-Methode mit der HTML-SaveFormat-Überladung aufrufen,
// Es konvertiert den Inhalt des Knotens in seine rohe HTML-Darstellung.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Wir können das Ergebnis dieser Konvertierung auch mithilfe eines SaveOptions-Objekts ändern.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

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

* enum [SaveFormat](../../saveformat/)
* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## ToString(*[SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#tostring_2}

Exportiert den Inhalt des Knotens mit den angegebenen Speicheroptionen in einen String.

```csharp
public string ToString(SaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveOptions | SaveOptions | Gibt die Optionen an, die steuern, wie der Knoten gespeichert wird. |

### Rückgabewert

Der Inhalt des Knotens im angegebenen Format.

## Beispiele

Exportiert den Inhalt eines Knotens als String im HTML-Format.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Wenn wir die ToString-Methode mit der HTML-SaveFormat-Überladung aufrufen,
// Es konvertiert den Inhalt des Knotens in seine rohe HTML-Darstellung.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Wir können das Ergebnis dieser Konvertierung auch mithilfe eines SaveOptions-Objekts ändern.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
