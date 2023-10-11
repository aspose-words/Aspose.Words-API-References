---
title: DocumentBuilder.InsertShape
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. Belirtilen tür ve boyutta satır içi şekil ekler.
type: docs
weight: 440
url: /tr/net/aspose.words/documentbuilder/insertshape/
---
## InsertShape(ShapeType, double, double) {#insertshape_1}

Belirtilen tür ve boyutta satır içi şekil ekler.

```csharp
public Shape InsertShape(ShapeType shapeType, double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| shapeType | ShapeType | Belgeye eklenecek şekil türü. |
| width | Double | Nokta cinsinden şeklin genişliği. |
| height | Double | Şeklin nokta cinsinden yüksekliği. |

### Geri dönüş değeri

Eklenen şekil düğümü.

### Örnekler

DML şekillerinin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda şekillerin sahip olabileceği iki sarma türü verilmiştir.
// 1 - Kayan:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Satır içi:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped gibi "ilkel olmayan" şekiller oluşturmanız gerekiyorsa,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded veya DiagonalCornersRounded,
// daha sonra belgeyi, şeklin DML olarak kaydedilmesine olanak tanıyan "Katı" veya "Geçişli" uyumlulukla kaydedin.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertShape(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertshape}

Belirtilen konuma, boyuta ve metin sarma türüne sahip serbest kayan şekil ekler.

```csharp
public Shape InsertShape(ShapeType shapeType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| shapeType | ShapeType | Belgeye eklenecek şekil türü |
| horzPos | RelativeHorizontalPosition | Şekle olan yatay mesafenin nereden ölçüleceğini belirtir. |
| left | Double | Nokta cinsinden başlangıç noktasından şeklin sol tarafına olan uzaklık. |
| vertPos | RelativeVerticalPosition | Şekle olan dikey mesafenin nereden ölçüleceğini belirtir. |
| top | Double | Başlangıç noktasından şeklin üst kısmına kadar olan nokta cinsinden uzaklık. |
| width | Double | Nokta cinsinden şeklin genişliği. |
| height | Double | Nokta cinsinden şeklin genişliği. |
| wrapType | WrapType | Metnin şeklin etrafına nasıl sarılacağını belirtir. |

### Geri dönüş değeri

Eklenen şekil düğümü.

### Örnekler

DML şekillerinin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda şekillerin sahip olabileceği iki sarma türü verilmiştir.
// 1 - Kayan:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Satır içi:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped gibi "ilkel olmayan" şekiller oluşturmanız gerekiyorsa,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded veya DiagonalCornersRounded,
// daha sonra belgeyi, şeklin DML olarak kaydedilmesine olanak tanıyan "Katı" veya "Geçişli" uyumlulukla kaydedin.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


