---
title: "Méthode Aspose::Words::DocumentBase::get_FontInfos"
linktitle: "get_FontInfos"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBase::get_FontInfos. Fournit l'accès aux propriétés des polices utilisées dans ce document en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/documentbase/get_fontinfos/
---
## DocumentBase::get_FontInfos method


Fournit l'accès aux propriétés des polices utilisées dans ce document.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> Aspose::Words::DocumentBase::get_FontInfos() const
```

## Remarques


Cette collection de définitions de polices est chargée telle quelle depuis le document. Les définitions de [Font](../../font/) peuvent être optionnelles, manquantes ou incomplètes dans certains documents.

Ne vous fiez pas à cette collection pour déterminer qu'une police particulière est utilisée dans le document. Vous ne devez l'utiliser que pour obtenir des informations sur les polices qui pourraient être utilisées dans le document.

## Exemples



Montre comment imprimer les détails des polices présentes dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Imprime toutes les polices utilisées et non utilisées dans le document.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```


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

* Class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
