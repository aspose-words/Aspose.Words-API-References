---
title: "Aspose::Words::Drawing::ShapeBase::get_Name yöntemi"
linktitle: "get_Name"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_Name yöntemi. C++'da isteğe bağlı şekil adını alır veya ayarlar."
type: docs
weight: 40000
url: /tr/cpp/aspose.words.drawing/shapebase/get_name/
---
## ShapeBase::get_Name method


İsteğe bağlı şekil adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Name()
```

## Açıklamalar


Varsayılan boş dizedir.

**null** olamaz, ancak boş bir dize olabilir.

## Örnekler



Bir şeklin alternatif metninin nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 150, 150);
shape->set_Name(u"MyCube");

shape->set_AlternativeText(u"Alt text for MyCube.");

// Bir şekle sağ tıklayarak ve ardından "Format AutoShape" -> "Alt Text" yoluyla alternatif metnine erişebiliriz.
doc->Save(get_ArtifactsDir() + u"Shape.AltText.docx");

// Belgeyi HTML olarak kaydedin ve ardından şekle ait bağlı resmi silin.
// HTML'imizi okuyan tarayıcı, eksik resmin yerine alt metni gösterecektir.
doc->Save(get_ArtifactsDir() + u"Shape.AltText.html");
System::IO::File::Delete(get_ArtifactsDir() + u"Shape.AltText.001.png");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
