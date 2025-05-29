---
title: ParagraphFormat.WidowControl
linktitle: WidowControl
articleTitle: WidowControl
second_title: .NET için Aspose.Words
description: ParagraphFormat WidowControl özelliğinin metninizin ilk ve son satırlarının aynı sayfada birlikte kalmasını sağlayarak daha iyi okunabilirlik sağladığını keşfedin.
type: docs
weight: 410
url: /tr/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

Paragraftaki ilk ve son satırların paragrafın geri kalanıyla aynı sayfada kalması gerekiyorsa doğrudur.

```csharp
public bool WidowControl { get; set; }
```

## Örnekler

Bir paragraf için dul/yetim denetiminin nasıl etkinleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir sayfaya sığmayan bir yazıyı yazdığımızda, bir satır diğer sayfaya taşabilir.
// Bir sonraki sayfada yer alan tek satıra "Yetim" denir.
// ve yetimin ayrıldığı önceki satıra "Dul" adı verilir.
// Metni yazı tipi boyutu, aralık veya sayfa kenar boşlukları aracılığıyla yeniden düzenleyerek yetim ve dul yazıları düzeltebiliriz.
// Belgemizin boyutlarını korumak istiyorsak bu bayrağı "true" olarak ayarlayabiliriz
// dul kadınları yetim çocuklarıyla aynı kefeye koymak.
// Bu bayrağı "false" olarak bırakmak metinde dul/yetim çiftleri bırakacaktır.
// Her paragrafın bu ayarı Microsoft Word'de Giriş -> Paragraf -> Paragraf Ayarları yoluyla erişilebilir
// ("Paragraf" sekmesinin sağ alt köşesindeki düğme) -> "Dul/Yetim denetimi".
builder.ParagraphFormat.WidowControl = widowControl; 

// Yetim ve dul üreten metni ekle.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
