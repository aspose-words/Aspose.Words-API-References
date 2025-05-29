---
title: DocumentBuilder.PopFont
linktitle: PopFont
articleTitle: PopFont
second_title: .NET için Aspose.Words
description: Karakter biçimlendirmesini yığından zahmetsizce geri yüklemek ve belge oluşturma sürecinizi geliştirmek için DocumentBuilder PopFont yöntemini keşfedin.
type: docs
weight: 630
url: /tr/net/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder.PopFont method

Yığında daha önce kaydedilmiş karakter biçimlendirmesini alır.

```csharp
public void PopFont()
```

## Örnekler

Bir belge oluşturucunun biçimlendirme yığınının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yazı tipi biçimlendirmesini ayarlayın, ardından köprü metninden önce gelecek metni yazın.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Yığındaki mevcut biçimlendirme yapılandırmamızı koruyalım.
builder.PushFont();

// Yeni bir stil uygulayarak oluşturucunun geçerli biçimlendirmesini değiştirin.
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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
