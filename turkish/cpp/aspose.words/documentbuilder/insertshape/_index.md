---
title: "Aspose::Words::DocumentBuilder::InsertShape method"
linktitle: "InsertShape"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertShape yöntemi. C++'da belirtilen konum, boyut ve metin kaydırma türüyle serbest yüzen şekil ekler."
type: docs
weight: 45000
url: /tr/cpp/aspose.words/documentbuilder/insertshape/
---
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Belirtilen konum, boyut ve metin kaydırma tipiyle serbest yüzen bir şekil ekler.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | Belgeye eklenecek şekil türü |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Şekle olan yatay mesafenin ölçüldüğü konumu belirtir. |
| left | double | Orijinden şeklin sol tarafına kadar olan mesafe (puan cinsinden). |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Şekle olan dikey mesafenin nereden ölçüldüğünü belirtir. |
| üst | double | Şeklin üst kenarına, orijinden nokta cinsinden olan mesafe. |
| genişlik | double | Şeklin genişliği nokta cinsinden. |
| yükseklik | double | Şeklin yüksekliği nokta cinsinden. |
| wrapType | Aspose::Words::Drawing::WrapType | Metnin şeklin etrafında nasıl sarılacağını belirtir. |

### ReturnValue

Ekleme yapılan şekil düğümü.

## Örnekler



Bir belgeye DML şekilleri nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda şekillerin sahip olabileceği iki sarma türü bulunmaktadır.
// 1 -  Yüzen:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  Satır içi:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// \"non-primitive\" şekiller oluşturmanız gerekiyorsa, örneğin SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, veya DiagonalCornersRounded,
// belgeyi \"Strict\" veya \"Transitional\" uyumlulukla kaydedin; bu, şeklin DML olarak kaydedilmesini sağlar.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, double, double) method


Belirtilen tip ve boyutta satır içi bir şekil ekler.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, double width, double height)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | Belgeye eklenecek şekil türü. |
| genişlik | double | Şeklin genişliği nokta cinsinden. |
| yükseklik | double | Şeklin yüksekliği nokta cinsinden. |

### ReturnValue

Ekleme yapılan şekil düğümü.

## Örnekler



Bir belgeye DML şekilleri nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda şekillerin sahip olabileceği iki sarma türü bulunmaktadır.
// 1 -  Yüzen:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  Satır içi:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// \"non-primitive\" şekiller oluşturmanız gerekiyorsa, örneğin SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, veya DiagonalCornersRounded,
// belgeyi \"Strict\" veya \"Transitional\" uyumlulukla kaydedin; bu, şeklin DML olarak kaydedilmesini sağlar.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
