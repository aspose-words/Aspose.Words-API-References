---
title: "Aspose::Words::LineSpacingRule enum"
linktitle: "LineSpacingRule"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LineSpacingRule enum. Указывает значения межстрочного интервала для абзаца в C++."
type: docs
weight: 95000
url: /ru/cpp/aspose.words/linespacingrule/
---
## LineSpacingRule enum


Указывает значения межстрочного интервала для абзаца.

```cpp
enum class LineSpacingRule
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| AtLeast | 0 | Межстрочный интервал может быть больше или равен, но никогда меньше значения, указанного в свойстве [LineSpacing](../paragraphformat/get_linespacing/). |
| Exactly | 1 | Межстрочный интервал никогда не меняется от значения, указанного в свойстве [LineSpacing](../paragraphformat/get_linespacing/), даже если в абзаце используется более крупный шрифт. |
| Multiple | 2 | Межстрочный интервал задаётся в свойстве [LineSpacing](../paragraphformat/get_linespacing/) как количество строк. Одна строка равна 12 пунктам. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
