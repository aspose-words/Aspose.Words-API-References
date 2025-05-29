---
title: LoadOptions.MswVersion
linktitle: MswVersion
articleTitle: MswVersion
second_title: .NET için Aspose.Words
description: LoadOptions MswVersion ile belge yüklemeyi optimize edin. Sorunsuz entegrasyon için varsayılan olarak Word 2019'u kullanarak belirli MS Word sürümleriyle uyumluluğu sağlayın.
type: docs
weight: 100
url: /tr/net/aspose.words.loading/loadoptions/mswversion/
---
## LoadOptions.MswVersion property

Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesi gerektiğini belirtmenize olanak tanır. Varsayılan değerWord2019

```csharp
public MsWordVersion MswVersion { get; set; }
```

## Notlar

Yükleme işlemi sırasında farklı Word sürümleri belge içeriğinin ve biçimlendirmesinin belirli yönlerini biraz farklı şekilde işleyebilir ve bu da Belge Nesne Modelinde küçük farklılıklara neden olabilir.

## Örnekler

Belge yükleme sırasında belirli bir Microsoft Word sürümünün yükleme prosedürünün nasıl taklit edileceğini gösterir.

```csharp
// Varsayılan olarak Aspose.Words belgeleri Microsoft Word 2019 spesifikasyonuna göre yükler.
LoadOptions loadOptions = new LoadOptions();

Assert.AreEqual(MsWordVersion.Word2019, loadOptions.MswVersion);

// Bu belgede varsayılan paragraf biçimlendirme stili eksik.
// Bu varsayılan stil, belgeyi Microsoft Word veya Aspose.Words ile yüklediğimizde yeniden oluşturulacaktır.
loadOptions.MswVersion = MsWordVersion.Word2007;
Document doc = new Document(MyDir + "Document.docx", loadOptions);

// Stilin satır aralığı, Microsoft Word 2007 spesifikasyonuyla yüklendiğinde bu değere sahip olacaktır.
Assert.AreEqual(12.95d, doc.Styles.DefaultParagraphFormat.LineSpacing, 0.01d);
```

### Ayrıca bakınız

* enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
