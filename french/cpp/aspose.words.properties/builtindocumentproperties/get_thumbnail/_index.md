---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail méthode"
linktitle: "get_Thumbnail"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail méthode. Obtient ou définit la vignette du document en C++."
type: docs
weight: 28000
url: /fr/cpp/aspose.words.properties/builtindocumentproperties/get_thumbnail/
---
## BuiltInDocumentProperties::get_Thumbnail method


Obtient ou définit la vignette du document.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail()
```

## Remarques


Pour l’instant, cette propriété n’est utilisée que lorsqu’un document est exporté vers ePub ; elle n’est pas lue ni écrite dans d’autres formats de document.

Une image de format arbitraire peut être affectée à cette propriété, mais le format est vérifié lors de l'exportation.

Seules les images gif, jpeg et png peuvent être utilisées pour la publication ePub.

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

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
