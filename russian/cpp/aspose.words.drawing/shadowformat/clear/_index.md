---
title: "Метод Aspose::Words::Drawing::ShadowFormat::Clear"
linktitle: "Clear"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ShadowFormat::Clear. Очищает формат тени в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat::Clear method


Очищает формат тени.

```cpp
void Aspose::Words::Drawing::ShadowFormat::Clear()
```


## Примеры



Показывает, как работать с форматированием тени для фигуры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

if (shape->get_ShadowFormat()->get_Visible() && shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::Shadow2)
{
    shape->get_ShadowFormat()->set_Type(Aspose::Words::Drawing::ShadowType::Shadow7);
}

if (shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::ShadowMixed)
{
    shape->get_ShadowFormat()->Clear();
}
```

## См. также

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
