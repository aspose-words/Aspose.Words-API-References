---
title: FieldSeq.InsertNextNumber
linktitle: InsertNextNumber
articleTitle: InsertNextNumber
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldSeq InsertNextNumber pour gérer facilement les numéros de séquence de vos éléments. Optimisez l'organisation de vos données sans effort !
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldseq/insertnextnumber/
---
## FieldSeq.InsertNextNumber property

Obtient ou définit s'il faut insérer le numéro de séquence suivant pour l'élément spécifié.

```csharp
public bool InsertNextNumber { get; set; }
```

## Exemples

Les émissions créent une numérotation à l'aide de champs SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les champs SEQ affichent un nombre qui augmente à chaque champ SEQ.
// Ces champs conservent également des comptes distincts pour chaque séquence nommée unique
// identifié par la propriété « SequenceIdentifier » du champ SEQ.
// Insérer un champ SEQ qui affichera la valeur de comptage actuelle de « MySequence »,
// après avoir utilisé la propriété "ResetNumber" pour la définir à 100.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Affichez le numéro suivant dans cette séquence avec un autre champ SEQ.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// Insérer un titre de niveau 1.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Insérez un autre champ SEQ de la même séquence et configurez-le pour réinitialiser le compte à chaque en-tête avec 1.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// Le titre ci-dessus est un titre de niveau 1, donc le nombre de cette séquence est réinitialisé à 1.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Passer au numéro suivant de cette séquence.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.InsertNextNumber = true;
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\n", fieldSeq.GetFieldCode());
Assert.AreEqual("2", fieldSeq.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.ResetNumbering.docx");
```

### Voir également

* class [FieldSeq](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
