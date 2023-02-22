---
title: LoadOptions.MswVersion
second_title: Aspose.Words for .NET API Referansı
description: LoadOptions mülk. Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesi gerektiğini belirtmeye izin verir. Varsayılan değerWord2019
type: docs
weight: 100
url: /tr/net/aspose.words.loading/loadoptions/mswversion/
---
## LoadOptions.MswVersion property

Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesi gerektiğini belirtmeye izin verir. Varsayılan değerWord2019

```csharp
public MsWordVersion MswVersion { get; set; }
```

### Notlar

Farklı Word sürümleri, yükleme işlemi sırasında belge içeriğinin belirli yönlerini ve biçimlendirmeyi biraz farklı şekilde işleyebilir , bu da Belge Nesne Modelinde küçük farklılıklara neden olabilir.

### Örnekler

Belge yükleme sırasında belirli bir Microsoft Word sürümünün yükleme prosedürünün nasıl taklit edileceğini gösterir.

```csharp
// Varsayılan olarak Aspose.Words, belgeleri Microsoft Word 2019 spesifikasyonuna göre yükler.
LoadOptions loadOptions = new LoadOptions();

Assert.AreEqual(MsWordVersion.Word2019, loadOptions.MswVersion);

// Bu belgede varsayılan paragraf biçimlendirme stili eksik.
// Belgeyi Microsoft Word veya Aspose.Words ile yüklediğimizde bu varsayılan stil yeniden oluşturulacaktır.
loadOptions.MswVersion = MsWordVersion.Word2007;
Document doc = new Document(MyDir + "Document.docx", loadOptions);

// Stilin satır aralığı, Microsoft Word 2007 belirtimi tarafından yüklendiğinde bu değere sahip olacaktır.
Assert.AreEqual(12.95d, doc.Styles.DefaultParagraphFormat.LineSpacing, 0.01d);
```

### Ayrıca bakınız

* enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)


