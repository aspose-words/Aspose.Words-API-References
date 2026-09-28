---
title: "Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle метод"
linktitle: "get_NoSpaceBetweenParagraphsOfSameStyle"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle метод. Когда **true**, SpaceBefore и SpaceAfter будут игнорироваться между абзацами одного и того же стиля в C++."
type: docs
weight: 25000
url: /ru/cpp/aspose.words/paragraphformat/get_nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle method


Когда **true**, [SpaceBefore](../get_spacebefore/) и [SpaceAfter](../get_spaceafter/) будут игнорироваться между абзацами одного и того же стиля.

```cpp
bool Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle()
```

## Примечания


Этот параметр действует только при применении к стилю абзаца. Если применить его непосредственно к абзацу, он не оказывает влияния.

## Примеры



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
