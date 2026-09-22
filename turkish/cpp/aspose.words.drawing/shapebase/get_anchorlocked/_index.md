---
title: "Aspose::Words::Drawing::ShapeBase::get_AnchorLocked yöntemi"
linktitle: "get_AnchorLocked"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_AnchorLocked yöntemi. Şeklin bağlayıcısının C++'ta kilitli olup olmadığını belirtir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.drawing/shapebase/get_anchorlocked/
---
## ShapeBase::get_AnchorLocked method


Şeklin çapa noktasının kilitli olup olmadığını belirtir.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AnchorLocked()
```

## Açıklamalar


Varsayılan değer **false**'tur.

Yalnızca üst düzey şekiller için etkilidir.

Bu özellik, şeklin Microsoft Word'deki çapa davranışını etkiler. Çap kilitli olmadığında, Microsoft Word'de şekli hareket ettirmek, şeklin çapasını da hareket ettirebilir.

## Örnekler



Bir şeklin paragraf çapasını nasıl kilitleyeceğinizi veya kilidini açacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

builder->Write(u"Our shape will have an anchor attached to this paragraph.");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 160);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

builder->Writeln(u"Hello again!");

// Şeklin çapasını önlemek için "AnchorLocked" özelliğini "true" olarak ayarlayın
// Microsoft Word'de şekli hareket ettirirken çapanın hareket etmesini önlemek için.
// Şeklin herhangi bir hareketine izin vermek için "AnchorLocked" özelliğini "false" olarak ayarlayın
// Aynı zamanda çapasını, şeklin yaklaştığı herhangi bir diğer paragrafın üzerine de taşıyabilmesi için.
shape->set_AnchorLocked(anchorLocked);

// Şeklin sol tarafında görünür bir çapa simgesi yoksa,
// Görünür çapa "Options" -> "Display" -> "Object Anchors" yoluyla etkinleştirmemiz gerekir.
doc->Save(get_ArtifactsDir() + u"Shape.AnchorLocked.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
