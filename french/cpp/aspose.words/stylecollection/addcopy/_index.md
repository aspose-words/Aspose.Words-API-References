---
title: "Aspose::Words::StyleCollection::AddCopy méthode"
linktitle: "AddCopy"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::StyleCollection::AddCopy méthode. Copie un style dans cette collection en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/stylecollection/addcopy/
---
## StyleCollection::AddCopy method


Copie un style dans cette collection.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::AddCopy(const System::SharedPtr<Aspose::Words::Style> &style)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| style | const System::SharedPtr\<Aspose::Words::Style\>\& | [Style](../../style/) à copier. |

### ReturnValue

Style copié prêt à l'emploi.
## Remarques


[Style](../../style/) to be copied can belong to the same document as well as to different document.

Le style lié est copié.

Cette méthode ne copie pas les styles de base.

Si la collection contient déjà un style portant le même nom, alors un nouveau nom est généré automatiquement en ajoutant le suffixe "_number" à partir de 0, par ex. "Normal_0", "Heading 1_1", etc. Utilisez le mutateur [Name](../../style/get_name/) pour modifier le nom du style importé.

## Exemples



Montre comment cloner le style d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// La méthode AddCopy crée une copie du style spécifié et
// génère automatiquement un nouveau nom pour le style, tel que "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// Utilisez la propriété "Name" du style pour modifier le nom d'identification du style.
newStyle->set_Name(u"My Heading 1");

// Notre document possède maintenant deux styles identiques en apparence avec des noms différents.
// Modifier les paramètres de l'un des styles n'affecte pas l'autre.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```


Montre comment importer un style d'un document à un autre document.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

// Créez un style personnalisé pour le document source.
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
srcStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Importez le style personnalisé du document source dans le document de destination.
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> newStyle = dstDoc->get_Styles()->AddCopy(srcStyle);

// Le style importé a une apparence identique à son style source.
ASSERT_EQ(u"MyStyle", newStyle->get_Name());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), newStyle->get_Font()->get_Color().ToArgb());
```

## Voir aussi

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
