---
title: "Aspose::Words::Drawing::ShapeBase::get_IsMoveFromRevision yöntemi"
linktitle: "get_IsMoveFromRevision"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_IsMoveFromRevision yöntemi. C++'ta değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse) true döndürür."
type: docs
weight: 33000
url: /tr/cpp/aspose.words.drawing/shapebase/get_ismovefromrevision/
---
## ShapeBase::get_IsMoveFromRevision method


Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (silinmiş) ise **true** döndürür.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsMoveFromRevision()
```


## Örnekler



Taşıma revizyon şekillerinin nasıl tanımlanacağını gösterir.
```cpp
// Bir taşıma revizyonu, Microsoft Word'de bir öğeyi kesip yapıştırarak belge gövdesinde bir öğeyi taşırken ortaya çıkar
// değişiklikleri izleme. Böyle bir metin hareketine satır içi bir şekil dahil edersek, o şekil de bir revizyon olacaktır.
// Kopyala-yapıştır veya yüzen şekilleri taşıma, taşıma revizyonları oluşturmaz.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision shape.docx");

// Taşıma revizyonları, "Move from" ve "Move to" revizyon çiftlerinden oluşur. Bu belgede bir şekil içinde taşıma yaptık,
// ancak taşıma revizyonunu kabul edip reddedene kadar, o şeklin iki örneği olacaktır.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// Bu, "Move to" revizyonudur, yani varış noktasındaki şekildir.
// Revizyonu kabul edersek, bu "Move to" revizyon şekli kaybolacaktır,
// ve "Move from" revizyon şekli kalacaktır.
ASSERT_FALSE(shapes[0]->get_IsMoveFromRevision());
ASSERT_TRUE(shapes[0]->get_IsMoveToRevision());

// Bu, "Move from" revizyonudur, yani orijinal konumundaki şekildir.
// Revizyonu kabul edersek, bu "Move from" revizyon şekli kaybolacaktır,
// ve "Move to" revizyon şekli kalacaktır.
ASSERT_TRUE(shapes[1]->get_IsMoveFromRevision());
ASSERT_FALSE(shapes[1]->get_IsMoveToRevision());
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
