---
title: Font.Kerning
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Karakter aralığının başlayacağı yazı tipi boyutunu alır veya ayarlar.
type: docs
weight: 180
url: /tr/net/aspose.words/font/kerning/
---
## Font.Kerning property

Karakter aralığının başlayacağı yazı tipi boyutunu alır veya ayarlar.

```csharp
public double Kerning { get; set; }
```

### Örnekler

Karakter aralığının etkili olmaya başlayacağı yazı tipi boyutunun nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// Oluşturucunun yazı tipi boyutunu ve karakter aralığının etkili olacağı minimum boyutu ayarlayın.
// Yazı tipi boyutu karakter aralığı eşiğinin altına düşer, bu nedenle aşağıdaki çalıştırmada karakter aralığı olmayacaktır.
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// Karakter aralığı eşiğini, oluşturucunun geçerli yazı tipi boyutu bunun üzerinde olacak şekilde ayarlayın.
// Bu noktadan itibaren ekleyeceğimiz tüm metinlerde karakter aralığı uygulanacaktır. Karakterler arasındaki boşluklar
// ayarlanacak, normalde estetik açıdan biraz daha hoş bir metin akışı elde edilecek.
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


