---
title: "Метод Aspose::Words::Saving::XpsSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::XpsSaveOptions::get_SaveFormat. Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. Может быть только Xps в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/xpssaveoptions/get_saveformat/
---
## XpsSaveOptions::get_SaveFormat method


Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. Может быть только [Xps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::XpsSaveOptions::get_SaveFormat() override
```


## Примеры



Показывает, как ограничить уровень заголовков, которые будут отображаться в структуре сохранённого XPS‑документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте заголовки, которые могут служить элементами оглавления уровней 1, 2 и затем 3.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// Создайте объект \"XpsSaveOptions\" объект, который мы можем передать методу \"Save\" документа
// чтобы изменить способ, которым этот метод преобразует документ в .XPS.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// Выходной XPS‑документ будет содержать структуру, оглавление, в котором перечислены заголовки в теле документа.
// Щелчок по элементу этой структуры перенесёт нас к месту соответствующего заголовка.
// Установите свойство \"HeadingsOutlineLevels\" в значение \"2\" , чтобы исключить из структуры все заголовки уровнем выше 2.
// Последние два заголовка, которые мы вставили выше, не появятся.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
