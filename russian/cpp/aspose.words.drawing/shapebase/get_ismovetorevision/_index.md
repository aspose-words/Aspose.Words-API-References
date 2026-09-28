---
title: "Метод Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision"
linktitle: "get_IsMoveToRevision"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision. Возвращает true, если этот объект был перемещён (вставлен) в Microsoft Word при включённом отслеживании изменений в C++."
type: docs
weight: 34000
url: /ru/cpp/aspose.words.drawing/shapebase/get_ismovetorevision/
---
## ShapeBase::get_IsMoveToRevision method


Возвращает **true**, если этот объект был перемещён (вставлен) в Microsoft Word при включённом отслеживании изменений.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision()
```


## Примеры



Показывает, как определить фигуры перемещения ревизий.
```cpp
// Перемещение ревизии происходит, когда мы перемещаем элемент в теле документа с помощью вырезания и вставки в Microsoft Word, пока
// отслеживание изменений. Если мы включаем встроенную форму в такое перемещение текста, эта форма также будет ревизией.
// Копирование и вставка или перемещение плавающих форм не создают перемещающих ревизий.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision shape.docx");

// Перемещающие ревизии состоят из пар ревизий \"Move from\" и \"Move to\". Мы переместили в этом документе одну форму,
// но пока мы не примем или не отклоним перемещающую ревизию, будет две копии этой формы.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// Это ревизия \"Move to\", которая представляет форму в месте её назначения.
// Если мы примем ревизию, форма ревизии \"Move to\" исчезнет,
// а форма ревизии \"Move from\" останется.
ASSERT_FALSE(shapes[0]->get_IsMoveFromRevision());
ASSERT_TRUE(shapes[0]->get_IsMoveToRevision());

// Это ревизия \"Move from\", которая представляет форму в её исходном месте.
// Если мы примем ревизию, форма ревизии \"Move from\" исчезнет,
// а форма ревизии \"Move to\" останется.
ASSERT_TRUE(shapes[1]->get_IsMoveFromRevision());
ASSERT_FALSE(shapes[1]->get_IsMoveToRevision());
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
