---
title: "Aspose::Words::Border::get_TintAndShade метод"
linktitle: "get_TintAndShade"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Border::get_TintAndShade метод. Получает или задает значение типа double, которое осветляет или затемняет цвет в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words/border/get_tintandshade/
---
## Border::get_TintAndShade method


Получает или задаёт двойное значение, которое осветляет или затемняет цвет.

```cpp
double Aspose::Words::Border::get_TintAndShade()
```

## Примечания


Допустимые значения находятся в диапазоне от -1 (самый темный) до 1 (самый светлый) для этого свойства. Ноль (0) — нейтральный.

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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
