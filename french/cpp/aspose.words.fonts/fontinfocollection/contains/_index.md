---
title: "Méthode Aspose::Words::Fonts::FontInfoCollection::Contains"
linktitle: "Contains"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fonts::FontInfoCollection::Contains. Détermine si la collection contient une police portant le nom donné en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection::Contains method


Détermine si la collection contient une police avec le nom donné.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::Contains(const System::String &name)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Nom de la police à rechercher, insensible à la casse. |

### ReturnValue

**true** if the item is found in the collection; otherwise, **false**.

## Exemples



Affiche des informations sur les polices présentes dans le document vierge.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un document vierge contient 3 polices par défaut. Chaque police dans le document
// aura un objet FontInfo correspondant qui contient des détails sur cette police.
ASSERT_EQ(3, doc->get_FontInfos()->get_Count());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Times New Roman"));
ASSERT_EQ(204, doc->get_FontInfos()->idx_get(u"Times New Roman")->get_Charset());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Symbol"));
ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Arial"));
```

## Voir aussi

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
