---
title: "Aspose::Words::ParagraphFormat::get_WidowControl метод"
linktitle: "get_WidowControl"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphFormat::get_WidowControl метод. True, если первая и последняя строки абзаца должны оставаться на той же странице, что и остальная часть абзаца, в C++."
type: docs
weight: 41000
url: /ru/cpp/aspose.words/paragraphformat/get_widowcontrol/
---
## ParagraphFormat::get_WidowControl method


True, если первая и последняя строки абзаца должны оставаться на той же странице, что и остальная часть абзаца.

```cpp
bool Aspose::Words::ParagraphFormat::get_WidowControl()
```


## Примеры



Показывает, как включить контроль вдов/сирот для абзаца.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Когда мы пишем текст, который не помещается на одну страницу, одна строка может перейти на следующую страницу.
// Одинокая строка, которая оказывается на следующей странице, называется "Orphan",
// а предыдущая строка, где "Orphan" обрывается, называется "Widow".
// Мы можем исправить сирот и вдов, переставив текст с помощью размера шрифта, интервалов или полей страницы.
// Если мы хотим сохранить размеры нашего документа, мы можем установить этот флаг в "true"
// чтобы переместить вдов на ту же страницу, что и их соответствующие сироты.
// Оставив этот флаг в значении "false", вы оставите пары вдова/сирота в тексте.
// Каждый абзац имеет эту настройку, доступную в Microsoft Word через Главная -> Абзац -> Параметры абзаца
// (кнопка в правом нижнем углу вкладки "Paragraph") -> "Widow/Orphan control".
builder->get_ParagraphFormat()->set_WidowControl(widowControl);

// Вставьте текст, который создает сироту и вдову.
builder->get_Font()->set_Size(68);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.WidowControl.docx");
```

## См. также

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
