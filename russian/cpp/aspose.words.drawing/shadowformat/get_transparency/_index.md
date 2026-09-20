---
title: "Метод Aspose::Words::Drawing::ShadowFormat::get_Transparency"
linktitle: "get_Transparency"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ShadowFormat::get_Transparency. Получает или задает степень прозрачности эффекта тени значением от 0.0 (непрозрачный) до 1.0 (полностью прозрачный). Значение по умолчанию — 0.0 в C++."
type: docs
weight: 2750
url: /ru/cpp/aspose.words.drawing/shadowformat/get_transparency/
---
## ShadowFormat::get_Transparency method


Получает или задает степень прозрачности эффекта тени как значение от 0.0 (непрозрачный) до 1.0 (прозрачный). Значение по умолчанию — 0.0.

```cpp
double Aspose::Words::Drawing::ShadowFormat::get_Transparency()
```


## Примеры



Показывает, как установить цвет с прозрачностью.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();
shadowFormat->set_Type(Aspose::Words::Drawing::ShadowType::Shadow21);
shadowFormat->set_Color(System::Drawing::Color::get_Red());
shadowFormat->set_Transparency(0.8);

doc->Save(get_ArtifactsDir() + u"Shape.ShadowFormatTransparency.docx");
```

## См. также

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
