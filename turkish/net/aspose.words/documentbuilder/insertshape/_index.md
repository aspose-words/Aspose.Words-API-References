---
title: DocumentBuilder.InsertShape
linktitle: InsertShape
articleTitle: InsertShape
second_title: .NET için Aspose.Words
description: DocumentBuilder'ın InsertShape yöntemi ile özel satır içi şekilleri zahmetsizce ekleyin. Etkili sunumlar için belgelerinizi özel görsellerle geliştirin!
type: docs
weight: 460
url: /tr/net/aspose.words/documentbuilder/insertshape/
---
## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), double, double*) {#insertshape_1}

Belirtilen tür ve boyutta satır içi şekil ekler.

```csharp
public Shape InsertShape(ShapeType shapeType, double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| shapeType | ShapeType | Belgeye eklenecek şekil türü. |
| width | Double | Şeklin nokta cinsinden genişliği. |
| height | Double | Şeklin nokta cinsinden yüksekliği. |

### Geri dönüş değeri

Eklenen şekil düğümü.

## Örnekler

DML şekillerinin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda şekillerin sahip olabileceği iki sarma türü bulunmaktadır.
// 1 - Yüzen:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Satır içi:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped gibi "ilkel olmayan" şekiller oluşturmanız gerekiyorsa,
// ÜstKöşelerBirYuvarlakBirKesilmiş, TekKöşeYuvarlak, ÜstKöşelerYuvarlak veya ÇaprazKöşelerYuvarlak,
// daha sonra belgeyi "Sıkı" veya "Geçiş" uyumluluğuyla kaydedin, bu da şeklin DML olarak kaydedilmesine olanak tanır.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertshape}

Belirtilen konum, boyut ve metin kaydırma türüyle serbest yüzen şekil ekler.

```csharp
public Shape InsertShape(ShapeType shapeType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| shapeType | ShapeType | Belgeye eklenecek şekil türü |
| horzPos | RelativeHorizontalPosition | Şekle olan yatay mesafenin nereden ölçüleceğini belirtir. |
| left | Double | Şeklin başlangıç noktasından sol tarafına kadar olan mesafe. |
| vertPos | RelativeVerticalPosition | Şekle olan dikey mesafenin nereden ölçüleceğini belirtir. |
| top | Double | Şeklin başlangıç noktasından üst kenarına kadar olan mesafenin nokta cinsinden ifadesi. |
| width | Double | Şeklin nokta cinsinden genişliği. |
| height | Double | Şeklin nokta cinsinden yüksekliği. |
| wrapType | WrapType | Metnin şeklin etrafına nasıl sarılacağını belirtir. |

### Geri dönüş değeri

Eklenen şekil düğümü.

## Örnekler

DML şekillerinin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda şekillerin sahip olabileceği iki sarma türü bulunmaktadır.
// 1 - Yüzen:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Satır içi:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped gibi "ilkel olmayan" şekiller oluşturmanız gerekiyorsa,
// ÜstKöşelerBirYuvarlakBirKesilmiş, TekKöşeYuvarlak, ÜstKöşelerYuvarlak veya ÇaprazKöşelerYuvarlak,
// daha sonra belgeyi "Sıkı" veya "Geçiş" uyumluluğuyla kaydedin, bu da şeklin DML olarak kaydedilmesine olanak tanır.
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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
