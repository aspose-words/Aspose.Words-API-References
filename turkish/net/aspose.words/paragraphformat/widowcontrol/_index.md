---
title: ParagraphFormat.WidowControl
linktitle: WidowControl
articleTitle: WidowControl
second_title: Aspose.Words for .NET
description: ParagraphFormat WidowControl mülk. Paragraftaki ilk ve son satırlar paragrafın geri kalanıyla aynı sayfada kalacaksa doğrudur C#'da.
type: docs
weight: 400
url: /tr/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

Paragraftaki ilk ve son satırlar paragrafın geri kalanıyla aynı sayfada kalacaksa doğrudur.

```csharp
public bool WidowControl { get; set; }
```

## Örnekler

Bir paragraf için dul/yetim kontrolünün nasıl etkinleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir sayfaya sığmayan metni yazdığımızda bir satır diğer sayfaya taşabilir.
// Bir sonraki sayfada biten tek satıra "Yetim" denir,
// ve yetimin kesildiği önceki satıra "Dul" adı verilir.
// Metni yazı tipi boyutuna, aralığına veya sayfa kenar boşluklarına göre yeniden düzenleyerek yetimleri ve dulları düzeltebiliriz.
// Belgemizin boyutlarını korumak istiyorsak bu bayrağı "true" olarak ayarlayabiliriz
 // dulları kendi yetimleriyle aynı sayfaya yönlendirmek için.
// Bu bayrağı "yanlış" olarak bırakın, metinde dul/yetim çiftleri kalacaktır.
// Her paragrafta bu ayara Microsoft Word'de Ana Sayfa üzerinden erişilebilir -> Paragraf -> Paragraf Ayarları
// ("Paragraf" sekmesinin sağ alt köşesindeki düğme) -> "Dul/Yetim kontrolü".
builder.ParagraphFormat.WidowControl = widowControl; 

// Yetim ve dul bırakan metni ekleyin.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
