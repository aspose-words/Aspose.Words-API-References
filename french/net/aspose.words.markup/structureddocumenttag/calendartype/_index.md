---
title: StructuredDocumentTag.CalendarType
linktitle: CalendarType
articleTitle: CalendarType
second_title: Aspose.Words pour .NET
description: StructuredDocumentTag CalendarType propriété. Spécifie le type de calendrier pour celaTSD . La valeur par défaut estDefault en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.markup/structureddocumenttag/calendartype/
---
## StructuredDocumentTag.CalendarType property

Spécifie le type de calendrier pour cela**TSD** . La valeur par défaut estDefault

```csharp
public SdtCalendarType CalendarType { get; set; }
```

## Remarques

L'accès à cette propriété ne fonctionnera que pourDate Type SDT.

Pour tous les autres types de SDT, une exception se produira.

## Exemples

Montre comment inviter l'utilisateur à saisir une date avec une balise de document structuré.

```csharp
Document doc = new Document();

// Insère une balise de document structuré qui invite l'utilisateur à saisir une date.
// Dans Microsoft Word, cet élément est appelé « Contrôle de contenu du sélecteur de date ».
// Quand on clique sur la flèche à l'extrémité droite de cette balise dans Microsoft Word,
// nous verrons une pop up sous la forme d'un calendrier cliquable.
// Nous pouvons utiliser cette fenêtre contextuelle pour sélectionner une date à laquelle la balise affichera.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Affiche la date, selon les paramètres régionaux de l'arabe saoudien.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Définit le format avec lequel afficher la date.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Afficher la date selon le calendrier Hijri.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Avant que l'utilisateur ne choisisse une date dans Microsoft Word, la balise affichera le texte "Cliquez ici pour saisir une date.".
// Selon le calendrier du tag, définissez la propriété "FullDate" pour que le tag affiche une date par défaut.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Voir également

* enum [SdtCalendarType](../../sdtcalendartype/)
* class [StructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
