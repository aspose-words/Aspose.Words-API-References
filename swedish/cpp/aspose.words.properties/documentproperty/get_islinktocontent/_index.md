---
title: "Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent metod"
linktitle: "get_IsLinkToContent"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent metod. Visar om den här egenskapen är länkad till innehåll eller inte i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.properties/documentproperty/get_islinktocontent/
---
## DocumentProperty::get_IsLinkToContent method


Visar om den här egenskapen är länkad till innehåll eller inte.

```cpp
bool Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent()
```


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

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
