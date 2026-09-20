---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml метод"
linktitle: "get_SupportVml"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml метод. Получает или задает значение, указывающее, поддерживать ли VML‑изображения в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.loading/htmlloadoptions/get_supportvml/
---
## HtmlLoadOptions::get_SupportVml method


Получает или задает значение, указывающее, поддерживать ли изображения VML.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml() const
```


## Примеры



Показывает, как поддерживать условные комментарии при загрузке HTML‑документа.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Если значение истинно, то мы учитываем код VML при разборе загруженного документа.
loadOptions->set_SupportVml(supportVml);

// Этот документ содержит JPEG‑изображение внутри тегов "<!--[if gte vml 1]>",
// и другое PNG‑изображение внутри тегов "<![if !vml]>".
// Если установить флаг "SupportVml" в значение "true", то Aspose.Words загрузит JPEG.
// Если установить этот флаг в значение "false", то Aspose.Words загрузит только PNG.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## См. также

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
