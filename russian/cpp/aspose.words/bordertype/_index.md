---
title: "Aspose::Words::BorderType перечисление"
linktitle: "BorderType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::BorderType перечисление. Указывает стороны границы. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 81000
url: /ru/cpp/aspose.words/bordertype/
---
## BorderType enum


Указывает стороны границы. Чтобы узнать больше, посетите статью документации [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
enum class BorderType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | -1 | Значение по умолчанию. |
| Низ | 0 | Указывает нижнюю границу абзаца или ячейки таблицы. |
| Слева | 1 | Указывает левую границу абзаца или ячейки таблицы. |
| Справа | 2 | Указывает правую границу абзаца или ячейки таблицы. |
| Верх | 3 | Указывает верхнюю границу абзаца или ячейки таблицы. |
| Горизонтальная | 4 | Указывает горизонтальную границу между ячейками в таблице или между согласованными абзацами. |
| Вертикальная | 5 | Указывает вертикальную границу между ячейками в таблице. |
| ДиагональВниз | 6 | Указывает диагональную границу в ячейке таблицы. |
| ДиагональВверх | 7 | Указывает диагональную границу в ячейке таблицы. |


## Примеры



Показывает, как вставить абзац с верхней границей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Устанавливайте ThemeColor только когда заданы LineWidth или LineStyle.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
