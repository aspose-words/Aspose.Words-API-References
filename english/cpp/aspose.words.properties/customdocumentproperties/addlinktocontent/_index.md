---
title: AddLinkToContent
second_title: Aspose.Words for C++ API Reference
description: Creates a new linked to content custom document property.
type: docs
weight: 14
url: /cpp/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties.AddLinkToContent method


Creates a new linked to content custom document property.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent(const System::String &name, const System::String &linkSource)
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | const System::String\& | The name of the property. |
| linkSource | const System::String\& | The source of the property. |

### ReturnValue


The newly created property object or null when the linkSource is invalid.

## Examples




Shows how to link a custom document property to a bookmark. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

// Link a new custom property to a bookmark. The value of this property
// will be the contents of the bookmark that it references in the "LinkSource" member.
SharedPtr<CustomDocumentProperties> customProperties = doc->get_CustomDocumentProperties();
SharedPtr<DocumentProperty> customProperty = customProperties->AddLinkToContent(u"Bookmark", u"MyBookmark");

ASPOSE_ASSERT_EQ(true, customProperty->get_IsLinkToContent());
ASSERT_EQ(u"MyBookmark", customProperty->get_LinkSource());
ASPOSE_ASSERT_EQ(u"Hello world!", customProperty->get_Value());

doc->Save(ArtifactsDir + u"DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

