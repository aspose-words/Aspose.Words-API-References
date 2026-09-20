---
title: "Конструктор Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions"
linktitle: "XpsSaveOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Конструктор Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions. Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в формате Xps в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions::XpsSaveOptions() constructor


Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в формате [Xps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions()
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

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat) constructor


Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в формате [Xps](../../../aspose.words/saveformat/) или [OpenXps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


## Примеры



Показывает, как сохранить документ в формате XPS в виде книжного сгиба.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Создайте объект \"XpsSaveOptions\" объект, который мы можем передать методу \"Save\" документа
// чтобы изменить способ, которым этот метод преобразует документ в .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>(Aspose::Words::SaveFormat::Xps);

// Установите свойство \"UseBookFoldPrintingSettings\" в значение \"true\", чтобы расположить содержимое
// в выходном XPS таким образом, чтобы мы могли использовать его для создания брошюры.
// Установите свойство "UseBookFoldPrintingSettings" в "false", чтобы отрисовать XPS нормально.
xpsOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Если мы рендерим документ как буклет, мы должны установить \"MultiplePages\"
// свойства объектов настройки страницы всех разделов в "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
{
    for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
    {
        s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
    }
}

// После печати этого документа мы можем превратить его в брошюру, сложив страницы
// выходить из принтера и складываться пополам.
doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.BookFold.xps", xpsOptions);
```

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
