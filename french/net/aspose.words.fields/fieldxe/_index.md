---
title: FieldXE Class
linktitle: FieldXE
articleTitle: FieldXE
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.FieldXE, votre solution pour implémenter efficacement les champs XE dans le traitement de documents. Améliorez votre flux de travail dès aujourd'hui !
type: docs
weight: 3020
url: /fr/net/aspose.words.fields/fieldxe/
---
## FieldXE class

Implémente le champ XE.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public class FieldXE : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldXE](fieldxe/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [EntryType](../../aspose.words.fields/fieldxe/entrytype/) { get; set; } | Obtient ou définit un type d'entrée d'index. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/)objet qui fournit un accès typé au formatage du champ. |
| [IsBold](../../aspose.words.fields/fieldxe/isbold/) { get; set; } | Obtient ou définit s'il faut appliquer une mise en forme en gras au numéro de page de l'entrée. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [IsItalic](../../aspose.words.fields/fieldxe/isitalic/) { get; set; } | Obtient ou définit s'il faut appliquer la mise en forme italique au numéro de page de l'entrée. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [PageNumberReplacement](../../aspose.words.fields/fieldxe/pagenumberreplacement/) { get; set; } | Obtient ou définit le texte utilisé à la place d'un numéro de page. |
| [PageRangeBookmarkName](../../aspose.words.fields/fieldxe/pagerangebookmarkname/) { get; set; } | Obtient ou définit le nom du signet qui marque une plage de pages qui est insérée comme numéro de page de l'entrée. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Récupère le nœud représentant le séparateur de champ. Peut être`nul` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| [Text](../../aspose.words.fields/fieldxe/text/) { get; set; } | Obtient ou définit le texte de l'entrée. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |
| [Yomi](../../aspose.words.fields/fieldxe/yomi/) { get; set; } | Obtient ou définit le yomi (premier caractère phonétique pour le tri des index) pour l'entrée d'index |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud immédiatement après le champ. Si la fin du champ est le dernier child de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie`nul` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/)() | Effectue la mise à jour du champ. Lève une requête si le champ est déjà en cours de mise à jour. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Effectue une mise à jour du champ. L'erreur est générée si le champ est déjà en cours de mise à jour. |

## Remarques

Définit le texte et le numéro de page d'une entrée d'index, qui est utilisé par un champ INDEX.

## Exemples

Montre comment créer un champ INDEX, puis utiliser des champs XE pour le remplir avec des entrées.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Texte du champ XE sur le côté gauche
// et la page contenant le champ XE à droite.
// Si les champs XE ont la même valeur dans leur propriété « Texte »,
// le champ INDEX les regroupera en une seule entrée.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Configurez le champ INDEX uniquement pour afficher les champs XE qui se trouvent dans les limites
// d'un signet nommé "MainBookmark", et dont les propriétés "EntryType" ont une valeur de "A".
// Pour les champs INDEX et XE, la propriété « EntryType » utilise uniquement le premier caractère de sa valeur de chaîne.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// Sur une nouvelle page, démarrez le signet avec un nom qui correspond à la valeur
// de la propriété « BookmarkName » du champ INDEX.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// Le champ INDEX récupérera cette entrée car elle se trouve à l'intérieur du signet,
// et son type d'entrée correspond également au type d'entrée du champ INDEX.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Insérer un champ XE qui n'apparaîtra pas dans l'INDEX car les types d'entrée ne correspondent pas.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Terminez le signet et insérez ensuite un champ XE.
// Il est du même type que le champ INDEX, mais n'apparaîtra pas
// car il est en dehors des limites du signet.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

Montre comment remplir un champ INDEX avec des entrées à l'aide de champs XE et également modifier son apparence.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Texte du champ XE sur le côté gauche,
// et le numéro de la page qui contient le champ XE à droite.
// Si les champs XE ont la même valeur dans leur propriété « Texte »,
// le champ INDEX les regroupera en une seule entrée.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Définir la valeur de cette propriété sur « A » regroupera toutes les entrées par leur première lettre,
// et placez cette lettre en majuscule au-dessus de chaque groupe.
index.Heading = "A";

// Définissez la table créée par le champ INDEX pour qu'elle s'étende sur 2 colonnes.
index.NumberOfColumns = "2";

// Définissez toutes les entrées avec des lettres de départ en dehors de la plage de caractères « ac » à omettre.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Ces deux prochains champs XE apparaîtront sous le titre « A »,
// avec leurs styles de texte respectifs également appliqués à leurs numéros de page.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

// Les deux champs XE suivants seront sous un en-tête « B » et « C » dans la table des matières des champs INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// Les champs INDEX trient toutes les entrées par ordre alphabétique, donc cette entrée apparaîtra sous « A » avec les deux autres.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Cette entrée n'apparaîtra pas car elle commence par la lettre « D »,
// qui est en dehors de la plage de caractères « ac » définie par la propriété LetterRange du champ INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
