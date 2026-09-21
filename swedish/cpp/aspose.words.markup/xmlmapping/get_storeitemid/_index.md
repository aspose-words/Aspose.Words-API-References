---
title: "Aspose::Words::Markup::XmlMapping::get_StoreItemId method"
linktitle: "get_StoreItemId"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::XmlMapping::get_StoreItemId method. Anger identifieraren för den anpassade XML-datan för den anpassade XML-deldelen som ska användas för att utvärdera XPath-uttrycket i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.markup/xmlmapping/get_storeitemid/
---
## XmlMapping::get_StoreItemId method


Anger identifieraren för den anpassade XML-datan för den anpassade XML-deldelen som ska användas för att utvärdera [XPath](../get_xpath/) uttrycket.

```cpp
System::String Aspose::Words::Markup::XmlMapping::get_StoreItemId()
```


## Exempel



Visar hur man hämtar identifieraren för den anpassade XML-datan för en XML-del.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom XML part in structured document tag.docx");

// Strukturerade dokumenttaggar har ID:n i form av GUID:er.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 0, true));

ASSERT_EQ(u"{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag->get_XmlMapping()->get_StoreItemId());
```

## Se även

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
