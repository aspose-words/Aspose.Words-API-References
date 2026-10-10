---
title: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts méthode"
linktitle: "get_EmbedTrueTypeFonts"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts méthode. Spécifie s'il faut ou non incorporer les polices TrueType dans un document lors de son enregistrement. La valeur par défaut de cette propriété est false en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/
---
## FontInfoCollection::get_EmbedTrueTypeFonts method


Spécifie s’il faut ou non incorporer les polices TrueType dans un document lors de son enregistrement. La valeur par défaut de cette propriété est **false**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts() const
```

## Remarques


L'incorporation des polices TrueType permet aux autres de visualiser le document avec les mêmes polices utilisées pour le créer, mais peut augmenter considérablement la taille du document.

Cette option fonctionne uniquement pour les formats DOC, DOCX et RTF.

## Exemples



Montre comment enregistrer un document avec des polices TrueType incorporées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## Voir aussi

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
