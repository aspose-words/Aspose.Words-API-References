---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes метод"
linktitle: "get_IgnoreShapes"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes метод. Получает или задает логическое значение, указывающее, следует ли игнорировать фигуры внутри текста. Значение по умолчанию — false в C++."
type: docs
weight: 11500
url: /ru/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreshapes/
---
## FindReplaceOptions::get_IgnoreShapes method


Получает или задает логическое значение, указывающее, следует ли игнорировать фигуры внутри текста. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes() const
```


## Примеры



Показывает, как игнорировать фигуры при замене текста.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Balloon, 200, 200);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

auto findReplaceOptions = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
findReplaceOptions->set_IgnoreShapes(true);
builder->get_Document()->get_Range()->Replace(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.", u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
ASSERT_EQ(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder->get_Document()->GetText().Trim());
```

## См. также

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
