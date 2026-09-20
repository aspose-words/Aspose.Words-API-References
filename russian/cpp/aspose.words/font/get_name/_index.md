---
title: "Метод Aspose::Words::Font::get_Name"
linktitle: "get_Name"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_Name. Получает или задает имя шрифта в C++."
type: docs
weight: 25000
url: /ru/cpp/aspose.words/font/get_name/
---
## Font::get_Name method


Получает или задаёт название шрифта.

```cpp
System::String Aspose::Words::Font::get_Name()
```

## Примечания


При получении возвращает [NameAscii](../get_nameascii/).

При установке задает [NameAscii](../get_nameascii/), [NameBi](../get_namebi/), [NameFarEast](../get_namefareast/) и [NameOther](../get_nameother/) указанным значением.

## Примеры



Показывает, как вставить отформатированный текст с помощью [DocumentBuilder](../../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Укажите форматирование шрифта, затем добавьте текст.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```


Показывает, как форматировать run текста, используя его свойство font.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
