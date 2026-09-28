---
title: "Aspose::Words::Drawing::ShapeBase::get_AnchorLocked метод"
linktitle: "get_AnchorLocked"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::get_AnchorLocked метод. Указывает, заблокирована ли привязка фигуры в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.drawing/shapebase/get_anchorlocked/
---
## ShapeBase::get_AnchorLocked method


Указывает, зафиксирован ли якорь фигуры.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AnchorLocked()
```

## Примечания


Значение по умолчанию — **false**.

Имеет эффект только для фигур верхнего уровня.

Это свойство влияет на поведение привязки фигуры в Microsoft Word. Когда привязка не заблокирована, перемещение фигуры в Microsoft Word может также переместить её привязку.

## Примеры



Показывает, как заблокировать или разблокировать привязку абзаца фигуры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

builder->Write(u"Our shape will have an anchor attached to this paragraph.");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 160);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

builder->Writeln(u"Hello again!");

// Установите свойство "AnchorLocked" в "true", чтобы предотвратить привязку фигуры
// от перемещения при перемещении фигуры в Microsoft Word.
// Установите свойство "AnchorLocked" в "false", чтобы разрешить любое перемещение фигуры
// и также перемещать её привязку к любому другому абзацу, к которому фигура окажется близко.
shape->set_AnchorLocked(anchorLocked);

// Если у фигуры слева нет видимого символа привязки,
// нам потребуется включить видимые привязки через "Options" -> "Display" -> "Object Anchors".
doc->Save(get_ArtifactsDir() + u"Shape.AnchorLocked.docx");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
