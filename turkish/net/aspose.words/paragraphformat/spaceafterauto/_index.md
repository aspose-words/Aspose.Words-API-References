---
title: ParagraphFormat.SpaceAfterAuto
linktitle: SpaceAfterAuto
articleTitle: SpaceAfterAuto
second_title: Aspose.Words for .NET
description: ParagraphFormat SpaceAfterAuto mülk. Paragraftan sonraki boşluk miktarı otomatik olarak ayarlanıyorsa doğrudur C#'da.
type: docs
weight: 310
url: /tr/net/aspose.words/paragraphformat/spaceafterauto/
---
## ParagraphFormat.SpaceAfterAuto property

Paragraftan sonraki boşluk miktarı otomatik olarak ayarlanıyorsa doğrudur.

```csharp
public bool SpaceAfterAuto { get; set; }
```

## Notlar

olarak ayarlandığında`doğru` etkisini geçersiz kılar[`SpaceAfter`](../spaceafter/).

Paragraf Öncesindeki Boşluk ve Sonraki Boşluk'u Otomatik olarak ayarladığınızda, Microsoft Word, aşağıdaki kurallara göre paragraflar arasına otomatik olarak 14 puntoluk aralık ekler :

* Normalde tüm paragraflardan sonra boşluk eklenir.
* Madde işaretli veya numaralandırılmış listede boşluk yalnızca listedeki son öğeden sonra eklenir. Liste öğeleri arasına boşluk eklenmez.
* İç içe geçmiş madde işaretli veya numaralı listede boşluk eklenmez.
* Boşluk normalde tablodan sonra eklenir.
* Tablo hücresindeki son blok ise tablodan sonra boşluk eklenmez.
* Tablo hücresinde son paragraftan sonra boşluk eklenmez.

## Örnekler

Otomatik paragraf aralığının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bu oluşturucunun oluşturacağı paragraflardan önce ve sonra büyük miktarda boşluk uygulayın.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Otomatik aralık uygulamak için bu bayrakları "true" olarak ayarlayın,
// yukarıda belirlediğimiz özelliklerdeki boşlukları etkili bir şekilde yok sayıyoruz.
// Bunları "yanlış" olarak bırakın, özel paragraf aralığımız uygulanacaktır.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Altlarında ve üstlerinde boşluk olacak iki paragraf ekleyin ve belgeyi kaydedin.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
