---
title: FieldListNum.ListName
linktitle: ListName
articleTitle: ListName
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldListNum ListName pour gérer facilement les définitions de numérotation abstraite pour une meilleure organisation et clarté des documents.
type: docs
weight: 40
url: /fr/net/aspose.words.fields/fieldlistnum/listname/
---
## FieldListNum.ListName property

Obtient ou définit le nom de la définition de numérotation abstraite utilisée pour la numérotation.

```csharp
public string ListName { get; set; }
```

## Exemples

Montre comment numéroter des paragraphes avec des champs LISTNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les champs LISTNUM affichent un nombre qui s'incrémente à chaque champ LISTNUM.
// Ces champs disposent également d'une variété d'options qui nous permettent de les utiliser pour émuler des listes numérotées.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Les listes commencent à compter à 1 par défaut, mais nous pouvons définir ce nombre sur une valeur différente, telle que 0.
// Ce champ affichera « 0) ».
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

// Les champs LISTNUM conservent des comptes séparés pour chaque niveau de liste.
// Insertion d'un champ LISTNUM dans le même paragraphe qu'un autre champ LISTNUM
// augmente le niveau de la liste au lieu du nombre.
// Le champ suivant continuera le décompte que nous avons commencé ci-dessus et affichera une valeur de « 1 » au niveau de la liste 1.
builder.InsertField(FieldType.FieldListNum, true);

// Ce champ démarrera un comptage au niveau de la liste 2. Il affichera une valeur de « 1 ».
builder.InsertField(FieldType.FieldListNum, true);

// Ce champ démarrera un comptage au niveau de la liste 3. Il affichera une valeur de « 1 ».
// Les différents niveaux de liste ont un formatage différent,
// donc ces champs combinés afficheront une valeur de "1)a)i)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Le prochain champ LISTNUM que nous insérons continuera le comptage au niveau de la liste
// que le champ LISTNUM précédent était activé.
// Nous pouvons utiliser la propriété « ListLevel » pour accéder à un niveau de liste différent.
// Si ce champ LISTNUM restait au niveau de liste 3, il afficherait « ii) »,
// mais, puisque nous l'avons déplacé au niveau de liste 2, il continue le comptage à ce niveau et affiche « b) ».
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Nous pouvons définir la propriété ListName pour que le champ émule un type de champ AUTONUM différent.
// "NumberDefault" émule AUTONUM, "OutlineDefault" émule AUTONUMOUT,
// et "LegalDefault" émule les champs AUTONUMLGL.
// Le nom de la liste « OutlineDefault » avec 1 comme numéro de départ entraînera l'affichage de « I. ».
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// Le ListName n'est pas repris du champ précédent, nous devrons donc le définir pour chaque nouveau champ.
// Ce champ continue le décompte avec le nom de liste différent et affiche « II. ».
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### Voir également

* class [FieldListNum](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
