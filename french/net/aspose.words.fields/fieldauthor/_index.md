---
title: Class FieldAuthor
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fields.FieldAuthor classe. Implémente le champ AUTHOR.
type: docs
weight: 1420
url: /fr/net/aspose.words.fields/fieldauthor/
---
## FieldAuthor class

Implémente le champ AUTHOR.

```csharp
public class FieldAuthor : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldAuthor](fieldauthor/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [AuthorName](../../aspose.words.fields/fieldauthor/authorname/) { get; set; } | Obtient ou définit le nom de l'auteur du document. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/) objet qui fournit un accès typé au formatage du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtient le nœud qui représente le séparateur de champs. Peut être null. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code de champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie **nul** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/)() | Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Effectue une mise à jour du champ. Lance si le champ est déjà mis à jour. |

### Remarques

Récupère et éventuellement définit le nom de l'auteur du document, tel qu'il est enregistré dans le **Auteur**propriété des propriétés de document intégrées .

### Exemples

Montre comment utiliser un champ AUTEUR pour afficher le nom du créateur d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les champs AUTHOR tirent leurs résultats de la propriété de document intégrée appelée "Auteur".
// Si nous créons et enregistrons un document dans Microsoft Word,
// il aura notre nom d'utilisateur dans cette propriété.
// Cependant, si nous créons un document par programme en utilisant Aspose.Words,
 // la propriété "Auteur", par défaut, sera une chaîne vide.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// Définir un nom d'auteur de sauvegarde pour les champs AUTEUR à utiliser
// si la propriété "Auteur" contient une chaîne vide.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Mise à jour d'un champ AUTEUR contenant une valeur
// appliquera cette valeur à la propriété intégrée "Auteur".
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// Changer cette propriété, puis mettre à jour le champ AUTEUR appliquera cette valeur au champ.
doc.BuiltInDocumentProperties.Author = "John Doe";      
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// Si on met à jour un champ AUTHOR après avoir changé sa propriété "Name",
// alors le champ affichera le nouveau nom et appliquera le nouveau nom à la propriété intégrée.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// Les champs AUTHOR n'affectent pas la propriété DefaultDocumentAuthor.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)


