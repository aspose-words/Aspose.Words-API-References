---
title: DocumentBuilder.PopFont
linktitle: PopFont
articleTitle: PopFont
second_title: Aspose.Words for .NET
description: DocumentBuilder PopFont yöntem. Daha önce yığına kaydedilen karakter formatını alır C#'da.
type: docs
weight: 590
url: /tr/net/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder.PopFont method

Daha önce yığına kaydedilen karakter formatını alır.

```csharp
public void PopFont()
```

## Örnekler

Belge oluşturucunun biçimlendirme yığınının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yazı tipi formatını ayarlayın, ardından köprüden önce gelen metni yazın.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Yığındaki mevcut biçimlendirme yapılandırmamızı koruyun.
builder.PushFont();

// Yeni bir stil uygulayarak oluşturucunun mevcut formatını değiştirin.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", false);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Daha önce kaydettiğimiz yazı tipi formatını geri yükleyin ve öğeyi yığından kaldırın.
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
