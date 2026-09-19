---
title: "Aspose::Words::Properties::DocumentProperty::get_LinkSource metodo"
linktitle: "get_LinkSource"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::DocumentProperty::get_LinkSource metodo. Ottiene la sorgente di una proprietà documento personalizzata collegata in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.properties/documentproperty/get_linksource/
---
## DocumentProperty::get_LinkSource method


Ottiene l'origine di una proprietà del documento personalizzata collegata.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::get_LinkSource() const
```


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

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
