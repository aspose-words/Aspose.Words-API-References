---
title: "Метод Aspose::Words::Properties::DocumentProperty::get_LinkSource"
linktitle: "get_LinkSource"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Properties::DocumentProperty::get_LinkSource. Получает источник связанного пользовательского свойства документа в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.properties/documentproperty/get_linksource/
---
## DocumentProperty::get_LinkSource method


Получает источник связанного пользовательского свойства документа.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::get_LinkSource() const
```


## Примеры



Показывает, как связать пользовательское свойство документа с закладкой.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

// Свяжите новое пользовательское свойство с закладкой. Значение этого свойства
// будет содержимым закладки, на которую оно ссылается в члене "LinkSource".
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> customProperties = doc->get_CustomDocumentProperties();
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> customProperty = customProperties->AddLinkToContent(u"Bookmark", u"MyBookmark");

ASPOSE_ASSERT_EQ(true, customProperty->get_IsLinkToContent());
ASSERT_EQ(u"MyBookmark", customProperty->get_LinkSource());
ASPOSE_ASSERT_EQ(u"Hello world!", customProperty->get_Value());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

## См. также

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
