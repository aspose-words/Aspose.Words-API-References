---
title: TxtLoadOptions.AutoNumberingDetection
linktitle: AutoNumberingDetection
articleTitle: AutoNumberingDetection
second_title: .NET için Aspose.Words
description: TxtLoadOptions' AutoNumberingDetection özelliğini keşfedin. Sorunsuz belge yüklemesi için otomatik numaralandırmayı kolayca etkinleştirin veya devre dışı bırakın. Varsayılan değer true'dur.
type: docs
weight: 20
url: /tr/net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

Bir belge yüklenirken otomatik numaralandırma algılamasının yapılıp yapılmayacağını belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`doğru` .

```csharp
public bool AutoNumberingDetection { get; set; }
```

## Örnekler

Otomatik numaralandırma algılamanın nasıl devre dışı bırakılacağını gösterir.

```csharp
TxtLoadOptions options = new TxtLoadOptions { AutoNumberingDetection = false };
Document doc = new Document(MyDir + "Number detection.txt", options);
```

### Ayrıca bakınız

* class [TxtLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
