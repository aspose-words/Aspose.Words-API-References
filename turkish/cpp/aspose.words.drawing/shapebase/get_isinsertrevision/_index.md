---
title: "Aspose::Words::Drawing::ShapeBase::get_IsInsertRevision metodu"
linktitle: "get_IsInsertRevision"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_IsInsertRevision metodu. Bu nesne, C++'da değişiklik izleme etkinleştirilmişken Microsoft Word'e eklenmişse true döndürür."
type: docs
weight: 31000
url: /tr/cpp/aspose.words.drawing/shapebase/get_isinsertrevision/
---
## ShapeBase::get_IsInsertRevision method


Bu nesne, değişiklik izleme etkinken Microsoft Word'de eklenmişse true döndürür.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsInsertRevision()
```


## Örnekler



Revizyon şekilleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_TrackRevisions());

// Revizyonları izlemeksizin bir satır içi şekil ekleyin, bu şekli herhangi bir revizyon olmaktan çıkaracaktır.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Revizyonları izlemeyi başlatın ve ardından başka bir şekil ekleyin, bu bir revizyon olacaktır.
doc->StartTrackRevisions(u"John Doe");

shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Sun);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

shapes[0]->Remove();

// Değişiklikleri izlerken o şekli sildiğimiz için,
// şekil belgede kalır ve bir silme revizyonu olarak sayılır.
// Bu revizyonu kabul etmek şekli kalıcı olarak kaldıracak, reddetmek ise belgede tutacaktır.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Cube, shapes[0]->get_ShapeType());
ASSERT_TRUE(shapes[0]->get_IsDeleteRevision());

// Ve değişiklikleri izlerken başka bir şekil ekledik, bu yüzden o şekil bir ekleme revizyonu olarak sayılacak.
// Bu revizyonu kabul etmek bu şekli belgeye revizyon olmayan bir öğe olarak dahil edecektir,
// ve revizyonu reddetmek bu şekli kalıcı olarak kaldıracaktır.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Sun, shapes[1]->get_ShapeType());
ASSERT_TRUE(shapes[1]->get_IsInsertRevision());
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
