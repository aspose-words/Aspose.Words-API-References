---
title: "Aspose::Words::Drawing::ShapeBase::get_ScreenTip yöntemi"
linktitle: "get_ScreenTip"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_ScreenTip yöntemi. Fare işaretçisi şeklin üzerine hareket ettiğinde gösterilen metni tanımlar C++ içinde."
type: docs
weight: 46000
url: /tr/cpp/aspose.words.drawing/shapebase/get_screentip/
---
## ShapeBase::get_ScreenTip method


Fare işaretçisi şeklin üzerine hareket ettiğinde gösterilen metni tanımlar.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_ScreenTip()
```

## Açıklamalar


Varsayılan değer boş bir dizedir.

## Örnekler



Bir resmi içeren ve aynı zamanda bir köprü olan şeklin nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_HRef(u"https://forum.aspose.com/");
shape->set_Target(u"New Window");
shape->set_ScreenTip(u"Aspose.Words Support Forums");

// Microsoft Word'de şekle Ctrl + sol tıklama yeni bir web tarayıcı penceresi açar
// ve bizi "HRef" özelliğindeki köprüye götürür.
doc->Save(get_ArtifactsDir() + u"Image.InsertImageWithHyperlink.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
