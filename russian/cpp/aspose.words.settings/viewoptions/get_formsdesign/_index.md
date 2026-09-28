---
title: "Aspose::Words::Settings::ViewOptions::get_FormsDesign метод"
linktitle: "get_FormsDesign"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::ViewOptions::get_FormsDesign метод. Указывает, находится ли документ в режиме разработки форм в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.settings/viewoptions/get_formsdesign/
---
## ViewOptions::get_FormsDesign method


Указывает, находится ли документ в режиме разработки форм.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_FormsDesign() const
```

## Примечания


В настоящее время работает только с документами в формате WordML.

## Примеры



Показывает, как включить/выключить режим разработки форм.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Установите свойство "FormsDesign" в "false", чтобы оставить режим разработки форм отключённым.
// Установите свойство "FormsDesign" в "true", чтобы включить режим разработки форм.
doc->get_ViewOptions()->set_FormsDesign(useFormsDesign);

doc->Save(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml");

ASPOSE_ASSERT_EQ(useFormsDesign, System::IO::File::ReadAllText(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml").Contains(u"<w:formsDesign />"));
```

## См. также

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
