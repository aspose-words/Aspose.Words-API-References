---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase méthode"
linktitle: "get_HyperlinkBase"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase méthode. Spécifie la chaîne de base utilisée pour évaluer les hyperliens relatifs dans ce document en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkbase/
---
## BuiltInDocumentProperties::get_HyperlinkBase method


Spécifie la chaîne de base utilisée pour évaluer les hyperliens relatifs dans ce document.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase()
```

## Remarques


Aspose.Words n'utilise pas cette propriété.

## Exemples



Montre comment stocker la partie de base d'un hyperlien dans les propriétés du document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez un hyperlien relatif vers un document du système de fichiers local nommé "Document.docx".
// Cliquer sur le lien dans Microsoft Word ouvrira le document désigné, s'il est disponible.
builder->InsertHyperlink(u"Relative hyperlink", u"Document.docx", false);

// Ce lien est relatif. S'il n'y a pas de "Document.docx" dans le même dossier
// que le document contenant ce lien, le lien sera cassé.
ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"Document.docx"));
doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Le document que nous essayons de lier se trouve dans un répertoire différent de celui où nous prévoyons d'enregistrer le document.
// Nous pourrions corriger les liens de cette façon en mettant un nom de fichier absolu dans chacun d'eux.
// Alternativement, nous pourrions fournir un lien de base que chaque hyperlien avec un nom de fichier relatif
// préfixera à son lien lorsque nous cliquerons dessus.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();
properties->set_HyperlinkBase(get_MyDir());

ASSERT_TRUE(System::IO::File::Exists(properties->get_HyperlinkBase() + (System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(doc->get_Range()->get_Fields()->idx_get(0)))->get_Address()));

doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

## Voir aussi

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
