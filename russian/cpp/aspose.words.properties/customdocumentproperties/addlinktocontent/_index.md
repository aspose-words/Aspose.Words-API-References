---
title: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent метод"
linktitle: "AddLinkToContent"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent метод. Создаёт новое пользовательское свойство документа, связанное с содержимым, в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties::AddLinkToContent method


Создает новое пользовательское свойство документа, связанное с содержимым.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent(const System::String &name, const System::String &linkSource)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| name | const System::String\& | Имя свойства. |
| linkSource | const System::String\& | Источник свойства. |

### ReturnValue

Недавно созданный объект свойства или **null**, когда *linkSource* недействителен.

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

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
