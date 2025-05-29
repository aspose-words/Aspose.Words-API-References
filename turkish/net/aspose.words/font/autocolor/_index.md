---
title: Font.AutoColor
linktitle: AutoColor
articleTitle: AutoColor
second_title: .NET için Aspose.Words
description: Font AutoColor özelliğini keşfedin, otomatik renk ayarlamaları için geçerli metin rengini (siyah veya beyaz) alın. Tasarımınızı zahmetsizce optimize edin!
type: docs
weight: 20
url: /tr/net/aspose.words/font/autocolor/
---
## Font.AutoColor property

'otomatik renk' için kullanılacak metnin (siyah veya beyaz) mevcut hesaplanmış rengini döndürür. Renk 'otomatik' değilse, o zaman şunu döndürür:[`Color`](../color/) .

```csharp
public Color AutoColor { get; }
```

## Notlar

Metin 'otomatik renk'e sahip olduğunda, metnin gerçek rengi otomatik olarak hesaplanır böylece arka plan rengine göre okunabilir olur. Arka plan rengini değiştirdiğinizde, metin rengi okunabilirliği en üst düzeye çıkarmak için MS Word'de otomatik olarak siyah veya beyaza dönüşür.

## Örnekler

Arka plan parlaklığına göre metin renginin otomatik olarak seçilmesiyle okunabilirliğin nasıl artırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir çalışmanın Font nesnesi metin rengini belirtmiyorsa, otomatik olarak
// Arkaplan renginin rengine bağlı olarak siyah veya beyazı seçin.
Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());

// Metnin varsayılan rengi siyahtır. Arkaplan rengi koyuysa, siyah metnin görülmesi zor olacaktır.
// Bu sorunu çözmek için AutoColor özelliği bu metni beyaz olarak gösterecektir.
builder.Font.Shading.BackgroundPatternColor = Color.DarkBlue;

builder.Writeln("The text color automatically chosen for this run is white.");

Assert.AreEqual(Color.White.ToArgb(), doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.AutoColor.ToArgb());

// Arkaplanı açık bir renge değiştirirsek, siyah daha hoş olacaktır.
// beyazdan daha uygun bir metin rengi, böylece otomatik renk siyah olarak gösterilecektir.
builder.Font.Shading.BackgroundPatternColor = Color.LightBlue;

builder.Writeln("The text color automatically chosen for this run is black.");

Assert.AreEqual(Color.Black.ToArgb(), doc.FirstSection.Body.Paragraphs[1].Runs[0].Font.AutoColor.ToArgb());

doc.Save(ArtifactsDir + "Font.SetFontAutoColor.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
