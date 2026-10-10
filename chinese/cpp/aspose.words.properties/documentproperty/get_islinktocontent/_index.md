---
title: "Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent 方法"
linktitle: "get_IsLinkToContent"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent 方法。显示此属性是否链接到内容（在 C++ 中）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.properties/documentproperty/get_islinktocontent/
---
## DocumentProperty::get_IsLinkToContent method


显示此属性是否链接到内容。

```cpp
bool Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent()
```


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

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
