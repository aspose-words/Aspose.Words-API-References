---
title: TxtSaveOptionsBase.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: .NET için Aspose.Words
description: TxtSaveOptionsBase'in Kodlama özelliğiyle metin dışa aktarımlarını nasıl optimize edeceğinizi keşfedin. Sorunsuz UTF-8 metin biçimlendirmesi için kodlama seçeneklerini kolayca ayarlayın.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/txtsaveoptionsbase/encoding/
---
## TxtSaveOptionsBase.Encoding property

Metin biçimlerinde dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer**Kodlama.UTF8** .

```csharp
public Encoding Encoding { get; set; }
```

## Örnekler

.txt çıktı belgesi için kodlamanın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// ASCII karakter setinin dışındaki karakterlerle biraz metin ekleyin.
builder.Write("À È Ì Ò Ù.");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "TxtSaveOptions" nesnesi oluşturun
// Belgeyi düz metne nasıl kaydedeceğimizi değiştirmek için.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// "Kodlama" özelliğinin belgemizin içeriğine uygun kodlamayı içerdiğini doğrulayın.
Assert.AreEqual(System.Text.Encoding.UTF8, txtSaveOptions.Encoding);

doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt", txtSaveOptions);

string docText = System.Text.Encoding.UTF8.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt"));

Assert.AreEqual("\uFEFFÀ È Ì Ò Ù.\r\n", docText);

// Uygun olmayan bir kodlamanın kullanılması belge içeriğinin kaybolmasına neden olabilir.
txtSaveOptions.Encoding = System.Text.Encoding.ASCII;
doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt", txtSaveOptions);
docText = System.Text.Encoding.ASCII.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt"));

Assert.AreEqual("? ? ? ? ?.\r\n", docText);
```

### Ayrıca bakınız

* class [TxtSaveOptionsBase](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
