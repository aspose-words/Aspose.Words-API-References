---
title: "Aspose::Words::ParagraphFormat::get_LineSpacingRule method"
linktitle: "get_LineSpacingRule"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphFormat::get_LineSpacingRule method. Получает или задает межстрочный интервал для абзаца в C++."
type: docs
weight: 21000
url: /ru/cpp/aspose.words/paragraphformat/get_linespacingrule/
---
## ParagraphFormat::get_LineSpacingRule method


Получает или задает межстрочный интервал для абзаца.

```cpp
Aspose::Words::LineSpacingRule Aspose::Words::ParagraphFormat::get_LineSpacingRule()
```


## Примеры



Показывает, как работать с межстрочным интервалом.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже приведены три правила межстрочного интервала, которые мы можем определить, используя
// свойство "LineSpacingRule" абзаца для настройки интервала между абзацами.
// 1 -  Установить минимальное значение интервала.
// Это добавит вертикальный отступ к строкам текста любого размера
// которые слишком малы, чтобы поддерживать минимальную высоту строки.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::AtLeast);
builder->get_ParagraphFormat()->set_LineSpacing(20);

builder->Writeln(u"Minimum line spacing of 20.");
builder->Writeln(u"Minimum line spacing of 20.");

// 2 -  Установить точный интервал.
// Использование размеров шрифта, слишком больших для интервала, приведёт к усечению текста.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Exactly);
builder->get_ParagraphFormat()->set_LineSpacing(5);

builder->Writeln(u"Line spacing of exactly 5.");
builder->Writeln(u"Line spacing of exactly 5.");

// 3 -  Установить интервал как кратный значению стандартного межстрочного интервала, которое по умолчанию равно 12 пунктов.
// Такой тип интервала будет масштабироваться под разные размеры шрифта.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Multiple);
builder->get_ParagraphFormat()->set_LineSpacing(18);

builder->Writeln(u"Line spacing of 1.5 default lines.");
builder->Writeln(u"Line spacing of 1.5 default lines.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LineSpacing.docx");
```

## См. также

* Enum [LineSpacingRule](../../linespacingrule/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
