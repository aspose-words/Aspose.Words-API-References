---
title: DocumentBuilder.InsertShape
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. Belirtilen tür ve boyutta satır içi şekil ekler.
type: docs
weight: 410
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
| height | Double | Nokta cinsinden şeklin yüksekliği. |

### Geri dönüş değeri

Eklenen şekil düğümü.

### Örnekler

DML şekillerinin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda, şekillerin sahip olabileceği iki sarma türü bulunmaktadır.
// 1 - Kayan:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Satır içi:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped gibi "ilkel olmayan" şekiller oluşturmanız gerekiyorsa,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded veya DiagonalCornersRounded,
// daha sonra belgeyi, şeklin DML olarak kaydedilmesine izin veren "Strict" veya "Transitional" uyumluluğu ile kaydedin.
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

Belirtilen konum, boyut ve metin sarma türü ile serbest kayan şekil ekler.

```csharp
public Shape InsertShape(ShapeType shapeType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| shapeType | ShapeType | Belgeye eklenecek şekil türü |
| horzPos | RelativeHorizontalPosition | Şekle olan yatay uzaklığın nereden ölçüleceğini belirtir. |
| left | Double | Şeklin başlangıç noktasından sol tarafına nokta cinsinden uzaklık. |
| vertPos | RelativeVerticalPosition | Şekle olan dikey mesafenin nereden ölçüleceğini belirtir. |
| top | Double | Orijinden şeklin üst tarafına nokta cinsinden uzaklık. |
| width | Double | Nokta cinsinden şeklin genişliği. |
| height | Double | Nokta cinsinden şeklin genişliği. |
| wrapType | WrapType | Metnin şeklin etrafına nasıl kaydırılacağını belirtir. |

### Geri dönüş değeri

Eklenen şekil düğümü.

### Örnekler

DML şekillerinin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda, şekillerin sahip olabileceği iki sarma türü bulunmaktadır.
// 1 - Kayan:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Satır içi:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped gibi "ilkel olmayan" şekiller oluşturmanız gerekiyorsa,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded veya DiagonalCornersRounded,
// daha sonra belgeyi, şeklin DML olarak kaydedilmesine izin veren "Strict" veya "Transitional" uyumluluğu ile kaydedin.
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


