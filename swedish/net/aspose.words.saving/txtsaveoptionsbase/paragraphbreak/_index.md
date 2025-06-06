---
title: TxtSaveOptionsBase.ParagraphBreak
linktitle: ParagraphBreak
articleTitle: ParagraphBreak
second_title: Aspose.Words för .NET
description: Upptäck TxtSaveOptionsBases ParagraphBreak-egenskap, som möjliggör anpassade styckebrytningar för sömlös export av textformat. Förbättra läsbarheten i ditt dokument!
type: docs
weight: 40
url: /sv/net/aspose.words.saving/txtsaveoptionsbase/paragraphbreak/
---
## TxtSaveOptionsBase.ParagraphBreak property

Anger strängen som ska användas som styckebrytning vid export i textformat.

```csharp
public string ParagraphBreak { get; set; }
```

## Anmärkningar

Standardvärdet är[`CrLf`](../../../aspose.words/controlchar/crlf/).

## Exempel

Visar hur man sparar ett .txt-dokument med en anpassad styckebrytning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur vi sparar dokumentet som klartext.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// Ställ in "ParagraphBreak" till ett anpassat värde som vi vill placera i slutet av varje stycke.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### Se även

* class [TxtSaveOptionsBase](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
