---
title: FieldAutoNum.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldAutoNum SeparatorCharacter, personnalisez facilement votre caractère séparateur pour un formatage des données amélioré et une convivialité améliorée.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

Obtient ou définit le caractère séparateur à utiliser.

```csharp
public string SeparatorCharacter { get; set; }
```

## Exemples

Montre comment numéroter des paragraphes à l'aide de champs autonum.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Chaque champ AUTONUM affiche la valeur actuelle d'un nombre courant de champs AUTONUM,
// nous permettant de numéroter automatiquement les éléments comme une liste numérotée.
// Ce champ affichera un numéro « 1 ».
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// Le caractère séparateur, qui apparaît dans le champ de résultat immédiatement après le nombre, est un point par défaut.
// Si nous laissons cette propriété nulle, notre deuxième champ AUTONUM affichera « 2. » dans le document.
Assert.IsNull(field.SeparatorCharacter);

// Nous pouvons définir cette propriété pour appliquer le premier caractère de sa chaîne comme nouveau caractère séparateur.
// Dans ce cas, notre champ AUTONUM affichera désormais « 2 : ».
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### Voir également

* class [FieldAutoNum](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
