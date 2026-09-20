---
title: "Метод Aspose::Words::PageSetup::get_PageHeight"
linktitle: "get_PageHeight"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::PageSetup::get_PageHeight. Возвращает или задает высоту страницы в пунктах в C++."
type: docs
weight: 33000
url: /ru/cpp/aspose.words/pagesetup/get_pageheight/
---
## PageSetup::get_PageHeight method


Возвращает или задает высоту страницы в пунктах.

```cpp
double Aspose::Words::PageSetup::get_PageHeight()
```


## Примеры



Показывает, как вставить изображение и использовать его в качестве водяного знака.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте изображение в верхний колонтитул, чтобы оно было видно на каждой странице.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// Разместите изображение в центре страницы.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```

## См. также

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
