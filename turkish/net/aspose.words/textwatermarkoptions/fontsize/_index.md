---
title: TextWatermarkOptions.FontSize
second_title: Aspose.Words for .NET API Referansı
description: TextWatermarkOptions mülk. Bir yazı tipi boyutunu alır veya ayarlar. Varsayılan değer 0  auto.
type: docs
weight: 40
url: /tr/net/aspose.words/textwatermarkoptions/fontsize/
---
## TextWatermarkOptions.FontSize property

Bir yazı tipi boyutunu alır veya ayarlar. Varsayılan değer 0 - auto.

```csharp
public float FontSize { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentOutOfRangeException | Bağımsız değişken geçerli değerler aralığının dışında olduğunda atar. |

### Notlar

Geçerli değerler 0 ile 65.5 arasında değişir.

Otomatik yazı tipi boyutu, filigranın sayfa kenar boşluklarına göre maksimum genişliğine ve maksimum yüksekliğine ölçekleneceği anlamına gelir.

### Örnekler

Metin filigranının nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Düz metin filigranı ekleyin.
doc.Watermark.SetText("Aspose Watermark");

// Metin biçimlendirmesini filigran olarak kullanarak düzenlemek istiyorsak,
// filigran oluştururken bir TextWatermarkOptions nesnesi ileterek bunu yapabiliriz.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Böyle bir belgeden bir filigranı kaldırabiliriz.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Ayrıca bakınız

* class [TextWatermarkOptions](../)
* ad alanı [Aspose.Words](../../textwatermarkoptions/)
* toplantı [Aspose.Words](../../../)


