---
title: DocumentProperty.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words pour .NET
description: Découvrez la fonctionnalité DocumentProperty Name qui récupère sans effort les noms de propriétés, améliorant ainsi la gestion de vos documents et l'efficacité de votre flux de travail.
type: docs
weight: 30
url: /fr/net/aspose.words.properties/documentproperty/name/
---
## DocumentProperty.Name property

Renvoie le nom de la propriété.

```csharp
public string Name { get; }
```

## Remarques

Ne peut pas être`nul` et ne peut pas être une chaîne vide.

## Exemples

Montre comment travailler avec les propriétés de document intégrées.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// L'objet « Document » contient certaines de ses métadonnées dans ses membres.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// Le document stocke également des métadonnées dans ses propriétés intégrées.
// Chaque propriété intégrée est un membre de l'objet « BuiltInDocumentProperties » du document.
Console.WriteLine("Built-in Properties:");
foreach (DocumentProperty docProperty in doc.BuiltInDocumentProperties)
{
    Console.WriteLine(docProperty.Name);
    Console.WriteLine($"\tType:\t{docProperty.Type}");

    // Certaines propriétés peuvent stocker plusieurs valeurs.
    if (docProperty.Value is ICollection<object>)
    {
        foreach (object value in docProperty.Value as ICollection<object>)
            Console.WriteLine($"\tValue:\t\"{value}\"");
    }
    else
    {
        Console.WriteLine($"\tValue:\t\"{docProperty.Value}\"");
    }
}
```

### Voir également

* class [DocumentProperty](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
