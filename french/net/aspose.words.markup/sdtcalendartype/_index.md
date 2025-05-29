---
title: SdtCalendarType Enum
linktitle: SdtCalendarType
articleTitle: SdtCalendarType
second_title: Aspose.Words pour .NET
description: Explorez l'énumération Aspose.Words.Markup.SdtCalendarType pour améliorer vos documents Office Open XML avec des options de calendrier polyvalentes pour une meilleure efficacité du flux de travail.
type: docs
weight: 4690
url: /fr/net/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enumeration

Spécifie les types possibles de calendriers qui peuvent être utilisés pour spécifier[`CalendarType`](../structureddocumenttag/calendartype/) dans un document Office Open XML.

```csharp
public enum SdtCalendarType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Default | `0` | Utilisé comme valeur par défaut dans OOXML. Égal àGregorian . |
| Gregorian | `0` | Spécifie que le calendrier grégorien, tel que défini dans la norme ISO 8601, doit être utilisé. Ce calendrier doit être localisé dans la langue appropriée. |
| GregorianArabic | `1` | Spécifie que le calendrier grégorien, tel que défini dans la norme ISO 8601, doit être utilisé. Les valeurs de ce calendrier doivent être présentées en arabe. |
| GregorianMeFrench | `2` | Spécifie que le calendrier grégorien, tel que défini dans la norme ISO 8601, doit être utilisé. Les valeurs de ce calendrier doivent être présentées en français du Moyen-Orient. |
| GregorianUs | `3` | Spécifie que le calendrier grégorien, tel que défini dans la norme ISO 8601, doit être utilisé. Les valeurs de ce calendrier doivent être présentées en anglais. |
| GregorianXlitEnglish | `4` | Spécifie que le calendrier grégorien, tel que défini dans la norme ISO 8601, doit être utilisé. Les valeurs de ce calendrier doivent être la représentation des chaînes anglaises dans les caractères arabes correspondants (la translittération arabe de l'anglais pour le calendrier grégorien). |
| GregorianXlitFrench | `5` | Spécifie que le calendrier grégorien, tel que défini dans la norme ISO 8601, doit être utilisé. Les valeurs de ce calendrier doivent être la représentation des chaînes françaises dans les caractères arabes correspondants (la translittération arabe du français pour le calendrier grégorien). |
| Hebrew | `6` | Spécifie que le calendrier lunaire hébreu, tel que décrit par la formule de Gauss pour Pessah [CITATION] et la reformulation complète de la loi orale (Mishneh Torah), doit être utilisé. |
| Hijri | `7` | Spécifie que le calendrier lunaire hégirien, tel que décrit par le Royaume d'Arabie saoudite, Ministère des Affaires islamiques, des Dotations, de la Da'wah et de l'Orientation, doit être utilisé. |
| Japan | `8` | Spécifie que le calendrier de l'ère impériale japonaise, tel que décrit par la norme industrielle japonaise JIS X 0301, doit être utilisé. |
| Korea | `9` | Spécifie que le calendrier coréen de l'ère Tangun, tel que décrit par la loi coréenne n° 4, doit être utilisé. |
| None | `10` | Spécifie qu'aucun calendrier ne doit être utilisé. |
| Saka | `11` | Spécifie que le calendrier de l'ère Saka, tel que décrit par le Comité de réforme du calendrier de l'Inde, dans le cadre des éphémérides indiennes et de l'almanach nautique, doit être utilisé. |
| Taiwan | `12` | Spécifie que le calendrier taïwanais, tel que défini par la norme nationale chinoise CNS 7648, doit être utilisé. |
| Thai | `13` | Spécifie que le calendrier thaïlandais, tel que défini par le décret royal de SM le roi Vajiravudh (Rama VI) dans la Gazette royale BE 2456 (1913 après J.-C.) et par le décret du Premier ministre Phibunsongkhram (1941 après J.-C.) pour commencer l'année le 1er janvier grégorien et pour faire correspondre l'année zéro à l'année grégorienne 543 avant J.-C., doit être utilisé. |

## Exemples

Montre comment inviter l'utilisateur à saisir une date avec une balise de document structurée.

```csharp
Document doc = new Document();

// Insérez une balise de document structurée qui invite l'utilisateur à saisir une date.
// Dans Microsoft Word, cet élément est connu sous le nom de « contrôle de contenu de sélecteur de date ».
// Lorsque nous cliquons sur la flèche à l'extrémité droite de cette balise dans Microsoft Word,
// nous verrons une fenêtre contextuelle sous la forme d'un calendrier cliquable.
// Nous pouvons utiliser cette fenêtre contextuelle pour sélectionner une date à laquelle la balise affichera.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Affiche la date, selon les paramètres régionaux de l'Arabie saoudite.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Définissez le format avec lequel afficher la date.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Affiche la date selon le calendrier hégirien.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Avant que l'utilisateur ne choisisse une date dans Microsoft Word, la balise affichera le texte « Cliquez ici pour saisir une date ».
// Selon le calendrier de la balise, définissez la propriété « FullDate » pour que la balise affiche une date par défaut.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Voir également

* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
