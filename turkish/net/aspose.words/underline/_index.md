---
title: Underline Enum
linktitle: Underline
articleTitle: Underline
second_title: .NET için Aspose.Words
description: Çok yönlü yazı tipi altını çizme seçenekleri için Aspose.Words.Underline enum'u keşfedin. Bugün özelleştirilebilir stillerle belge biçimlendirmenizi geliştirin!
type: docs
weight: 7360
url: /tr/net/aspose.words/underline/
---
## Underline enumeration

Bir yazı tipine uygulanan alt çizginin türünü belirtir.

```csharp
public enum Underline
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` |  |
| Single | `1` |  |
| Words | `2` |  |
| Double | `3` |  |
| Dotted | `4` |  |
| Thick | `6` |  |
| Dash | `7` |  |
| DashLong | `39` |  |
| DotDash | `9` |  |
| DotDotDash | `10` |  |
| Wavy | `11` |  |
| DottedHeavy | `20` |  |
| DashHeavy | `23` |  |
| DashLongHeavy | `55` |  |
| DotDashHeavy | `25` |  |
| DotDotDashHeavy | `26` |  |
| WavyHeavy | `27` |  |
| WavyDouble | `43` |  |

## Örnekler

Bir köprü metni alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Bir köprü metni ekleyin ve özel biçimlendirmeyle vurgulayın.
// Köprü metni, URL'de belirtilen yere bizi götürecek tıklanabilir bir metin parçası olacaktır.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", yanlış);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Microsoft Word'de metindeki bağlantıya Ctrl + sol tıklama bizi yeni bir web tarayıcısı penceresi aracılığıyla URL'ye götürecektir.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
