---
title: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts méthode"
linktitle: "get_EmbedSystemFonts"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts méthode. Spécifie s'il faut ou non incorporer les polices système dans le document. La valeur par défaut de cette propriété est false. Cette option ne fonctionne que lorsque l'option EmbedTrueTypeFonts est définie sur true en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.fonts/fontinfocollection/get_embedsystemfonts/
---
## FontInfoCollection::get_EmbedSystemFonts method


Spécifie s'il faut ou non incorporer les polices système dans le document. La valeur par défaut de cette propriété est **false**. Cette option ne fonctionne que lorsque l'option [EmbedTrueTypeFonts](../get_embedtruetypefonts/) est définie sur **true**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts() const
```

## Remarques


Définir cette propriété sur **true** est utile si l'utilisateur se trouve sur un système d'Asie de l'Est et souhaite créer un document lisible par d'autres qui n'ont pas les polices de cette langue sur leur système. Par exemple, un utilisateur sur un système japonais pourrait choisir d'incorporer les polices dans un document afin que le document japonais soit lisible sur tous les systèmes.

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
