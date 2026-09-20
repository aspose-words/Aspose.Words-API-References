---
title: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter метод"
linktitle: "MoveToHeaderFooter"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter метод. Перемещает курсор в начало заголовка или нижнего колонтитула в текущем разделе в C++."
type: docs
weight: 57000
url: /ru/cpp/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder::MoveToHeaderFooter method


Перемещает курсор в начало колонтитула или нижнего колонтитула в текущем разделе.

```cpp
void Aspose::Words::DocumentBuilder::MoveToHeaderFooter(Aspose::Words::HeaderFooterType headerFooterType)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Указывает заголовок или нижний колонтитул, к которому следует переместиться. |
## Примечания


После того как вы переместили курсор в заголовок или нижний колонтитул, вы можете использовать остальные методы [DocumentBuilder](../) для изменения содержимого заголовка или нижнего колонтитула.

Если вы хотите создать разные заголовки и нижние колонтитулы для первой страницы, вам нужно установить [DifferentFirstPageHeaderFooter](../../pagesetup/get_differentfirstpageheaderfooter/).

Если вы хотите создать разные заголовки и нижние колонтитулы для чётных и нечётных страниц, вам нужно установить [OddAndEvenPagesHeaderFooter](../../pagesetup/get_oddandevenpagesheaderfooter/).

Используйте [MoveToSection()](../movetosection/) чтобы выйти из заголовка в основной текст.

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

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
