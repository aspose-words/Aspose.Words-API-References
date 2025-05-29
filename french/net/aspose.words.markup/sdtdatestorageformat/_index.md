---
title: SdtDateStorageFormat Enum
linktitle: SdtDateStorageFormat
articleTitle: SdtDateStorageFormat
second_title: Aspose.Words pour .NET
description: Découvrez comment Aspose.Words.Markup.SdtDateStorageFormat améliore la gestion des dates dans les SDT, garantissant une intégration transparente des données XML dans vos documents.
type: docs
weight: 4700
url: /fr/net/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enumeration

Spécifie comment la date d'un SDT de date est stockée/récupérée lorsque le SDT est lié à un nœud XML dans le magasin de données du document.

```csharp
public enum SdtDateStorageFormat
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Date | `0` | La valeur de date pour un SDT de date est stockée sous forme de date au format de date de schéma XML standard. |
| DateTime | `1` | La valeur de date pour un SDT de date est stockée sous forme de date au format XML Schema DateTime standard. |
| Text | `2` | La valeur de date pour un SDT de date est stockée sous forme de texte. |
| Default | `1` | Par défautDateTime |

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
