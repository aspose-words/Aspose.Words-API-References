---
title: "Aspose::Words::Markup::SdtCalendarType énum"
linktitle: "SdtCalendarType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::SdtCalendarType énum. Spécifie les types possibles de calendriers qui peuvent être utilisés pour spécifier CalendarType dans un document Office Open XML en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enum


Spécifie les types possibles de calendriers qui peuvent être utilisés pour spécifier [CalendarType](../structureddocumenttag/get_calendartype/) dans un document Office Open XML.

```cpp
enum class SdtCalendarType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Default | 0 | Utilisé comme valeur par défaut dans OOXML. Égal à [Gregorian](./). |
| Gregorian | n/a | Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. Ce calendrier doit être localisé dans la langue appropriée. |
| GregorianArabic | n/a | Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. Les valeurs de ce calendrier doivent être présentées en arabe. |
| GregorianMeFrench | n/a | Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. Les valeurs de ce calendrier doivent être présentées en français du Moyen-Orient. |
| GregorianUs | n/a | Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. Les valeurs de ce calendrier doivent être présentées en anglais. |
| GregorianXlitEnglish | n/a | Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. Les valeurs de ce calendrier doivent être la représentation des chaînes anglaises en caractères arabes correspondants (la translittération arabe de l'anglais pour le calendrier grégorien). |
| GregorianXlitFrench | n/a | Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. Les valeurs de ce calendrier doivent être la représentation des chaînes françaises en caractères arabes correspondants (la translittération arabe du français pour le calendrier grégorien). |
| Hébreu | n/a | Spécifie que le calendrier lunaire hébreu, tel que décrit par la formule de Gauss pour la Pâque [CITATION] et le Restatement complet de la loi orale (Mishneh Torah), doit être utilisé. |
| Hijri | n/a | Spécifie que le calendrier lunaire hijri, tel que décrit par le Royaume d'Arabie Saoudite, le Ministère des Affaires Islamiques, les Endowments, Da‘wah et Guidance, doit être utilisé. |
| Japon | n/a | Spécifie que le calendrier de l'ère impériale japonaise, tel que décrit par la norme industrielle japonaise JIS X 0301, doit être utilisé. |
| Corée | n/a | Spécifie que le calendrier de l'ère coréenne Tangun, tel que décrit par la loi coréenne n° 4, doit être utilisé. |
| None | n/a | Spécifie qu'aucun calendrier ne doit être utilisé. |
| Saka | n/a | Spécifie que le calendrier de l'ère Saka, tel que décrit par le Comité de réforme du calendrier de l'Inde, dans le cadre de l'éphéméride indienne et de l'almanach nautique, doit être utilisé. |
| Taïwan | n/a | Spécifie que le calendrier taïwanais, tel que défini par la norme nationale chinoise CNS 7648, doit être utilisé. |
| Thaï | n/a | Spécifie que le calendrier thaïlandais, tel que défini par le décret royal de Sa Majesté le Roi Vajiravudh (Rama VI) publié dans le Journal royal B. E. 2456 (1913 apr. J.-C.) et par le décret du Premier ministre Phibunsongkhram (1941 apr. J.-C.), doit commencer l'année le 1er janvier du calendrier grégorien et associer l'année zéro à l'année grégorienne 543 av. J.-C., doit être utilisé. |


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
