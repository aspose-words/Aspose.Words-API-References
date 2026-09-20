---
title: "Aspose::Words::ParagraphFormat::get_LinesToDrop method"
linktitle: "get_LinesToDrop"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphFormat::get_LinesToDrop method. Получает или задает количество строк текста абзаца, используемых для расчёта высоты буквицы в C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words/paragraphformat/get_linestodrop/
---
## ParagraphFormat::get_LinesToDrop method


Получает или задает количество строк текста абзаца, используемых для расчёта высоты броской буквы.

```cpp
int32_t Aspose::Words::ParagraphFormat::get_LinesToDrop()
```


## Примеры



Показывает, как задать размер буквицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Измените свойство "LinesToDrop", чтобы обозначить абзац как букву‑капитель,
// что превратит его в большую заглавную букву, которая будет украшать следующий абзац.
// Установите для этого свойства значение 4, чтобы высота буквы‑капителя составляла четыре строки текста.
builder->get_ParagraphFormat()->set_LinesToDrop(4);
builder->Writeln(u"H");

// Сбросьте свойство "LinesToDrop" до 0, чтобы следующий абзац стал обычным.
// Текст в этом абзаце будет обтекать букву‑капитель.
builder->get_ParagraphFormat()->set_LinesToDrop(0);
builder->Writeln(u"ello world!");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LinesToDrop.odt");
```

## См. также

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
