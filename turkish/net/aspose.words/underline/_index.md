---
title: Underline Enum
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words for .NET
description: Aspose.Words.Underline Sıralama. Fonta uygulanan alt çizginin türünü belirtir C#'da.
type: docs
weight: 6510
url: /tr/net/aspose.words/underline/
---
## Underline enumeration

Fonta uygulanan alt çizginin türünü belirtir.

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

Köprü alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Bir köprü ekleyin ve bunu özel biçimlendirmeyle vurgulayın.
// Köprü, bizi URL'de belirtilen konuma götürecek tıklanabilir bir metin parçası olacaktır.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Microsoft Word'deki metindeki bağlantıya Ctrl + sol tıklamak bizi yeni bir web tarayıcı penceresi aracılığıyla URL'ye götürecektir.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
