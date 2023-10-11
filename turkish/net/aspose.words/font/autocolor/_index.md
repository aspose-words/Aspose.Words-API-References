---
title: Font.AutoColor
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Otomatik renk için kullanılacak metnin hesaplanmış mevcut rengini siyah veya beyaz döndürür. Renk otomatik değilse şunu döndürürColor .
type: docs
weight: 20
url: /tr/net/aspose.words/font/autocolor/
---
## Font.AutoColor property

'Otomatik renk' için kullanılacak metnin hesaplanmış mevcut rengini (siyah veya beyaz) döndürür. Renk 'otomatik' değilse şunu döndürür:[`Color`](../color/) .

```csharp
public Color AutoColor { get; }
```

### Notlar

Metnin 'otomatik rengi' olduğunda, metnin gerçek rengi otomatik olarak hesaplanır , böylece arka plan rengine göre okunabilir. Arka plan rengini değiştirdiğinizde, metin rengi, okunabilirliği en üst düzeye çıkarmak için MS Word'de otomatik olarak siyah veya beyaza geçecektir.

### Örnekler

Arka planın parlaklığına göre metin renginin otomatik olarak seçilmesiyle okunabilirliğin nasıl artırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir çalıştırmanın Font nesnesi metin rengini belirtmiyorsa, otomatik olarak
// arka plan rengine bağlı olarak siyah veya beyazı seçin.
Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());

// Metnin varsayılan rengi siyahtır. Arka planın rengi koyu ise siyah metnin görülmesi zor olacaktır.
// Bu sorunu çözmek için AutoColor özelliği bu metni beyaz renkte görüntüleyecektir.
builder.Font.Shading.BackgroundPatternColor = Color.DarkBlue;

builder.Writeln("The text color automatically chosen for this run is white.");

Assert.AreEqual(Color.White.ToArgb(), doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.AutoColor.ToArgb());

// Arka planı açık bir renkle değiştirirsek siyah daha fazla olur
// beyaz yerine uygun metin rengi, böylece otomatik renk siyah olarak görüntülenecektir.
builder.Font.Shading.BackgroundPatternColor = Color.LightBlue;

builder.Writeln("The text color automatically chosen for this run is black.");

Assert.AreEqual(Color.Black.ToArgb(), doc.FirstSection.Body.Paragraphs[1].Runs[0].Font.AutoColor.ToArgb());

doc.Save(ArtifactsDir + "Font.SetFontAutoColor.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


