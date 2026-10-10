---
title: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent Methode"
linktitle: "AddLinkToContent"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent Methode. Erstellt eine neue, an Inhalte verknüpfte benutzerdefinierte Dokumenteigenschaft in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties::AddLinkToContent method


Erstellt eine neue, mit Inhalt verknüpfte benutzerdefinierte Dokumenteigenschaft.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent(const System::String &name, const System::String &linkSource)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | const System::String\& | Der Name der Eigenschaft. |
| linkSource | const System::String\& | Die Quelle der Eigenschaft. |

### ReturnValue

Das neu erstellte Eigenschaftsobjekt oder **null**, wenn *linkSource* ungültig ist.

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

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
