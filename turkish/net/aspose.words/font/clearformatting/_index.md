---
title: Font.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words for .NET
description: Font ClearFormatting yöntem. Varsayılan yazı tipi formatına sıfırlar C#'da.
type: docs
weight: 550
url: /tr/net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

Varsayılan yazı tipi formatına sıfırlar.

```csharp
public void ClearFormatting()
```

## Notlar

Where nesnesinde açıkça belirtilen tüm yazı tipi formatlarını kaldırır[`Font`](../) yazı tipi formatının uygun ebeveynden devralınması için elde edildi.

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

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
