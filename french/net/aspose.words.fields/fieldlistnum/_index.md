---
title: FieldListNum Class
linktitle: FieldListNum
articleTitle: FieldListNum
second_title: Aspose.Words pour .NET
description: Aspose.Words.Fields.FieldListNum classe. Implémente le champ LISTNUM en C#.
type: docs
weight: 2120
url: /fr/net/aspose.words.fields/fieldlistnum/
---
## FieldListNum class

Implémente le champ LISTNUM.

Pour en savoir plus, visitez le[Travailler avec des champs](https://docs.aspose.com/words/net/working-with-fields/) article documentaire.

```csharp
public class FieldListNum : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldListNum](fieldlistnum/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/) objet qui fournit un accès typé au formatage du champ. |
| [HasListName](../../aspose.words.fields/fieldlistnum/haslistname/) { get; } | Renvoie une valeur indiquant si le nom d'une définition de numérotation abstraite est fourni par le code du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [ListLevel](../../aspose.words.fields/fieldlistnum/listlevel/) { get; set; } | Obtient ou définit le niveau dans la liste, remplaçant le comportement par défaut du champ. |
| [ListName](../../aspose.words.fields/fieldlistnum/listname/) { get; set; } | Obtient ou définit le nom de la définition de numérotation abstraite utilisée pour la numérotation. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte situé entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtient le nœud qui représente le séparateur de champ. Peut être`nul` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| [StartingNumber](../../aspose.words.fields/fieldlistnum/startingnumber/) { get; set; } | Obtient ou définit la valeur de départ de ce champ. |
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

## Exemples

Montre comment numéroter les paragraphes avec les champs LISTNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les champs LISTNUM affichent un nombre qui s'incrémente à chaque champ LISTNUM.
// Ces champs ont également une variété d'options qui nous permettent de les utiliser pour émuler des listes numérotées.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Les listes commencent à compter à 1 par défaut, mais nous pouvons définir ce nombre sur une valeur différente, telle que 0.
// Ce champ affichera "0)".
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

 // Les champs LISTNUM conservent des décomptes séparés pour chaque niveau de liste.
// Insertion d'un champ LISTNUM dans le même paragraphe qu'un autre champ LISTNUM
// augmente le niveau de la liste au lieu du nombre.
// Le champ suivant continuera le décompte que nous avons commencé ci-dessus et affichera une valeur de "1" au niveau de liste 1.
builder.InsertField(FieldType.FieldListNum, true);

// Ce champ lancera un décompte au niveau de liste 2. Il affichera une valeur de "1".
builder.InsertField(FieldType.FieldListNum, true);

// Ce champ lancera un décompte au niveau de liste 3. Il affichera une valeur de "1".
// Différents niveaux de liste ont un formatage différent,
// donc ces champs combinés afficheront une valeur de "1)a)i)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Le prochain champ LISTNUM que nous insérons continuera le décompte au niveau de la liste
// que le champ LISTNUM précédent était activé.
// Nous pouvons utiliser la propriété "ListLevel" pour passer à un autre niveau de liste.
// Si ce champ LISTNUM restait au niveau de liste 3, il afficherait "ii)",
// mais, puisque nous l'avons déplacé au niveau de liste 2, il continue le décompte à ce niveau et affiche "b)".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Nous pouvons définir la propriété ListName pour que le champ émule un type de champ AUTONUM différent.
// "NumberDefault" émule AUTONUM, "OutlineDefault" émule AUTONUMOUT,
// et "LegalDefault" émule les champs AUTONUMLGL.
// Le nom de la liste "OutlineDefault" avec 1 comme numéro de départ entraînera l'affichage de "I.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// Le ListName n'est pas reporté du champ précédent, nous devrons donc le définir pour chaque nouveau champ.
// Ce champ continue le décompte avec le nom de liste différent et affiche "II.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
