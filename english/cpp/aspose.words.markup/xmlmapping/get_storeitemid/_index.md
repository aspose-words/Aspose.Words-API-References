---
title: Aspose::Words::Markup::XmlMapping::get_StoreItemId method
linktitle: get_StoreItemId
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::XmlMapping::get_StoreItemId method. Specifies the custom XML data identifier for the custom XML data part which shall be used to evaluate the XPath expression in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.markup/xmlmapping/get_storeitemid/
---
## XmlMapping::get_StoreItemId method


Specifies the custom XML data identifier for the custom XML data part which shall be used to evaluate the [XPath](../get_xpath/) expression.

```cpp
System::String Aspose::Words::Markup::XmlMapping::get_StoreItemId()
```


## Examples



Shows how to get the custom XML data identifier of an XML part. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Custom XML part in structured document tag.docx");

// Structured document tags have IDs in the form of GUIDs.
auto tag = System::DynamicCast<StructuredDocumentTag>(doc->GetChild(NodeType::StructuredDocumentTag, 0, true));

ASSERT_EQ(u"{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag->get_XmlMapping()->get_StoreItemId());
```

## See Also

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
