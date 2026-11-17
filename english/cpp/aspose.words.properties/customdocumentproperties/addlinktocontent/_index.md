---
title: Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent method
linktitle: AddLinkToContent
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent method. Creates a new linked to content custom document property in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties::AddLinkToContent method


Creates a new linked to content custom document property.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent(const System::String & name, const System::String & linkSource)
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | const System::String \& | The name of the property. |
| linkSource | const System::String \& | The source of the property. |

### ReturnValue

The newly created property object or **null** when the linkSource is invalid.
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

ASPOSE_ASSERT_EQ(customProperty->get_IsLinkToContent(), true);
ASSERT_EQ(customProperty->get_LinkSource(), u"MyBookmark");
ASPOSE_ASSERT_EQ(customProperty->get_Value(), u"Hello world!");

doc->Save(get_ArtifactsDir() + u"DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```
## See Also

* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
