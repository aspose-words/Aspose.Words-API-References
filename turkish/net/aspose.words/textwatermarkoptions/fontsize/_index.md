---
title: TextWatermarkOptions.FontSize
linktitle: FontSize
articleTitle: FontSize
second_title: .NET için Aspose.Words
description: Ayarlanabilir FontSize ile TextWatermarkOptions'ınızı özelleştirin. Tasarımlarınızda optimum görünürlük ve stil için tercih ettiğiniz boyutu kolayca ayarlayın.
type: docs
weight: 40
url: /tr/net/aspose.words/textwatermarkoptions/fontsize/
---
## TextWatermarkOptions.FontSize property

Bir yazı tipi boyutu alır veya ayarlar. Varsayılan değer 0'dır - auto.

```csharp
public float FontSize { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentOutOfRangeException | Argüman geçerli değerler aralığının dışında olduğunda fırlatılır. |

## Notlar

Geçerli değerler 0 ile 65,5 arasındadır.

Otomatik yazı tipi boyutu, filigranın sayfa kenar boşluklarına göre maksimum genişliğine ve maksimum yüksekliğine ölçekleneceği anlamına gelir.

## Örnekler

Metin filigranının nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Düz metin filigranı ekleyin.
doc.Watermark.SetText("Aspose Watermark");

// Eğer metin biçimlendirmesini filigran olarak kullanarak düzenlemek istersek,
// filigranı oluştururken TextWatermarkOptions nesnesini geçirerek bunu yapabiliriz.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Bir belgeden filigranı şu şekilde kaldırabiliriz.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Ayrıca bakınız

* class [TextWatermarkOptions](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
