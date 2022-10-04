---
title: FieldMergeField
second_title: Référence de l'API Aspose.Words pour .NET
description: Implémente le champ MERGEFIELD.
type: docs
weight: 2000
url: /fr/net/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class

Implémente le champ MERGEFIELD.

```csharp
public class FieldMergeField : Field
```

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [FieldName](../../aspose.words.fields/fieldmergefield/fieldname/) { get; set; } | Obtient ou définit le nom d'un champ de données. |
| [FieldNameNoPrefix](../../aspose.words.fields/fieldmergefield/fieldnamenoprefix/) { get; } | Renvoie uniquement le nom du champ de données. Tout préfixe est supprimé dans la propriété de préfixe. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/) objet qui fournit un accès typé au formatage du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [IsMapped](../../aspose.words.fields/fieldmergefield/ismapped/) { get; set; } | Obtient ou définit si ce champ est un champ mappé. |
| [IsVerticalFormatting](../../aspose.words.fields/fieldmergefield/isverticalformatting/) { get; set; } | Obtient ou définit s'il faut activer la conversion de caractères pour le formatage vertical. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtient le nœud qui représente le séparateur de champs. Peut être null. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| [TextAfter](../../aspose.words.fields/fieldmergefield/textafter/) { get; set; } | Obtient ou définit le texte à insérer après le champ si le champ n'est pas vide. |
| [TextBefore](../../aspose.words.fields/fieldmergefield/textbefore/) { get; set; } | Obtient ou définit le texte à insérer avant le champ si le champ n'est pas vide. |
| override [Type](../../aspose.words.fields/fieldmergefield/type/) { get; } | Obtient le type de champ Microsoft Word. |

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

Récupère le nom d'un champ de données dans les caractères de fusion d'un document principal de fusion et publipostage. Lorsque le document principal est fusionné avec la source de données sélectionnée, les informations du champ de données spécifié sont insérées à la place du champ de fusion.

### Exemples

Montre comment utiliser les champs MERGEFIELD pour effectuer un publipostage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crée une table de données à utiliser comme source de données de publipostage.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Insère un MERGEFIELD avec une propriété FieldName définie sur le nom d'une colonne dans la source de données.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// Nous pouvons appliquer du texte avant et après la valeur que ce champ accepte lors de la fusion.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());

// Insérer un autre MERGEFIELD pour une colonne différente dans la source de données.
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
