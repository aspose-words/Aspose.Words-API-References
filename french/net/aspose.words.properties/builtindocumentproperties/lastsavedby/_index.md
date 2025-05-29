---
title: BuiltInDocumentProperties.LastSavedBy
linktitle: LastSavedBy
articleTitle: LastSavedBy
second_title: Aspose.Words pour .NET
description: Découvrez la propriété BuiltInDocumentProperties LastSavedBy pour gérer facilement la paternité des documents et améliorer la collaboration dans vos projets.
type: docs
weight: 170
url: /fr/net/aspose.words.properties/builtindocumentproperties/lastsavedby/
---
## BuiltInDocumentProperties.LastSavedBy property

Obtient ou définit le nom du dernier auteur.

```csharp
public string LastSavedBy { get; set; }
```

## Remarques

Aspose.Words ne met pas à jour cette propriété.

## Exemples

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
