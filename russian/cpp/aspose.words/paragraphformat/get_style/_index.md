---
title: "Метод Aspose::Words::ParagraphFormat::get_Style"
linktitle: "get_Style"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ParagraphFormat::get_Style. Получает или задает стиль абзаца, применяемый к этому форматированию в C++."
type: docs
weight: 35000
url: /ru/cpp/aspose.words/paragraphformat/get_style/
---
## ParagraphFormat::get_Style method


Получает или задает стиль абзаца, применяемый к этому форматированию.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::ParagraphFormat::get_Style()
```


## Примеры



Показывает, как создать и использовать абзацный стиль со списковой разметкой.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте пользовательский абзацный стиль.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Создайте список и убедитесь, что абзацы, использующие этот стиль, будут использовать этот список.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Примените абзацный стиль к текущему абзацу DocumentBuilder, а затем добавьте некоторый текст.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Измените стиль DocumentBuilder на такой, который не содержит форматирования списка, и напишите еще один абзац.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## См. также

* Class [Style](../../style/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
