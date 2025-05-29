---
title: Watermark.SetText
linktitle: SetText
articleTitle: SetText
second_title: .NET için Aspose.Words
description: Belgelerinizi Watermark SetText yöntemimizle geliştirin. Profesyonel bir dokunuş için kolayca özelleştirilebilir metin filigranları ekleyin!
type: docs
weight: 40
url: /tr/net/aspose.words/watermark/settext/
---
## SetText(*string*) {#settext}

Belgeye Metin filigranı ekler.

```csharp
public void SetText(string text)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| text | String | Filigran olarak görüntülenen metin. |

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentOutOfRangeException | Metin uzunluğu aralık dışında olduğunda veya metin yalnızca boşluklar içerdiğinde fırlatılır. |
| ArgumentNullException | Metin olduğunda fırlatılır`hükümsüz` . |

## Notlar

Metin uzunluğu 1 ile 200 dahil aralığında olmalıdır. Metin,`hükümsüz` veya yalnızca boşluklar içerir.

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

* class [Watermark](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## SetText(*string, [TextWatermarkOptions](../../textwatermarkoptions/)*) {#settext_1}

Belgeye Metin filigranı ekler.

```csharp
public void SetText(string text, TextWatermarkOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| text | String | Filigran olarak görüntülenen metin. |
| options | TextWatermarkOptions | Metin filigranı için ek seçenekleri tanımlar. |

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentOutOfRangeException | Metin uzunluğu aralık dışında olduğunda veya metin yalnızca boşluklar içerdiğinde fırlatılır. |
| ArgumentNullException | Metin olduğunda fırlatılır`hükümsüz` . |

## Notlar

Metin uzunluğu 1 ile 200 dahil aralığında olmalıdır. Metin,`hükümsüz` veya yalnızca boşluklar içerir.

Eğer[`TextWatermarkOptions`](../../textwatermarkoptions/) dır`hükümsüz`, filigran varsayılan seçeneklerle ayarlanacaktır.

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

* class [TextWatermarkOptions](../../textwatermarkoptions/)
* class [Watermark](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
