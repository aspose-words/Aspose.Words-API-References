---
title: "Aspose::Words::ParagraphFormat::get_SpaceBefore method"
linktitle: "get_SpaceBefore"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphFormat::get_SpaceBefore method. Получает или задает количество интервала (в пунктах) перед абзацем в C++."
type: docs
weight: 33000
url: /ru/cpp/aspose.words/paragraphformat/get_spacebefore/
---
## ParagraphFormat::get_SpaceBefore method


Получает или задает величину интервала (в пунктах) перед абзацем.

```cpp
double Aspose::Words::ParagraphFormat::get_SpaceBefore()
```

## Примечания


Не оказывает влияния, когда [SpaceBeforeAuto](../get_spacebeforeauto/) **true**.

Допустимые значения находятся в диапазоне от 0 до 1584 включительно.

## Примеры



Показывает, как установить автоматический интервал абзаца.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Примените большое количество отступов до и после абзацев, которые будет создавать этот построитель.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Установите эти флаги в "true", чтобы применить автоматический интервал,
// фактически игнорируя интервалы в свойствах, которые мы задали выше.
// Оставьте их как "false", и будет применён наш пользовательский интервал абзаца.
builder->get_ParagraphFormat()->set_SpaceAfterAuto(autoSpacing);
builder->get_ParagraphFormat()->set_SpaceBeforeAuto(autoSpacing);

// Вставьте два абзаца, у которых будет интервал сверху и снизу, и сохраните документ.
builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingAuto.docx");
```


Показывает, как применить отсутствие отступов между абзацами с одинаковым стилем.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Примените большое количество отступов до и после абзацев, которые будет создавать этот построитель.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Установите флаг "NoSpaceBetweenParagraphsOfSameStyle" в значение "true", чтобы применить
// отсутствие отступов между абзацами с одинаковым стилем, что сгруппирует похожие абзацы.
// Оставьте флаг "NoSpaceBetweenParagraphsOfSameStyle" со значением "false"
// чтобы равномерно применить отступы к каждому абзацу.
builder->get_ParagraphFormat()->set_NoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Quote"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

## См. также

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
