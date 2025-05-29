---
title: Document.CustomDocumentProperties
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words pour .NET
description: Explorez la propriété CustomDocumentProperties pour accéder et gérer efficacement toutes les propriétés de document personnalisées, améliorant ainsi les fonctionnalités de votre document.
type: docs
weight: 80
url: /fr/net/aspose.words/document/customdocumentproperties/
---
## Document.CustomDocumentProperties property

Renvoie une collection qui représente toutes les propriétés de document personnalisées du document.

```csharp
public CustomDocumentProperties CustomDocumentProperties { get; }
```

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

* class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
