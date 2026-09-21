---
title: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent metod"
linktitle: "AddLinkToContent"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent metod. Skapar en ny anpassad dokumentegenskap länkad till innehåll i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties::AddLinkToContent method


Skapar en ny anpassad dokumentegenskap som är länkad till innehåll.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent(const System::String &name, const System::String &linkSource)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| namn | const System::String\& | Namnet på egenskapen. |
| linkSource | const System::String\& | Källan till egenskapen. |

### ReturnValue

Det nyss skapade egenskapsobjektet eller **null** när *linkSource* är ogiltig.

## Exempel



Visar hur man länkar en anpassad dokumentegenskap till ett bokmärke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

// Länka en ny anpassad egenskap till ett bokmärke. Värdet på denna egenskap
// kommer att vara innehållet i bokmärket som den refererar till i "LinkSource"-medlemmen.
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> customProperties = doc->get_CustomDocumentProperties();
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> customProperty = customProperties->AddLinkToContent(u"Bookmark", u"MyBookmark");

ASPOSE_ASSERT_EQ(true, customProperty->get_IsLinkToContent());
ASSERT_EQ(u"MyBookmark", customProperty->get_LinkSource());
ASPOSE_ASSERT_EQ(u"Hello world!", customProperty->get_Value());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

## Se även

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
