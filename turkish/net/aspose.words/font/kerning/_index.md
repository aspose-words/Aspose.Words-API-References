---
title: Font.Kerning
linktitle: Kerning
articleTitle: Kerning
second_title: .NET için Aspose.Words
description: Font Kerning özelliğini keşfedin, optimum metin netliği ve tasarımı için kerning'in ne zaman başlayacağını kontrol edin. Tipografinizi hassasiyetle geliştirin!
type: docs
weight: 180
url: /tr/net/aspose.words/font/kerning/
---
## Font.Kerning property

Kerning'in başlayacağı yazı tipi boyutunu alır veya ayarlar.

```csharp
public double Kerning { get; set; }
```

## Örnekler

Kerning'in etkili olmaya başlayacağı yazı tipi boyutunun nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// Oluşturucunun yazı tipi boyutunu ve harf aralığının etkili olacağı minimum boyutu ayarlayın.
// Yazı tipi boyutu harf aralığı eşiğinin altına düştüğü için aşağıdaki satırda harf aralığı olmayacaktır.
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// Kerning eşiğini, oluşturucunun geçerli yazı tipi boyutunun üstünde olacak şekilde ayarlayın.
// Bu noktadan itibaren eklediğimiz her metne kerning uygulanacaktır. Karakterler arasındaki boşluklar
// ayarlanacak ve bu da normalde biraz daha estetik bir metin çalışmasıyla sonuçlanacaktır.
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
