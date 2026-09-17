---
title: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent méthode"
linktitle: "AddLinkToContent"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent méthode. Crée une nouvelle propriété de document personnalisée liée au contenu en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties::AddLinkToContent method


Crée une nouvelle propriété de document personnalisée liée au contenu.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent(const System::String &name, const System::String &linkSource)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom de la propriété. |
| linkSource | const System::String\& | La source de la propriété. |

### ReturnValue

L'objet de propriété nouvellement créé ou **null** lorsque le *linkSource* est invalide.

## Exemples



Montre comment lier une propriété de document personnalisée à un signet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

// Liez une nouvelle propriété personnalisée à un signet. La valeur de cette propriété
// sera le contenu du signet auquel elle fait référence dans le membre "LinkSource".
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> customProperties = doc->get_CustomDocumentProperties();
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> customProperty = customProperties->AddLinkToContent(u"Bookmark", u"MyBookmark");

ASPOSE_ASSERT_EQ(true, customProperty->get_IsLinkToContent());
ASSERT_EQ(u"MyBookmark", customProperty->get_LinkSource());
ASPOSE_ASSERT_EQ(u"Hello world!", customProperty->get_Value());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

## Voir aussi

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
