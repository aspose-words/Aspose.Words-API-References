---
title: DocumentBuilder.PopFont
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. Daha önce yığına kaydedilmiş karakter biçimlendirmesini alır.
type: docs
weight: 560
url: /tr/net/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder.PopFont method

Daha önce yığına kaydedilmiş karakter biçimlendirmesini alır.

```csharp
public void PopFont()
```

### Örnekler

Bir belge oluşturucunun biçimlendirme yığınının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yazı tipi biçimlendirmesini ayarlayın, ardından köprüden önce gelen metni yazın.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Mevcut biçimlendirme yapılandırmamızı yığında koru.
builder.PushFont();

// Yeni bir stil uygulayarak oluşturucunun mevcut biçimlendirmesini değiştirin.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", yanlış);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Daha önce kaydettiğimiz yazı tipi biçimlendirmesini geri yükleyin ve öğeyi yığından kaldırın.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### Ayrıca bakınız

* property [Font](../font/)
* method [PushFont](../pushfont/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


