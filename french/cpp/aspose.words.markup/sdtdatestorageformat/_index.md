---
title: "Aspose::Words::Markup::SdtDateStorageFormat enum"
linktitle: "SdtDateStorageFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::SdtDateStorageFormat enum. Spécifie comment la date d’un SDT de type date est stockée/récupérée lorsque le SDT est lié à un nœud XML dans le magasin de données du document en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enum


Spécifie comment la date d'un SDT de type date est stockée/récupérée lorsque le SDT est lié à un nœud XML dans le magasin de données du document.

```cpp
enum class SdtDateStorageFormat
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Date | 0 | La valeur de date d’un SDT de type date est stockée comme une date au format standard XML Schema Date. |
| DateTime | 1 | La valeur de date d’un SDT de type date est stockée comme une date au format standard XML Schema DateTime. |
| Texte | 2 | La valeur de date d’un SDT de type date est stockée sous forme de texte. |
| Default | n/a | Par défaut à [DateTime](./) |


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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
