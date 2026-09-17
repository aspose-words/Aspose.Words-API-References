---
title: "Méthode Aspose::Words::Markup::XmlMapping::get_StoreItemId"
linktitle: "get_StoreItemId"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Markup::XmlMapping::get_StoreItemId. Spécifie l'identifiant de données XML personnalisé pour la partie de données XML personnalisée qui doit être utilisé pour évaluer l'expression XPath en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.markup/xmlmapping/get_storeitemid/
---
## XmlMapping::get_StoreItemId method


Spécifie l'identifiant de données XML personnalisé pour la partie de données XML personnalisée qui doit être utilisé pour évaluer l'expression [XPath](../get_xpath/).

```cpp
System::String Aspose::Words::Markup::XmlMapping::get_StoreItemId()
```


## Exemples



Montre comment obtenir l'identifiant de données XML personnalisé d'une partie XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom XML part in structured document tag.docx");

// Les tags de document structuré ont des ID sous forme de GUIDs.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 0, true));

ASSERT_EQ(u"{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag->get_XmlMapping()->get_StoreItemId());
```

## Voir aussi

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
