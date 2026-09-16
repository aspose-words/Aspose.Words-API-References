---
title: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent 方法"
linktitle: "AddLinkToContent"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent 方法。在 C++ 中创建一个新的链接到内容的自定义文档属性。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties::AddLinkToContent method


创建一个新的链接到内容的自定义文档属性。

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent(const System::String &name, const System::String &linkSource)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 属性的名称。 |
| linkSource | const System::String\& | 属性的来源。 |

### ReturnValue

当 *linkSource* 无效时，新创建的属性对象或 **null**。

## 示例



展示如何将自定义文档属性链接到书签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

// 将新的自定义属性链接到书签。此属性的值
// 将是它在 \"LinkSource\" 成员中引用的书签的内容。
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> customProperties = doc->get_CustomDocumentProperties();
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> customProperty = customProperties->AddLinkToContent(u"Bookmark", u"MyBookmark");

ASPOSE_ASSERT_EQ(true, customProperty->get_IsLinkToContent());
ASSERT_EQ(u"MyBookmark", customProperty->get_LinkSource());
ASPOSE_ASSERT_EQ(u"Hello world!", customProperty->get_Value());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

## 另见

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
