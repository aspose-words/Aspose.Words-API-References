---
title: "Aspose::Words::PageSetup::get_BorderSurroundsHeader метод"
linktitle: "get_BorderSurroundsHeader"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageSetup::get_BorderSurroundsHeader метод. Указывает, включает ли граница страницы заголовок или исключает его в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/pagesetup/get_bordersurroundsheader/
---
## PageSetup::get_BorderSurroundsHeader method


Указывает, включает ли граница страницы верхний колонтитул или исключает его.

```cpp
bool Aspose::Words::PageSetup::get_BorderSurroundsHeader()
```


## Примеры



Показывает, как применить границу к странице и верхнему/нижнему колонтитулу.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This is the main body text.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer.");
builder->MoveToDocumentEnd();

// Вставьте синюю двойную линию границы.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// Объект PageSetup секции имеет флаги \"BorderSurroundsHeader\" и \"BorderSurroundsFooter\", которые определяют
// окружает ли граница страницы основной текст, а также включает ли соответственно верхний или нижний колонтитул.
// Установите флаг \"BorderSurroundsHeader\" в значение \"true\", чтобы окружить верхний колонтитул нашей границей,
// а затем установите флаг \"BorderSurroundsFooter\", чтобы оставить нижний колонтитул за пределами границы.
pageSetup->set_BorderSurroundsHeader(true);
pageSetup->set_BorderSurroundsFooter(false);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorder.docx");
```

## См. также

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
