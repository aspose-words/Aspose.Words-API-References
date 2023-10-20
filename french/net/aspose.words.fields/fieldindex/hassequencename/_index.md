---
title: FieldIndex.HasSequenceName
linktitle: HasSequenceName
articleTitle: HasSequenceName
second_title: Aspose.Words pour .NET
description: FieldIndex HasSequenceName propriété. Obtient une valeur indiquant si une séquence doit être utilisée lors de la création du résultat du champ en C#.
type: docs
weight: 60
url: /fr/net/aspose.words.fields/fieldindex/hassequencename/
---
## FieldIndex.HasSequenceName property

Obtient une valeur indiquant si une séquence doit être utilisée lors de la création du résultat du champ.

```csharp
public bool HasSequenceName { get; }
```

## Exemples

Montre comment diviser un document en parties en combinant les champs INDEX et SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Text du champ XE sur le côté gauche,
// et le numéro de la page qui contient le champ XE à droite.
// Si les champs XE ont la même valeur dans leur propriété "Texte",
// le champ INDEX les regroupera en une seule entrée.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Dans la propriété SequenceName, nommez une séquence de champ SEQ. Chaque entrée de ce champ INDEX affichera désormais également
// le numéro sur lequel se trouve le décompte de séquence à l'emplacement du champ XE qui a créé cette entrée.
index.SequenceName = "MySequence";

// Définit le texte qui entoure les numéros de séquence et de page pour expliquer leur signification à l'utilisateur.
// Une entrée créée avec cette configuration affichera quelque chose comme "MySequence at 1 on page 1" à son numéro de page.
// PageNumberSeparator et SequenceSeparator ne peuvent pas comporter plus de 15 caractères.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

// Les champs SEQ affichent un nombre qui s'incrémente à chaque champ SEQ.
// Ces champs conservent également des comptes séparés pour chaque séquence nommée unique
// identifié par la propriété "SequenceIdentifier" du champ SEQ.
// Insère un champ SEQ qui déplace la séquence "MySequence" à 1.
// Ce champ n'est pas différent du texte normal du document. Il n'apparaîtra pas dans la table des matières d'un champ INDEX.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// Insère un champ XE qui créera une entrée dans le champ INDEX.
// Puisque "MySequence" est à 1 et que ce champ XE est en page 2, avec les séparateurs personnalisés que nous avons définis ci-dessus,
// l'entrée INDEX de ce champ affichera "Cat" sur le côté gauche et "MySequence at 1 on page 2" sur la droite.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// Insère un saut de page et utilise les champs SEQ pour avancer "MySequence" à 3.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// Insère un champ XE avec la même propriété Text que celle ci-dessus.
// L'entrée INDEX regroupera les champs XE avec les valeurs correspondantes dans la propriété "Texte"
// en une seule entrée au lieu de créer une entrée pour chaque champ XE.
// Puisque nous sommes à la page 2 avec "MySequence" à 3, ", 3 sur la page 3" sera ajouté à la même entrée INDEX que ci-dessus.
// La partie numéro de page de cette entrée INDEX affichera désormais "MySequence à 1 sur la page 2, 3 sur la page 3".
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

// Insère un champ XE avec une nouvelle valeur de propriété Text unique.
// Cela ajoutera une nouvelle entrée, avec MySequence à 3 sur la page 4.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Dog";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Sequence.docx");
```

### Voir également

* class [FieldIndex](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
