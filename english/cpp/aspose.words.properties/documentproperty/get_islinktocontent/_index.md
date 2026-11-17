---
title: Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent method
linktitle: get_IsLinkToContent
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent method. Shows whether this property is linked to content or not in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.properties/documentproperty/get_islinktocontent/
---
## DocumentProperty::get_IsLinkToContent method


Shows whether this property is linked to content or not.

```cpp
bool Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent()
```


## Examples



Shows how to link a custom document property to a bookmark. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

// Link a new custom property to a bookmark. The value of this property
// will be the contents of the bookmark that it references in the "LinkSource" member.
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> customProperties = doc->get_CustomDocumentProperties();
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> customProperty = customProperties->AddLinkToContent(u"Bookmark", u"MyBookmark");

ASPOSE_ASSERT_EQ(true, customProperty->get_IsLinkToContent());
ASSERT_EQ(u"MyBookmark", customProperty->get_LinkSource());
ASPOSE_ASSERT_EQ(u"Hello world!", customProperty->get_Value());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

## See Also

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
