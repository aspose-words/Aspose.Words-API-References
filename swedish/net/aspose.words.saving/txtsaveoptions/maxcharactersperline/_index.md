---
title: TxtSaveOptions.MaxCharactersPerLine
linktitle: MaxCharactersPerLine
articleTitle: MaxCharactersPerLine
second_title: Aspose.Words för .NET
description: Upptäck TxtSaveOptions MaxCharactersPerLine, ställ enkelt in teckengränser per rad för bättre textformatering. Standardinställningen är 0 för obegränsat antal tecken.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/txtsaveoptions/maxcharactersperline/
---
## TxtSaveOptions.MaxCharactersPerLine property

Hämtar eller ställer in ett heltal som anger det maximala antalet tecken per rad. Standardvärdet är 0, det betyder ingen gräns.

```csharp
public int MaxCharactersPerLine { get; set; }
```

## Exempel

Visar hur man ställer in maximalt antal tecken per rad.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Ange max 30 tecken per rad.
TxtSaveOptions saveOptions = new TxtSaveOptions { MaxCharactersPerLine = 30 };

doc.Save(ArtifactsDir + "TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

### Se även

* class [TxtSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
