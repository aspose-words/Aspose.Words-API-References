---
title: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent metodo"
linktitle: "AddLinkToContent"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent metodo. Crea una nuova proprietà documento personalizzata collegata al contenuto in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties::AddLinkToContent method


Crea una nuova proprietà personalizzata del documento collegata al contenuto.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent(const System::String &name, const System::String &linkSource)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | const System::String\& | Il nome della proprietà. |
| linkSource | const System::String\& | La sorgente della proprietà. |

### ReturnValue

L'oggetto proprietà appena creato o **null** quando il *linkSource* non è valido.

## Esempi



Mostra come collegare una proprietà documento personalizzata a un segnalibro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

// Collega una nuova proprietà personalizzata a un segnalibro. Il valore di questa proprietà
// sarà il contenuto del segnalibro a cui fa riferimento nel membro "LinkSource".
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> customProperties = doc->get_CustomDocumentProperties();
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> customProperty = customProperties->AddLinkToContent(u"Bookmark", u"MyBookmark");

ASPOSE_ASSERT_EQ(true, customProperty->get_IsLinkToContent());
ASSERT_EQ(u"MyBookmark", customProperty->get_LinkSource());
ASPOSE_ASSERT_EQ(u"Hello world!", customProperty->get_Value());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

## Vedi anche

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
