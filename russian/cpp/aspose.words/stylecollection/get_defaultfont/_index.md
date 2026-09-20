---
title: "Aspose::Words::StyleCollection::get_DefaultFont метод"
linktitle: "get_DefaultFont"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::StyleCollection::get_DefaultFont метод. Получает форматирование текста документа по умолчанию в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/stylecollection/get_defaultfont/
---
## StyleCollection::get_DefaultFont method


Получает форматирование текста по умолчанию документа.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::StyleCollection::get_DefaultFont()
```

## Примечания


Обратите внимание, что настройки по умолчанию для всего документа были введены в Microsoft Word 2007 и полностью поддерживаются только в форматах OOXML ([Docx](../../loadformat/)). Ранние форматы документов имеют ограниченную поддержку этой функции, и могут сохранять только имена шрифтов.

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

* Class [Font](../../font/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
