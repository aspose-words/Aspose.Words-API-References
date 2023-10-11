---
title: TextWatermarkOptions.FontSize
second_title: Aspose.Words for .NET API Referansı
description: TextWatermarkOptions mülk. Yazı tipi boyutunu alır veya ayarlar. Varsayılan değer 0dır  auto.
type: docs
weight: 40
url: /tr/net/aspose.words/textwatermarkoptions/fontsize/
---
## TextWatermarkOptions.FontSize property

Yazı tipi boyutunu alır veya ayarlar. Varsayılan değer 0'dır - auto.

```csharp
public float FontSize { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentOutOfRangeException | Bağımsız değişken geçerli değerler aralığının dışında olduğunda atar. |

### Notlar

Geçerli değerler 0 ila 65,5 (dahil) arasındadır.

Otomatik yazı tipi boyutu, filigranın sayfa kenar boşluklarına göre maksimum genişliğine ve maksimum yüksekliğine göre ölçeklendirileceği anlamına gelir.

### Örnekler

Metin filigranının nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Düz metin filigranı ekleyin.
doc.Watermark.SetText("Aspose Watermark");

// Metin formatını filigran olarak kullanarak düzenlemek istersek,
// filigranı oluştururken bir TextWatermarkOptions nesnesini ileterek bunu yapabiliriz.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Bunun gibi bir belgeden filigranı kaldırabiliriz.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Ayrıca bakınız

* class [TextWatermarkOptions](../)
* ad alanı [Aspose.Words](../../textwatermarkoptions/)
* toplantı [Aspose.Words](../../../)


