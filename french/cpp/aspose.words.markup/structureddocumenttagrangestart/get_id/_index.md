---
title: "Méthode Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Id"
linktitle: "get_Id"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Id méthode. Spécifie un identifiant numérique unique en lecture seule et persistant pour cette balise de document structuré en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.markup/structureddocumenttagrangestart/get_id/
---
## StructuredDocumentTagRangeStart::get_Id method


Spécifie un identifiant numérique persistant en lecture seule unique pour cette balise de document structuré.

```cpp
int32_t Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Id() override
```

## Remarques


L'attribut Id doit respecter ces règles :* Le document ne conserve les identifiants des balises de document structuré que si le document entier est cloné [Clone](../../../aspose.words/document/clone/).
* During [ImportNode()](../) Id shall be retained if import does not cause conflicts with other structured document tag Ids in the target document.
* If multiple structured document tag nodes specify the same decimal number value for the Id attribute, then the first structured document tag in the document shall maintain this original Id, and all subsequent structured document tag nodes shall have new identifiers assigned to them when the document is loaded.
* During standalone structured document tag [Clone()](../) operation new unique ID will be generated for the cloned structured document tag node.
* If Id is not specified in the source document, then the structured document tag node shall have a new unique identifier assigned to it when the document is loaded.



## Exemples



Montre comment obtenir les propriétés des balises de document structuré multi‑sections.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

auto rangeStartTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeEnd>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeStartTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|Title: {0}", rangeStartTag->get_Title()) << std::endl;
std::cout << System::String::Format(u"\t|PlaceholderName: {0}", rangeStartTag->get_PlaceholderName()) << std::endl;
std::cout << System::String::Format(u"\t|IsShowingPlaceholderText: {0}", rangeStartTag->get_IsShowingPlaceholderText()) << std::endl;
std::cout << System::String::Format(u"\t|LockContentControl: {0}", rangeStartTag->get_LockContentControl()) << std::endl;
std::cout << System::String::Format(u"\t|LockContents: {0}", rangeStartTag->get_LockContents()) << std::endl;
std::cout << System::String::Format(u"\t|Level: {0}", rangeStartTag->get_Level()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeStartTag->get_NodeType()) << std::endl;
std::cout << System::String::Format(u"\t|RangeEnd: {0}", rangeStartTag->get_RangeEnd()) << std::endl;
std::cout << System::String::Format(u"\t|Color: {0}", rangeStartTag->get_Color().ToArgb()) << std::endl;
std::cout << System::String::Format(u"\t|SdtType: {0}", rangeStartTag->get_SdtType()) << std::endl;
std::cout << System::String::Format(u"\t|FlatOpcContent: {0}", rangeStartTag->get_WordOpenXML()) << std::endl;
std::cout << System::String::Format(u"\t|Tag: {0}\n", rangeStartTag->get_Tag()) << std::endl;

std::cout << "StructuredDocumentTagRangeEnd values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeEndTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeEndTag->get_NodeType()) << std::endl;
```

## Voir aussi

* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
