---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat méthode"
linktitle: "get_DateStorageFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat méthode. Obtient/Définit le format dans lequel la date d'un SDT de type date est stockée lorsque le SDT est lié à un nœud XML dans le magasin de données du document. La valeur par défaut est DateTime en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.markup/structureddocumenttag/get_datestorageformat/
---
## StructuredDocumentTag::get_DateStorageFormat method


Obtient/Définit le format dans lequel la date d'un SDT de type date est stockée lorsque le **SDT** est lié à un nœud XML dans le magasin de données du document. La valeur par défaut est [DateTime](../../sdtdatestorageformat/)

```cpp
Aspose::Words::Markup::SdtDateStorageFormat Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat()
```

## Remarques


L'accès à cette propriété ne fonctionnera que pour le type SDT [Date](../../sdttype/).

Pour tous les autres types de SDT, une exception se produira.

## Exemples



Montre comment inviter l’utilisateur à saisir une date avec une balise de document structuré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Insérez une balise de document structuré qui invite l’utilisateur à saisir une date.
// Dans Microsoft Word, cet élément est appelé « Date picker content control ».
// Lorsque nous cliquons sur la flèche à l’extrémité droite de cette balise dans Microsoft Word,
// Nous verrons une fenêtre contextuelle sous la forme d'un calendrier cliquable.
// Nous pouvons utiliser cette fenêtre contextuelle pour sélectionner une date que la balise affichera.
auto sdtDate = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Date, Aspose::Words::Markup::MarkupLevel::Inline);

// Affichez la date, selon les paramètres régionaux arabes d'Arabie saoudite.
sdtDate->set_DateDisplayLocale(System::Globalization::CultureInfo::GetCultureInfo(u"ar-SA")->get_LCID());

// Définissez le format avec lequel afficher la date.
sdtDate->set_DateDisplayFormat(u"dd MMMM, yyyy");
sdtDate->set_DateStorageFormat(Aspose::Words::Markup::SdtDateStorageFormat::DateTime);

// Affichez la date selon le calendrier hijri.
sdtDate->set_CalendarType(Aspose::Words::Markup::SdtCalendarType::Hijri);

// Avant que l'utilisateur ne choisisse une date dans Microsoft Word, la balise affichera le texte "Cliquez ici pour saisir une date.".
// Selon le calendrier de la balise, définissez la propriété "FullDate" pour que la balise affiche une date par défaut.
sdtDate->set_FullDate(System::DateTime(1440, 10, 20));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(sdtDate);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Date.docx");
```

## Voir aussi

* Enum [SdtDateStorageFormat](../../sdtdatestorageformat/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
