---
title: "Метод Aspose::Words::PageSetup::get_HeaderDistance"
linktitle: "get_HeaderDistance"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::PageSetup::get_HeaderDistance. Возвращает или задает расстояние (в пунктах) между заголовком и верхом страницы в C++."
type: docs
weight: 19000
url: /ru/cpp/aspose.words/pagesetup/get_headerdistance/
---
## PageSetup::get_HeaderDistance method


Возвращает или задает расстояние (в пунктах) между верхним колонтитулом и верхней границей страницы.

```cpp
double Aspose::Words::PageSetup::get_HeaderDistance()
```


## Примеры



Показывает, как настроить размер бумаги, ориентацию, поля и другие параметры раздела.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```

## См. также

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
