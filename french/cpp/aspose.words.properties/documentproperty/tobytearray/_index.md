---
title: "Aspose::Words::Properties::DocumentProperty::ToByteArray méthode"
linktitle: "ToByteArray"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::DocumentProperty::ToByteArray méthode. Retourne la valeur de la propriété sous forme de tableau d’octets en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty::ToByteArray method


Renvoie la valeur de la propriété sous forme de tableau d'octets.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::DocumentProperty::ToByteArray()
```

## Remarques


Lance une exception si le type de la propriété n’est pas [ByteArray](../../propertytype/).

## Exemples



Montre comment ajouter une vignette à un document que nous enregistrons au format Epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Si nous enregistrons un document, dont la propriété "Thumbnail" contient les données d'image que nous avons ajoutées, au format Epub,
// un lecteur qui ouvre ce document peut afficher l'image avant la première page.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

System::ArrayPtr<uint8_t> thumbnailBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");
properties->set_Thumbnail(thumbnailBytes);

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.epub");

// Nous pouvons extraire l'image de vignette d'un document et l'enregistrer sur le système de fichiers local.
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> thumbnail = doc->get_BuiltInDocumentProperties()->idx_get(u"Thumbnail");
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.gif", thumbnail->ToByteArray());
```

## Voir aussi

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
