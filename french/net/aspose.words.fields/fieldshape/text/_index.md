---
title: FieldShape.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words pour .NET
description: FieldShape Text propriété. Obtient ou définit le texte à récupérer en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldshape/text/
---
## FieldShape.Text property

Obtient ou définit le texte à récupérer.

```csharp
public string Text { get; set; }
```

## Exemples

Montre comment créer des listes compatibles avec les langues de droite à gauche avec les champs BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le champ BIDIOUTLINE numérote les paragraphes comme les champs AUTONUM/LISTNUM,
// mais n'est visible que lorsqu'une langue d'édition de droite à gauche est activée, comme l'hébreu ou l'arabe.
// Le champ suivant affichera ".1", l'équivalent RTL du numéro de liste "1.".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Ajoutez deux champs BIDIOUTLINE supplémentaires, qui afficheront ".2" et ".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Définissez l'alignement horizontal du texte pour chaque paragraphe du document sur RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Si nous activons une langue d'édition de droite à gauche dans Microsoft Word, nos champs afficheront des chiffres.
// Sinon, ils afficheront "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

Montre comment certains anciens champs Microsoft Word tels que SHAPE et EMBED sont gérés lors du chargement.

```csharp
// Ouvrez un document créé dans Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Si nous ouvrons le document Word et appuyons sur Alt+F9, nous verrons un champ SHAPE et un champ EMBED.
// Un champ SHAPE est l'ancre/le canevas d'un objet AutoShape avec le style d'habillage "En ligne avec le texte" activé.
// Un champ EMBED a la même fonction, mais pour un objet incorporé,
// comme une feuille de calcul provenant d'un document Excel externe.
// Cependant, ces champs n'apparaîtront pas dans la collection Fields du document.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Ces champs sont pris en charge uniquement par les anciennes versions de Microsoft Word.
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

// La troisième forme est le champ EMBED qui contenait la feuille de calcul externe.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Voir également

* class [FieldShape](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
