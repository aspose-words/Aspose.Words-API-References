---
title: "Перечисление Aspose::Words::BaselineAlignment"
linktitle: "BaselineAlignment"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::BaselineAlignment. Указывает вертикальное положение шрифтов на строке в C++."
type: docs
weight: 80500
url: /ru/cpp/aspose.words/baselinealignment/
---
## BaselineAlignment enum


Указывает вертикальное положение шрифтов в строке.

```cpp
enum class BaselineAlignment
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Верх | 0 | Выравнивает по верхнему краю каждого шрифта. |
| По центру | 1 | Выравнивает центральные точки каждого шрифта. |
| Базовая линия | 2 | Выравнивает по базовой линии абзаца. |
| Низ | 3 | Выравнивает по нижнему краю каждого шрифта. |
| Авто | 4 | Базовая линия регулируется автоматически. |


## Примеры



Показывает, как установить вертикальное положение шрифтов на строке.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();
if (format->get_BaselineAlignment() == Aspose::Words::BaselineAlignment::Auto)
{
    format->set_BaselineAlignment(Aspose::Words::BaselineAlignment::Top);
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphBaselineAlignment.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
