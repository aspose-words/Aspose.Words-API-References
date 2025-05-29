---
title: SaveOptions.UpdateAmbiguousTextFont
linktitle: UpdateAmbiguousTextFont
articleTitle: UpdateAmbiguousTextFont
second_title: Aspose.Words für .NET
description: Verbessern Sie die Textklarheit in PDF-Dateien mit UpdateAmbiguousTextFont. Sorgen Sie für eine präzise Schriftdarstellung basierend auf Zeichencodes für bessere Lesbarkeit.
type: docs
weight: 150
url: /de/net/aspose.words.saving/saveoptions/updateambiguoustextfont/
---
## SaveOptions.UpdateAmbiguousTextFont property

Bestimmt, ob die Schriftattribute entsprechend dem verwendeten Zeichencode geändert werden.

```csharp
public bool UpdateAmbiguousTextFont { get; set; }
```

## Beispiele

Zeigt, wie die Schriftart aktualisiert wird, damit sie dem verwendeten Zeichencode entspricht.

```csharp
Document doc = new Document(MyDir + "Special symbol.docx");
Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
Console.WriteLine(run.Text); // ฿
Console.WriteLine(run.Font.Name); // Arial

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateAmbiguousTextFont = true;
doc.Save(ArtifactsDir + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx");
run = doc.FirstSection.Body.FirstParagraph.Runs[0];
Console.WriteLine(run.Text); // ฿
Console.WriteLine(run.Font.Name); // Angsana Neu
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
