---
title: DocumentBuilder.PushFont
linktitle: PushFont
articleTitle: PushFont
second_title: .NET için Aspose.Words
description: DocumentBuilder PushFont yönteminin, karakter stillerini kaydederek kolay erişim ve tutarlı tasarım yoluyla belge biçimlendirmenizi nasıl geliştirdiğini keşfedin.
type: docs
weight: 640
url: /tr/net/aspose.words/documentbuilder/pushfont/
---
## DocumentBuilder.PushFont method

Mevcut karakter biçimlendirmesini yığına kaydeder.

```csharp
public void PushFont()
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
* method [PopFont](../popfont/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
