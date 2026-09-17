---
title: "Aspose::Words::Hyphenation::RegisterDictionary méthode"
linktitle: "RegisterDictionary"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Hyphenation::RegisterDictionary méthode. Enregistre et charge un dictionnaire de césure pour la langue spécifiée à partir d'un flux. Lève une exception si le dictionnaire ne peut pas être lu ou a un format invalide en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/hyphenation/registerdictionary/
---
## Hyphenation::RegisterDictionary(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Enregistre et charge un dictionnaire de césure pour la langue spécifiée à partir d'un flux. Lève une exception si le dictionnaire ne peut pas être lu ou a un format invalide.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::SharedPtr<System::IO::Stream> &stream)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| langue | const System::String\& | Un nom de langue, par ex. "en-US". Voir la documentation .NET pour "culture name" et le RFC 4646 pour plus de détails. |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Un flux pour le fichier de dictionnaire au format OpenOffice. |

## Voir aussi

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Hyphenation::RegisterDictionary(const System::String\&, const System::String\&) method


Enregistre et charge un dictionnaire de césure pour la langue spécifiée à partir d'un fichier. Lève une exception si le dictionnaire ne peut pas être lu ou a un format invalide. Cette méthode peut également être utilisée pour enregistrer un dictionnaire Null afin d'empêcher que le [Callback](../get_callback/) soit appelé de façon répétée pour la même langue.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::String &fileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| langue | const System::String\& | Un nom de langue, par ex. "en-US". Voir la documentation .NET pour "culture name" et le RFC 4646 pour plus de détails. |
| fileName | const System::String\& | Un chemin vers le fichier de dictionnaire au format Open Office. Si ce paramètre est **null** ou une chaîne vide, alors le dictionnaire enregistré est Null et le rappel n'est plus appelé pour cette langue. Pour réactiver le rappel, utilisez la méthode [UnregisterDictionary()](../). |

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
## Hyphenation::RegisterDictionary(System::String, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::Hyphenation::RegisterDictionary(System::String language, std::basic_istream<CharType, Traits> &stream)
```

## Voir aussi

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
