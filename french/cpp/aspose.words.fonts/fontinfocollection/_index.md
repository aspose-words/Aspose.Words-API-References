---
title: "Aspose::Words::Fonts::FontInfoCollection classe"
linktitle: "FontInfoCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontInfoCollection classe. Représente une collection de polices utilisées dans un document. Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class


Représente une collection de polices utilisées dans un document. Pour en savoir plus, visitez l’article de documentation [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontInfoCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Contains](./contains/)(const System::String\&) | Détermine si la collection contient une police avec le nom donné. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtient le nombre d’éléments contenus dans la collection. |
| [get_EmbedSystemFonts](./get_embedsystemfonts/)() const | Spécifie s’il faut ou non incorporer les polices système dans le document. La valeur par défaut de cette propriété est **false**. Cette option ne fonctionne que lorsque l’option [EmbedTrueTypeFonts](./get_embedtruetypefonts/) est définie sur **true**. |
| [get_EmbedTrueTypeFonts](./get_embedtruetypefonts/)() const | Spécifie s’il faut ou non incorporer les polices TrueType dans un document lors de son enregistrement. La valeur par défaut de cette propriété est **false**. |
| [get_SaveSubsetFonts](./get_savesubsetfonts/)() const | Spécifie s’il faut ou non enregistrer un sous-ensemble des polices TrueType incorporées avec le document. La valeur par défaut de cette propriété est **false**. Cette option ne fonctionne que lorsque la propriété [EmbedTrueTypeFonts](./get_embedtruetypefonts/) est définie sur **true**. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Obtient une police avec le nom spécifié. |
| [idx_get](./idx_get/)(int32_t) | Obtient une police à l’indice spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EmbedSystemFonts](./set_embedsystemfonts/)(bool) | Mutateur pour [Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts](./get_embedsystemfonts/). |
| [set_EmbedTrueTypeFonts](./set_embedtruetypefonts/)(bool) | Mutateur pour [Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts](./get_embedtruetypefonts/). |
| [set_SaveSubsetFonts](./set_savesubsetfonts/)(bool) | Mutateur pour [Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts](./get_savesubsetfonts/). |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Remarques


Les éléments sont des objets [FontInfo](../fontinfo/).

Vous ne créez pas d’instances de cette classe directement. Utilisez la propriété [FontInfos](../../aspose.words/documentbase/get_fontinfos/) pour accéder à la collection de polices définies dans le document.

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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
