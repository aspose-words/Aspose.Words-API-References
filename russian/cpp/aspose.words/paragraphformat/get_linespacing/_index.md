---
title: "Aspose::Words::ParagraphFormat::get_LineSpacing метод"
linktitle: "get_LineSpacing"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphFormat::get_LineSpacing метод. Получает или задает межстрочный интервал (в пунктах) для абзаца в C++."
type: docs
weight: 20000
url: /ru/cpp/aspose.words/paragraphformat/get_linespacing/
---
## ParagraphFormat::get_LineSpacing method


Получает или задает межстрочный интервал (в пунктах) для абзаца.

```cpp
double Aspose::Words::ParagraphFormat::get_LineSpacing()
```

## Примечания


Когда свойство [LineSpacingRule](../get_linespacingrule/) установлено в значение [AtLeast](../../linespacingrule/), межстрочный интервал может быть больше или равен, но никогда меньше указанного значения [LineSpacing](./).

Когда свойство [LineSpacingRule](../get_linespacingrule/) установлено в значение [Exactly](../../linespacingrule/), межстрочный интервал никогда не меняется от указанного значения [LineSpacing](./), даже если в абзаце используется более крупный шрифт.

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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
