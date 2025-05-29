---
title: BuiltInDocumentProperties.TotalEditingTime
linktitle: TotalEditingTime
articleTitle: TotalEditingTime
second_title: Aspose.Words pour .NET
description: Découvrez la propriété TotalEditingTime de BuiltInDocumentProperties pour suivre efficacement les modifications de vos documents. Optimisez votre flux de travail grâce à une gestion précise du temps d'édition.
type: docs
weight: 340
url: /fr/net/aspose.words.properties/builtindocumentproperties/totaleditingtime/
---
## BuiltInDocumentProperties.TotalEditingTime property

Obtient ou définit le temps total d'édition en minutes.

```csharp
public int TotalEditingTime { get; set; }
```

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
