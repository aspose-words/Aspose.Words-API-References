---
title: "Aspose::Words::ParagraphFormat::get_Borders метод"
linktitle: "get_Borders"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphFormat::get_Borders метод. Получает коллекцию границ абзаца в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/paragraphformat/get_borders/
---
## ParagraphFormat::get_Borders method


Получает коллекцию границ абзаца.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::ParagraphFormat::get_Borders()
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

* Class [BorderCollection](../../bordercollection/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
