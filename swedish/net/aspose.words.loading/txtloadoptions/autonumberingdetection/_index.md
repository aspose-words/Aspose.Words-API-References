---
title: TxtLoadOptions.AutoNumberingDetection
linktitle: AutoNumberingDetection
articleTitle: AutoNumberingDetection
second_title: Aspose.Words för .NET
description: TxtLoadOptions AutoNumberingDetection fast egendom. Hämtar eller ställer in ett booleskt värde som indikerar att antingen automatisk numreringsdetektering kommer att utföras när ett dokument laddas. Standardvärdet ärSann  i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

Hämtar eller ställer in ett booleskt värde som indikerar att antingen automatisk numreringsdetektering kommer att utföras när ett dokument laddas. Standardvärdet är`Sann` .

```csharp
public bool AutoNumberingDetection { get; set; }
```

## Exempel

Visar hur du inaktiverar automatisk numreringsdetektering.

```csharp
TxtLoadOptions options = new TxtLoadOptions { AutoNumberingDetection = false };
Document doc = new Document(MyDir + "Number detection.txt", options);
```

### Se även

* class [TxtLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
