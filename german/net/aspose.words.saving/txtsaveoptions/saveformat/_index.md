---
title: TxtSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die SaveFormat-Eigenschaft von TxtSaveOptions Dokumentspeicherformate definiert und so sicherstellt, dass Ihre Dateien immer im bevorzugten Textformat vorliegen.
type: docs
weight: 60
url: /de/net/aspose.words.saving/txtsaveoptions/saveformat/
---
## TxtSaveOptions.SaveFormat property

Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nurText .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Beispiele

Zeigt, wie ein TXT-Dokument mit einem benutzerdefinierten Absatzumbruch gespeichert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Erstellen Sie ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument im Klartext speichern.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// Setzen Sie „Absatzumbruch“ auf einen benutzerdefinierten Wert, den wir am Ende jedes Absatzes einfügen möchten.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TxtSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
