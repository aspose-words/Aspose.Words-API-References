---
title: FileFormatUtil.SaveFormatToLoadFormat
linktitle: SaveFormatToLoadFormat
articleTitle: SaveFormatToLoadFormat
second_title: Aspose.Words för .NET
description: Konvertera enkelt SaveFormat till LoadFormat med FileFormatUtil-metoden. Förenkla filhanteringen och förbättra kompatibiliteten idag!
type: docs
weight: 90
url: /sv/net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

Konverterar en[`SaveFormat`](../../saveformat/) värde till en[`LoadFormat`](../../loadformat/) värde om möjligt.

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentException | Kastar när det inte går att konvertera. |

## Exempel

Visar hur man konverterar ett sparformat till motsvarande laddningsformat.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// Vissa filtyper kan ha dokument sparade i, men inte laddade från Aspose.Words.
// Om vi försöker konvertera ett sparformat av en sådan typ till ett laddningsformat, kommer ett undantag att utlösas.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### Se även

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
