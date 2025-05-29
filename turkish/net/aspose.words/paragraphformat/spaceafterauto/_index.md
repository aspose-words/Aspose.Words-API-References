---
title: ParagraphFormat.SpaceAfterAuto
linktitle: SpaceAfterAuto
articleTitle: SpaceAfterAuto
second_title: .NET için Aspose.Words
description: ParagraphFormat SpaceAfterAuto özelliğini keşfedin. Daha temiz, daha profesyonel bir belge düzeni için paragraf aralığını otomatik olarak ayarlayın.
type: docs
weight: 320
url: /tr/net/aspose.words/paragraphformat/spaceafterauto/
---
## ParagraphFormat.SpaceAfterAuto property

Paragraftan sonraki boşluk miktarı otomatik olarak ayarlanıyorsa doğrudur.

```csharp
public bool SpaceAfterAuto { get; set; }
```

## Notlar

Ayarlandığında`doğru` , etkisini geçersiz kılar[`SpaceAfter`](../spaceafter/).

Paragraf Öncesi ve Sonrası Boşluk'u Otomatik olarak ayarladığınızda, Microsoft Word, aşağıdaki kurallara göre paragraflar arasına otomatik olarak 14 punto boşluk ekler :

* Normalde her paragraftan sonra boşluk eklenir.
* Madde işaretli veya numaralı listelerde, boşluk yalnızca listenin son öğesinden sonra eklenir. Liste öğeleri arasına boşluk eklenmez.
* İç içe madde işaretli veya numaralı listelerde boşluk eklenmez.
* Tablodan sonra genellikle boşluk eklenir.
* Tablo hücresinin son bloğu ise tablodan sonra boşluk eklenmez.
* Tablo hücresindeki son paragraftan sonra boşluk eklenmez.

## Örnekler

Otomatik paragraf aralığının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bu oluşturucunun oluşturacağı paragraflardan önce ve sonra büyük miktarda boşluk uygulayın.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Otomatik aralık uygulamak için bu bayrakları "true" olarak ayarlayın.
// yukarıda ayarladığımız özelliklerde boşlukları etkili bir şekilde görmezden geliyoruz.
// Bunları "false" olarak bırakmak özel paragraf aralığımızı uygulayacaktır.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Üst ve altlarında boşluk olacak şekilde iki paragraf ekleyin ve belgeyi kaydedin.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
