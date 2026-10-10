---
title: "Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent Methode"
linktitle: "get_IsLinkToContent"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent Methode. Zeigt, ob diese Eigenschaft mit Inhalt verknüpft ist oder nicht in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.properties/documentproperty/get_islinktocontent/
---
## DocumentProperty::get_IsLinkToContent method


Zeigt, ob diese Eigenschaft mit Inhalt verknüpft ist oder nicht.

```cpp
bool Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent()
```


## Beispiele



Zeigt, wie man eine benutzerdefinierte Dokumenteigenschaft mit einem Lesezeichen verknüpft.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

// Verknüpfen Sie eine neue benutzerdefinierte Eigenschaft mit einem Lesezeichen. Der Wert dieser Eigenschaft
// ist der Inhalt des Lesezeichens, auf das im Mitglied "LinkSource" verwiesen wird.
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> customProperties = doc->get_CustomDocumentProperties();
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> customProperty = customProperties->AddLinkToContent(u"Bookmark", u"MyBookmark");

ASPOSE_ASSERT_EQ(true, customProperty->get_IsLinkToContent());
ASSERT_EQ(u"MyBookmark", customProperty->get_LinkSource());
ASPOSE_ASSERT_EQ(u"Hello world!", customProperty->get_Value());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

## Siehe auch

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
