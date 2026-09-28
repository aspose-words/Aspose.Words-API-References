---
title: "Aspose::Words::StyleCollection::get_Count метод"
linktitle: "get_Count"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::StyleCollection::get_Count метод. Получает количество стилей в коллекции в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/stylecollection/get_count/
---
## StyleCollection::get_Count method


Получает количество стилей в коллекции.

```cpp
int32_t Aspose::Words::StyleCollection::get_Count()
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

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
