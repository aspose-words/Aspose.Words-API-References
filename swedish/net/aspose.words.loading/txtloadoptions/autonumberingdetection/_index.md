---
title: TxtLoadOptions.AutoNumberingDetection
linktitle: AutoNumberingDetection
articleTitle: AutoNumberingDetection
second_title: Aspose.Words för .NET
description: Upptäck TxtLoadOptions egenskap AutoNumberingDetection. Aktivera eller inaktivera enkelt automatisk numrering för sömlös dokumentinläsning. Standardvärdet är sant.
type: docs
weight: 20
url: /sv/net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

Hämtar eller ställer in ett booleskt värde som anger att antingen automatisk numreringsdetektering kommer att utföras när ett dokument laddas. Standardvärdet är`sann` .

```csharp
public bool AutoNumberingDetection { get; set; }
```

## Exempel

Visar hur man inaktiverar automatisk numreringsidentifiering.

```csharp
TxtLoadOptions options = new TxtLoadOptions { AutoNumberingDetection = false };
Document doc = new Document(MyDir + "Number detection.txt", options);
```

### Se även

* class [TxtLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
