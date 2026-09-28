---
title: "Aspose::Words::Border::get_ThemeColor метод"
linktitle: "get_ThemeColor"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Border::get_ThemeColor метод. Получает или задает цвет темы в применённой цветовой схеме, связанной с этим объектом Border в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words/border/get_themecolor/
---
## Border::get_ThemeColor method


Получает или задает цвет темы в применённой цветовой схеме, связанной с этим объектом [Border](../).

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Border::get_ThemeColor()
```


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

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
