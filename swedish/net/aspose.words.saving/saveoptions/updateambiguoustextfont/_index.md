---
title: SaveOptions.UpdateAmbiguousTextFont
linktitle: UpdateAmbiguousTextFont
articleTitle: UpdateAmbiguousTextFont
second_title: Aspose.Words för .NET
description: Förbättra textens tydlighet i PDF-filer med UpdateAmbiguousTextFont. Säkerställ korrekt teckensnittsrendering baserat på teckenkoder för bättre läsbarhet.
type: docs
weight: 150
url: /sv/net/aspose.words.saving/saveoptions/updateambiguoustextfont/
---
## SaveOptions.UpdateAmbiguousTextFont property

Avgör om teckensnittsattributen ska ändras beroende på den teckenkod som används.

```csharp
public bool UpdateAmbiguousTextFont { get; set; }
```

## Exempel

Visar hur man uppdaterar teckensnittet så att det matchar den teckenkod som används.

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
Console.WriteLine(run.Font.Name); // Angsana New
```

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
