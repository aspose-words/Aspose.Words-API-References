---
title: "Aspose::Words::Markup::XmlMapping::get_StoreItemId method"
linktitle: "get_StoreItemId"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::XmlMapping::get_StoreItemId method. Gibt den benutzerdefinierten XML-Datenbezeichner für den benutzerdefinierten XML-Datenabschnitt an, der zur Auswertung des XPath-Ausdrucks in C++ verwendet werden soll."
type: docs
weight: 6000
url: /de/cpp/aspose.words.markup/xmlmapping/get_storeitemid/
---
## XmlMapping::get_StoreItemId method


Gibt den benutzerdefinierten XML-Datenbezeichner für den benutzerdefinierten XML-Datenabschnitt an, der zur Auswertung des [XPath](../get_xpath/) Ausdrucks verwendet werden soll.

```cpp
System::String Aspose::Words::Markup::XmlMapping::get_StoreItemId()
```


## Beispiele



Zeigt, wie man den benutzerdefinierten XML-Datenbezeichner eines XML-Abschnitts abruft.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom XML part in structured document tag.docx");

// Strukturierte Dokument-Tags haben IDs in Form von GUIDs.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 0, true));

ASSERT_EQ(u"{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag->get_XmlMapping()->get_StoreItemId());
```

## Siehe auch

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
