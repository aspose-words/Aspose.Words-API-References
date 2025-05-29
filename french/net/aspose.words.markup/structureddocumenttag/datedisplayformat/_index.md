---
title: StructuredDocumentTag.DateDisplayFormat
linktitle: DateDisplayFormat
articleTitle: DateDisplayFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété StructuredDocumentTag DateDisplayFormat pour personnaliser facilement les formats d'affichage des dates. Améliorez la clarté et l'attrait de votre document !
type: docs
weight: 90
url: /fr/net/aspose.words.markup/structureddocumenttag/datedisplayformat/
---
## StructuredDocumentTag.DateDisplayFormat property

Chaîne qui représente le format dans lequel les dates sont affichées.

```csharp
public string DateDisplayFormat { get; set; }
```

## Remarques

Ça ne peut pas être`nul`.

Les dates pour l'anglais (États-Unis) sont « mm/jj/aaaa »

L'accès à cette propriété ne fonctionnera que pourDate Type SDT.

Pour tous les autres types de SDT, une exception se produira.

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

* class [StructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
