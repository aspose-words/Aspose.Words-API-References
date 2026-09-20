---
title: "Aspose::Words::PageSetup::get_BottomMargin метод"
linktitle: "get_BottomMargin"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageSetup::get_BottomMargin метод. Возвращает или задает расстояние (в пунктах) между нижним краем страницы и нижней границей основного текста в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words/pagesetup/get_bottommargin/
---
## PageSetup::get_BottomMargin method


Возвращает или задает расстояние (в пунктах) между нижним краем страницы и нижней границей основного текста.

```cpp
double Aspose::Words::PageSetup::get_BottomMargin()
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
