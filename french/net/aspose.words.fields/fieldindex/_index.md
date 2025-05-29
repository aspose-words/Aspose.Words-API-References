---
title: FieldIndex Class
linktitle: FieldIndex
articleTitle: FieldIndex
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.FieldIndex pour implémenter facilement des champs INDEX dans vos documents. Améliorez votre gestion documentaire dès aujourd'hui !
type: docs
weight: 2470
url: /fr/net/aspose.words.fields/fieldindex/
---
## FieldIndex class

Implémente le champ INDEX.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public class FieldIndex : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldIndex](fieldindex/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldindex/bookmarkname/) { get; set; } | Obtient ou définit le nom du signet qui marque la partie du document utilisée pour créer l'index. |
| [CrossReferenceSeparator](../../aspose.words.fields/fieldindex/crossreferenceseparator/) { get; set; } | Obtient ou définit la séquence de caractères utilisée pour séparer les références croisées et les autres entrées. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [EntryType](../../aspose.words.fields/fieldindex/entrytype/) { get; set; } | Obtient ou définit un type d'entrée d'index utilisé pour créer l'index. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/)objet qui fournit un accès typé au formatage du champ. |
| [HasPageNumberSeparator](../../aspose.words.fields/fieldindex/haspagenumberseparator/) { get; } | Obtient une valeur indiquant si un séparateur de numéro de page est remplacé par le code du champ. |
| [HasSequenceName](../../aspose.words.fields/fieldindex/hassequencename/) { get; } | Obtient une valeur indiquant si une séquence doit être utilisée lors de la création du résultat du champ. |
| [Heading](../../aspose.words.fields/fieldindex/heading/) { get; set; } | Obtient ou définit un en-tête qui apparaît au début de chaque ensemble d'entrées pour une lettre donnée. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LanguageId](../../aspose.words.fields/fieldindex/languageid/) { get; set; } | Obtient ou définit l'ID de langue utilisé pour générer l'index. |
| [LetterRange](../../aspose.words.fields/fieldindex/letterrange/) { get; set; } | Obtient ou définit une plage de lettres à laquelle limite l'index. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [NumberOfColumns](../../aspose.words.fields/fieldindex/numberofcolumns/) { get; set; } | Obtient ou définit le nombre de colonnes par page utilisées lors de la création de l'index. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldindex/pagenumberlistseparator/) { get; set; } | Obtient ou définit la séquence de caractères utilisée pour séparer deux numéros de page dans une liste de numéros de page. |
| [PageNumberSeparator](../../aspose.words.fields/fieldindex/pagenumberseparator/) { get; set; } | Obtient ou définit la séquence de caractères utilisée pour séparer une entrée d'index et son numéro de page. |
| [PageRangeSeparator](../../aspose.words.fields/fieldindex/pagerangeseparator/) { get; set; } | Obtient ou définit la séquence de caractères utilisée pour séparer le début et la fin d'une plage de pages. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [RunSubentriesOnSameLine](../../aspose.words.fields/fieldindex/runsubentriesonsameline/) { get; set; } | Obtient ou définit si les sous-entrées doivent être exécutées sur la même ligne que l'entrée principale. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Récupère le nœud représentant le séparateur de champ. Peut être`nul` . |
| [SequenceName](../../aspose.words.fields/fieldindex/sequencename/) { get; set; } | Obtient ou définit le nom d'une séquence dont le numéro est inclus avec le numéro de page. |
| [SequenceSeparator](../../aspose.words.fields/fieldindex/sequenceseparator/) { get; set; } | Obtient ou définit la séquence de caractères utilisée pour séparer les numéros de séquence et les numéros de page. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |
| [UseYomi](../../aspose.words.fields/fieldindex/useyomi/) { get; set; } | Obtient ou définit s'il faut activer l'utilisation du texte Yomi pour les entrées d'index. |

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

Crée un index en utilisant les entrées d'index spécifiées par les champs XE et insère cet index à cet endroit dans le document.

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
