---
title: "Méthode Aspose::Words::Markup::CustomXmlPart::get_DataChecksum"
linktitle: "get_DataChecksum"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Markup::CustomXmlPart::get_DataChecksum. Spécifie une somme de contrôle de redondance cyclique (CRC) du contenu Data en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.markup/customxmlpart/get_datachecksum/
---
## CustomXmlPart::get_DataChecksum method


Spécifie une somme de contrôle de redondance cyclique (CRC) du contenu [Data](../get_data/).

```cpp
int64_t Aspose::Words::Markup::CustomXmlPart::get_DataChecksum()
```


## Exemples



Montre comment la somme de contrôle est calculée à l'exécution.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto richText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(richText);

// La somme de contrôle est en lecture seule et calculée à l'aide des données de la partie XML personnalisée correspondante.
richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>ContentControl</text></root>"), u"/root/text", u"");

int64_t checksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << checksum << std::endl;

richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>Updated ContentControl</text></root>"), u"/root/text", u"");

int64_t updatedChecksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << updatedChecksum << std::endl;

// Nous avons modifié le XmlPart de la balise, et la somme de contrôle a été mise à jour à l'exécution.
ASSERT_NE(checksum, updatedChecksum);
```

## Voir aussi

* Class [CustomXmlPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
