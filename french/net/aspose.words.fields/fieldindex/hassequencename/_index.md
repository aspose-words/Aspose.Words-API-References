---
title: FieldIndex.HasSequenceName
linktitle: HasSequenceName
articleTitle: HasSequenceName
second_title: Aspose.Words pour .NET
description: Découvrez si une séquence est nécessaire pour générer efficacement des résultats de champ grâce à la propriété FieldIndex HasSequenceName. Optimisez votre gestion de données dès aujourd'hui !
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
// Chaque entrée affichera la valeur de la propriété Texte du champ XE sur le côté gauche,
// et le numéro de la page qui contient le champ XE à droite.
// Si les champs XE ont la même valeur dans leur propriété « Texte »,
// le champ INDEX les regroupera en une seule entrée.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Dans la propriété SequenceName, nommez une séquence de champs SEQ. Chaque entrée de ce champ INDEX s'affichera désormais également.
// le numéro sur lequel se trouve le nombre de séquences à l'emplacement du champ XE qui a créé cette entrée.
index.SequenceName = "MySequence";

// Définissez le texte qui entourera la séquence et les numéros de page pour expliquer leur signification à l'utilisateur.
// Une entrée créée avec cette configuration affichera quelque chose comme « MySequence à 1 sur la page 1 » à son numéro de page.
// PageNumberSeparator et SequenceSeparator ne peuvent pas dépasser 15 caractères.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

// Les champs SEQ affichent un nombre qui augmente à chaque champ SEQ.
// Ces champs conservent également des comptes distincts pour chaque séquence nommée unique
// identifié par la propriété « SequenceIdentifier » du champ SEQ.
// Insérer un champ SEQ qui déplace la séquence « MySequence » à 1.
// Ce champ n'est pas différent du texte normal d'un document. Il n'apparaîtra pas dans la table des matières d'un champ INDEX.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// Insérez un champ XE qui créera une entrée dans le champ INDEX.
// Étant donné que « MySequence » est à 1 et que ce champ XE est à la page 2, avec les séparateurs personnalisés que nous avons définis ci-dessus,
// L'entrée INDEX de ce champ affichera « Cat » sur le côté gauche et « MySequence à 1 sur la page 2 » sur la droite.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// Insérez un saut de page et utilisez les champs SEQ pour faire avancer « MySequence » à 3.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// Insérer un champ XE avec la même propriété Texte que celle ci-dessus.
// L'entrée INDEX regroupera les champs XE avec des valeurs correspondantes dans la propriété « Texte »
// dans une seule entrée au lieu de créer une entrée pour chaque champ XE.
// Puisque nous sommes à la page 2 avec « MySequence » à 3, « 3 à la page 3 » sera ajouté à la même entrée INDEX que ci-dessus.
// La partie numéro de page de cette entrée INDEX affichera désormais « MySequence à 1 sur la page 2, 3 sur la page 3 ».
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

// Insérer un champ XE avec une valeur de propriété Text nouvelle et unique.
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
