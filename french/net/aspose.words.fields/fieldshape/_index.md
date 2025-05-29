---
title: FieldShape Class
linktitle: FieldShape
articleTitle: FieldShape
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.FieldShape pour une implémentation simplifiée des champs SHAPE. Améliorez la conception de vos documents grâce à des fonctionnalités puissantes et flexibles.
type: docs
weight: 2820
url: /fr/net/aspose.words.fields/fieldshape/
---
## FieldShape class

Implémente le champ SHAPE.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public class FieldShape : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldShape](fieldshape/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/)objet qui fournit un accès typé au formatage du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Récupère le nœud représentant le séparateur de champ. Peut être`nul` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| [Text](../../aspose.words.fields/fieldshape/text/) { get; set; } | Obtient ou définit le texte à récupérer. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |

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

Récupère le texte spécifié.

## Exemples

Montre comment créer des listes compatibles avec les langues de droite à gauche avec des champs BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le champ BIDIOUTLINE numérote les paragraphes comme les champs AUTONUM/LISTNUM,
// mais n'est visible que lorsqu'une langue d'édition de droite à gauche est activée, comme l'hébreu ou l'arabe.
// Le champ suivant affichera « .1 », l'équivalent RTL du numéro de liste « 1 ».
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Ajoutez deux autres champs BIDIOUTLINE, qui afficheront « .2 » et « .3 ».
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Définissez l'alignement horizontal du texte pour chaque paragraphe du document sur RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Si nous activons une langue d'édition de droite à gauche dans Microsoft Word, nos champs afficheront des nombres.
// Sinon, ils afficheront "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

Montre comment certains anciens champs Microsoft Word tels que SHAPE et EMBED sont gérés lors du chargement.

```csharp
// Ouvrez un document créé dans Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Si nous ouvrons le document Word et appuyons sur Alt+F9, nous verrons un champ SHAPE et un champ EMBED.
// Un champ SHAPE est l'ancre/le canevas d'un objet AutoShape avec le style d'habillage « En ligne avec le texte » activé.
// Un champ EMBED a la même fonction, mais pour un objet incorporé,
// comme une feuille de calcul provenant d'un document Excel externe.
// Cependant, ces champs n'apparaîtront pas dans la collection Fields du document.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Ces champs ne sont pris en charge que par les anciennes versions de Microsoft Word.
// Le processus de chargement du document convertira ces champs en objets Shape,
// auquel nous pouvons accéder dans la collection de nœuds du document.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// Le premier nœud Shape correspond au champ SHAPE dans le document d'entrée,
// qui est le canevas en ligne pour la forme automatique.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// Le deuxième nœud Shape est la forme automatique elle-même.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// La troisième forme est ce qui était le champ EMBED qui contenait la feuille de calcul externe.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
