---
title: BuiltInDocumentProperties.Manager
linktitle: Manager
articleTitle: Manager
second_title: Aspose.Words pour .NET
description: Gérez facilement vos propriétés BuiltInDocumentProperties grâce à notre outil intuitif. Obtenez ou définissez facilement des propriétés pour optimiser la gestion de vos documents.
type: docs
weight: 210
url: /fr/net/aspose.words.properties/builtindocumentproperties/manager/
---
## BuiltInDocumentProperties.Manager property

Obtient ou définit la propriété du gestionnaire.

```csharp
public string Manager { get; set; }
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
