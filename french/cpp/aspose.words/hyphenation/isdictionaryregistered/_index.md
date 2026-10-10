---
title: "Méthode Aspose::Words::Hyphenation::IsDictionaryRegistered"
linktitle: "IsDictionaryRegistered"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Hyphenation::IsDictionaryRegistered. Retourne false s'il n'existe aucun dictionnaire enregistré pour la langue spécifiée ou si le dictionnaire enregistré est Null, true sinon en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation::IsDictionaryRegistered method


Renvoie **false** si, pour la langue spécifiée, aucun dictionnaire n'est enregistré ou si le dictionnaire enregistré est Null, **true** sinon.

```cpp
static bool Aspose::Words::Hyphenation::IsDictionaryRegistered(const System::String &language)
```


## Exemples



Montre comment enregistrer un dictionnaire de césure.
```cpp
// Un dictionnaire de césure contient une liste de chaînes qui définissent les règles de césure pour la langue du dictionnaire.
// Lorsqu'un document contient des lignes de texte dans lesquelles un mot pourrait être séparé et continué sur la ligne suivante,
// la césure parcourra la liste de chaînes du dictionnaire à la recherche des sous‑chaînes de ce mot.
// Si le dictionnaire contient une sous‑chaîne, la césure séparera le mot sur deux lignes
// à l'endroit de la sous‑chaîne et ajoutera un trait d'union à la première moitié.
// Enregistrez un fichier de dictionnaire depuis le système de fichiers local pour la locale "de-CH".
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Ouvrez un document contenant du texte dont la locale correspond à celle de notre dictionnaire,
// et enregistrez‑le dans un format à pages fixes. Le texte de ce document sera césuré.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Run> >()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Run>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Run> r)>>([](System::SharedPtr<Aspose::Words::Run> r) -> bool
{
    return r->get_Font()->get_LocaleId() == System::MakeObject<System::Globalization::CultureInfo>(u"de-CH")->get_LCID();
}))));

doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Registered.pdf");

// Rechargez le document après avoir désenregistré le dictionnaire,
// et enregistrez‑le dans un autre PDF, qui ne contiendra pas de texte césuré.
Aspose::Words::Hyphenation::UnregisterDictionary(u"de-CH");

ASSERT_FALSE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");
doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Unregistered.pdf");
```

## Voir aussi

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
