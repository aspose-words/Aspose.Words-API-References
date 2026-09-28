---
title: "Метод Aspose::Words::Font::get_DoubleStrikeThrough"
linktitle: "get_DoubleStrikeThrough"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Font::get_DoubleStrikeThrough метод. True, если шрифт отформатирован как двойное перечёркивание текста в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words/font/get_doublestrikethrough/
---
## Font::get_DoubleStrikeThrough method


Истина, если шрифт отформатирован как двойное зачеркивание.

```cpp
bool Aspose::Words::Font::get_DoubleStrikeThrough()
```


## Примеры



Показывает, как добавить линию перечёркивания к тексту.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Text with a single-line strikethrough.");
run->get_Font()->set_StrikeThrough(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

para = System::ExplicitCast<Aspose::Words::Paragraph>(para->get_ParentNode()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));

run = System::MakeObject<Aspose::Words::Run>(doc, u"Text with a double-line strikethrough.");
run->get_Font()->set_DoubleStrikeThrough(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.StrikeThrough.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
