---
title: FieldPage
second_title: Référence de l'API Aspose.Words pour .NET
description: Implémente le champ PAGE.
type: docs
weight: 2110
url: /fr/net/aspose.words.fields/fieldpage/
---
## FieldPage class

Implémente le champ PAGE.

```csharp
public class FieldPage : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldPage](fieldpage)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format) { get; } | Obtient un[`FieldFormat`](../fieldformat) objet qui fournit un accès typé au formatage du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Obtient le nœud qui représente le séparateur de champs. Peut être null. |
| [Start](../../aspose.words.fields/field/start) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code de champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie **nul** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update)() | Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour. |
| [Update](../../aspose.words.fields/field/update)(bool) | Effectue une mise à jour du champ. Lance si le champ est déjà mis à jour. |

### Remarques

Récupère le numéro de la page en cours.

### Exemples

Montre comment utiliser les champs NUMCHARS, NUMWORDS, NUMPAGES et PAGE pour suivre la taille de nos documents.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Vous trouverez ci-dessous trois types de champs que nous pouvons utiliser pour suivre la taille de nos documents.
// 1 - Suivre le nombre de caractères avec un champ NUMCHARS :
FieldNumChars fieldNumChars = (FieldNumChars)builder.InsertField(FieldType.FieldNumChars, true);       
builder.Writeln(" characters");

// 2 - Suivre le nombre de mots avec un champ NUMWORDS :
FieldNumWords fieldNumWords = (FieldNumWords)builder.InsertField(FieldType.FieldNumWords, true);
builder.Writeln(" words");

// 3 - Utilisez les champs PAGE et NUMPAGES pour afficher sur quelle page se trouve le champ,
// et le nombre total de pages du document :
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
builder.Write("Page ");
FieldPage fieldPage = (FieldPage)builder.InsertField(FieldType.FieldPage, true);
builder.Write(" of ");
FieldNumPages fieldNumPages = (FieldNumPages)builder.InsertField(FieldType.FieldNumPages, true);

Assert.AreEqual(" NUMCHARS ", fieldNumChars.GetFieldCode());
Assert.AreEqual(" NUMWORDS ", fieldNumWords.GetFieldCode());
Assert.AreEqual(" NUMPAGES ", fieldNumPages.GetFieldCode());
Assert.AreEqual(" PAGE ", fieldPage.GetFieldCode());

// Ces champs ne maintiendront pas des valeurs précises en temps réel
// pendant que nous modifions le document par programmation à l'aide de Aspose.Words ou dans Microsoft Word.
 // Nous devons les mettre à jour chaque fois que nous en avons besoin pour voir une valeur à jour.
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.NUMCHARS.NUMWORDS.NUMPAGES.PAGE.docx");
```

### Voir également

* class [Field](../field)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
