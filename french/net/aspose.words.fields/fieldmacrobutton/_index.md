---
title: FieldMacroButton Class
linktitle: FieldMacroButton
articleTitle: FieldMacroButton
second_title: Aspose.Words pour .NET
description: Aspose.Words.Fields.FieldMacroButton classe. Implémente le champ MACROBUTTON en C#.
type: docs
weight: 2130
url: /fr/net/aspose.words.fields/fieldmacrobutton/
---
## FieldMacroButton class

Implémente le champ MACROBUTTON.

Pour en savoir plus, visitez le[Travailler avec des champs](https://docs.aspose.com/words/net/working-with-fields/) article documentaire.

```csharp
public class FieldMacroButton : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldMacroButton](fieldmacrobutton/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [DisplayText](../../aspose.words.fields/fieldmacrobutton/displaytext/) { get; set; } | Obtient ou définit le texte devant apparaître comme le « bouton » sélectionné pour exécuter la macro ou la commande. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/) objet qui fournit un accès typé au formatage du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [MacroName](../../aspose.words.fields/fieldmacrobutton/macroname/) { get; set; } | Obtient ou définit le nom de la macro ou de la commande à exécuter. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte situé entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtient le nœud qui représente le séparateur de champ. Peut être`nul` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code de champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier child de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie`nul` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/)() | Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Effectue une mise à jour du champ. Lance si le champ est déjà mis à jour. |

## Remarques

Permet d'exécuter une macro ou une commande.

Dans Aspose.Words, ce champ peut également servir de champ de fusion.

## Exemples

Montre comment utiliser les champs MACROBUTTON pour nous permettre d'exécuter les macros d'un document en cliquant.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// Insère un champ MACROBUTTON et référence l'une des macros du document par son nom dans la propriété MacroName.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// Utilisez la propriété pour référencer "ViewZoom200", une macro fournie avec Microsoft Word.
// On peut retrouver toutes les autres macros via View -> Macros (liste déroulante) -> Afficher les macros.
// Dans ce menu, sélectionnez "Commandes Word" dans la liste déroulante "Macros dans :".
// Si notre document contient une macro personnalisée portant le même nom qu'une macro stock,
// notre macro sera celle exécutée par le champ MACROBUTTON.
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.GetFieldCode());

// Enregistrez le document en tant que type de document prenant en charge les macros.
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
