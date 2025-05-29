---
title: BuiltInDocumentProperties.RevisionNumber
linktitle: RevisionNumber
articleTitle: RevisionNumber
second_title: Aspose.Words pour .NET
description: Gérez le numéro de révision de votre document avec BuiltInDocumentProperties. Suivez facilement les modifications et optimisez le contrôle des versions pour une meilleure collaboration.
type: docs
weight: 250
url: /fr/net/aspose.words.properties/builtindocumentproperties/revisionnumber/
---
## BuiltInDocumentProperties.RevisionNumber property

Obtient ou définit le numéro de révision du document.

```csharp
public int RevisionNumber { get; set; }
```

## Remarques

Aspose.Words ne met pas à jour cette propriété.

## Exemples

Montre comment travailler avec les champs REVNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Current revision #");

// Insérer un champ REVNUM, qui affiche la propriété du numéro de révision actuel du document.
FieldRevNum field = (FieldRevNum)builder.InsertField(FieldType.FieldRevisionNum, true);

Assert.AreEqual(" REVNUM ", field.GetFieldCode());
Assert.AreEqual("1", field.Result);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.RevisionNumber);

// Cette propriété compte combien de fois un document a été enregistré dans Microsoft Word,
// et n'est pas lié aux révisions suivies. On peut le trouver en faisant un clic droit sur le document dans l'Explorateur Windows.
// via Propriétés -> Détails. Nous pouvons mettre à jour cette propriété manuellement.
doc.BuiltInDocumentProperties.RevisionNumber++;
field.Update();

Assert.AreEqual("2", field.Result);
```

Montre comment travailler avec les propriétés du document dans la catégorie « Origine ».

```csharp
// Ouvrez un document que nous avons créé et modifié à l’aide de Microsoft Word.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Les propriétés intégrées suivantes contiennent des informations concernant la création et la modification de ce document.
// Nous pouvons cliquer avec le bouton droit de la souris sur ce document dans l'Explorateur Windows et trouver
// ces propriétés via la catégorie "Propriétés" -> "Détails" -> "Origine".
// Des champs tels que PRINTDATE et EDITTIME peuvent afficher ces valeurs dans le corps du document.
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// Nous pouvons également modifier les valeurs des propriétés intégrées.
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// Microsoft Word met à jour automatiquement les propriétés suivantes lorsque nous enregistrons le document.
// Pour utiliser ces propriétés avec Aspose.Words, nous devrons définir leurs valeurs manuellement.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// Nous pouvons cliquer avec le bouton droit de la souris sur ce document dans l'Explorateur Windows et trouver these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### Voir également

* class [BuiltInDocumentProperties](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
