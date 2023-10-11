---
title: TxtSaveOptionsBase.ParagraphBreak
second_title: Aspose.Words für .NET-API-Referenz
description: TxtSaveOptionsBase eigendom. Gibt die Zeichenfolge an die beim Exportieren in Textformate als Absatzumbruch verwendet werden soll.
type: docs
weight: 40
url: /de/net/aspose.words.saving/txtsaveoptionsbase/paragraphbreak/
---
## TxtSaveOptionsBase.ParagraphBreak property

Gibt die Zeichenfolge an, die beim Exportieren in Textformate als Absatzumbruch verwendet werden soll.

```csharp
public string ParagraphBreak { get; set; }
```

### Bemerkungen

Der Standardwert ist[`CrLf`](../../../aspose.words/controlchar/crlf/).

### Beispiele

Zeigt, wie man ein TXT-Dokument mit einem benutzerdefinierten Absatzumbruch speichert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Erstelle ein „TxtSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument im Klartext speichern.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// Setzen Sie „ParagraphBreak“ auf einen benutzerdefinierten Wert, den wir am Ende jedes Absatzes einfügen möchten.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### Siehe auch

* class [TxtSaveOptionsBase](../)
* namensraum [Aspose.Words.Saving](../../txtsaveoptionsbase/)
* Montage [Aspose.Words](../../../)


