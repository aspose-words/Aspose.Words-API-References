---
title: Font.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: .NET için Aspose.Words
description: Metninizi Font ClearFormatting yöntemiyle orijinal stiline geri döndürün. Cilalı bir görünüm için temiz, tutarlı biçimlendirmenin tadını çıkarın!
type: docs
weight: 560
url: /tr/net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

Varsayılan yazı tipi biçimlendirmesine sıfırlar.

```csharp
public void ClearFormatting()
```

## Notlar

which nesnesinde açıkça belirtilen tüm yazı tipi biçimlendirmelerini kaldırır[`Font`](../) elde edildi, böylece yazı tipi biçimlendirmesi uygun üst öğeden miras alınacak.

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

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
