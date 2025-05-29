---
title: Node.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words für .NET
description: Entdecken Sie die Node-ToString-Methode und konvertieren Sie Knoteninhalte mühelos in Zeichenfolgen mit anpassbaren Formaten für eine verbesserte Datenverarbeitung. Optimieren Sie Ihren Code noch heute!
type: docs
weight: 160
url: /de/net/aspose.words/node/tostring/
---
## ToString(*[SaveFormat](../../saveformat/)*) {#tostring_1}

Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format.

```csharp
public string ToString(SaveFormat saveFormat)
```

### Rückgabewert

Der Inhalt des Knotens im angegebenen Format.

## Beispiele

Zeigt den Unterschied zwischen dem Aufrufen der Methoden GetText und ToString auf einem Knoten.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText ruft den sichtbaren Text sowie Feldcodes und Sonderzeichen ab.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015", doc.GetText().Trim());

// ToString gibt uns das Erscheinungsbild des Dokuments an, wenn es in einem übergebenen Speicherformat gespeichert wird.
Assert.AreEqual("«Field»", doc.ToString(SaveFormat.Text).Trim());
```

Exportiert den Inhalt eines Knotens in einen String im HTML-Format.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Wenn wir die ToString-Methode mit der HTML-SaveFormat-Überladung aufrufen,
// es konvertiert den Inhalt des Knotens in seine Roh-HTML-Darstellung.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Wir können das Ergebnis dieser Konvertierung auch mit einem SaveOptions-Objekt ändern.
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

* enum [SaveFormat](../../saveformat/)
* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## ToString(*[SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#tostring_2}

Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge.

```csharp
public string ToString(SaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveOptions | SaveOptions | Gibt die Optionen an, die steuern, wie der Knoten gespeichert wird. |

### Rückgabewert

Der Inhalt des Knotens im angegebenen Format.

## Beispiele

Exportiert den Inhalt eines Knotens in einen String im HTML-Format.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Wenn wir die ToString-Methode mit der HTML-SaveFormat-Überladung aufrufen,
// es konvertiert den Inhalt des Knotens in seine Roh-HTML-Darstellung.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Wir können das Ergebnis dieser Konvertierung auch mit einem SaveOptions-Objekt ändern.
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
