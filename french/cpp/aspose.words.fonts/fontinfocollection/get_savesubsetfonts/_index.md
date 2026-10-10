---
title: "Méthode Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts"
linktitle: "get_SaveSubsetFonts"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts. Indique s’il faut enregistrer ou non un sous‑ensemble des polices TrueType incorporées avec le document. La valeur par défaut de cette propriété est false. Cette option ne fonctionne que lorsque la propriété EmbedTrueTypeFonts est définie sur true en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.fonts/fontinfocollection/get_savesubsetfonts/
---
## FontInfoCollection::get_SaveSubsetFonts method


Indique s’il faut enregistrer ou non un sous‑ensemble des polices TrueType incorporées avec le document. La valeur par défaut de cette propriété est **false**. Cette option ne fonctionne que lorsque la propriété [EmbedTrueTypeFonts](../get_embedtruetypefonts/) est définie sur **true**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts() const
```


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
