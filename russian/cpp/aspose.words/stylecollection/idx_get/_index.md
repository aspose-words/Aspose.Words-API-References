---
title: "Aspose::Words::StyleCollection::idx_get метод"
linktitle: "idx_get"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::StyleCollection::idx_get метод. Получает встроенный стиль по его независимому от локали идентификатору в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words/stylecollection/idx_get/
---
## StyleCollection::idx_get(Aspose::Words::StyleIdentifier) method


Получает встроенный стиль по его независимому от локали идентификатору.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(Aspose::Words::StyleIdentifier sti)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| sti | Aspose::Words::StyleIdentifier | Значение [StyleIdentifier](../../styleidentifier/), которое указывает встроенный стиль для получения. |
## Примечания


При обращении к стилю, которого ещё нет, он автоматически создаётся.

## Примеры



Показывает, как добавить [Style](../../style/) в коллекцию стилей документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Установите параметры по умолчанию для новых стилей, которые мы позже можем добавить в эту коллекцию.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Если мы добавим стиль типа "StyleType.Paragraph", коллекция применит значения
// его свойство "DefaultParagraphFormat" к свойству "ParagraphFormat" стиля.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Добавьте стиль и затем проверьте, что у него установлены настройки по умолчанию.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## См. также

* Class [Style](../../style/)
* Enum [StyleIdentifier](../../styleidentifier/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(const System::String\&) method


Получает стиль по имени или псевдониму.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(const System::String &name)
```

## Примечания


С учётом регистра, возвращает **null**, если стиль с указанным именем не найден.

Если это английское название встроенного стиля, которого ещё нет, он автоматически создаётся.

## Примеры



Показывает, когда необходимо пересчитать макет страниц документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Сохранение документа в PDF, в изображение или печать в первый раз будет автоматически
// кешировать макет документа в его страницах.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Измените документ каким-либо образом.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// В текущей версии Aspose.Words изменение документа не приводит к автоматическому пересозданию
// кешированный макет страницы. Если мы хотим, чтобы кешированный макет
// чтобы оставаться актуальным, нам придётся обновлять его вручную.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## См. также

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(int32_t) method


Получает стиль по индексу.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(int32_t index)
```


## Примеры



Показывает, как добавить [Style](../../style/) в коллекцию стилей документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Установите параметры по умолчанию для новых стилей, которые мы позже можем добавить в эту коллекцию.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Если мы добавим стиль типа "StyleType.Paragraph", коллекция применит значения
// его свойство "DefaultParagraphFormat" к свойству "ParagraphFormat" стиля.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Добавьте стиль и затем проверьте, что у него установлены настройки по умолчанию.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## См. также

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
