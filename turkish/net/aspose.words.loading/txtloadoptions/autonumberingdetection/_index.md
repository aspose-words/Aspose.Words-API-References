---
title: TxtLoadOptions.AutoNumberingDetection
linktitle: AutoNumberingDetection
articleTitle: AutoNumberingDetection
second_title: Aspose.Words for .NET
description: TxtLoadOptions AutoNumberingDetection mülk. Bir belge yüklenirken otomatik numaralandırma algılamasının gerçekleştirileceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değerdoğru  C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

Bir belge yüklenirken otomatik numaralandırma algılamasının gerçekleştirileceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`doğru` .

```csharp
public bool AutoNumberingDetection { get; set; }
```

## Örnekler

Otomatik numaralandırma algılamasının nasıl devre dışı bırakılacağını gösterir.

```csharp
TxtLoadOptions options = new TxtLoadOptions { AutoNumberingDetection = false };
Document doc = new Document(MyDir + "Number detection.txt", options);
```

### Ayrıca bakınız

* class [TxtLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
