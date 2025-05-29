---
title: DocumentProperty Class
linktitle: DocumentProperty
articleTitle: DocumentProperty
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Properties.DocumentProperty pour gérer efficacement les propriétés de document personnalisées et intégrées. Améliorez la gestion de vos documents dès aujourd'hui !
type: docs
weight: 5200
url: /fr/net/aspose.words.properties/documentproperty/
---
## DocumentProperty class

Représente une propriété de document personnalisée ou intégrée.

Pour en savoir plus, visitez le[Travailler avec les propriétés du document](https://docs.aspose.com/words/net/work-with-document-properties/) article de documentation.

```csharp
public class DocumentProperty
```

## Propriétés

| Nom | La description |
| --- | --- |
| [IsLinkToContent](../../aspose.words.properties/documentproperty/islinktocontent/) { get; } | Indique si cette propriété est liée au contenu ou non. |
| [LinkSource](../../aspose.words.properties/documentproperty/linksource/) { get; } | Obtient la source d'une propriété de document personnalisé liée. |
| [Name](../../aspose.words.properties/documentproperty/name/) { get; } | Renvoie le nom de la propriété. |
| [Type](../../aspose.words.properties/documentproperty/type/) { get; } | Obtient le type de données de la propriété. |
| [Value](../../aspose.words.properties/documentproperty/value/) { get; set; } | Obtient ou définit la valeur de la propriété. |

## Méthodes

| Nom | La description |
| --- | --- |
| [ToBool](../../aspose.words.properties/documentproperty/tobool/)() | Renvoie la valeur de la propriété sous forme booléenne. |
| [ToByteArray](../../aspose.words.properties/documentproperty/tobytearray/)() | Renvoie la valeur de la propriété sous forme de tableau d'octets. |
| [ToDateTime](../../aspose.words.properties/documentproperty/todatetime/)() | Renvoie la valeur de la propriété sous la forme**Date et heure** en UTC. |
| [ToDouble](../../aspose.words.properties/documentproperty/todouble/)() | Renvoie la valeur de la propriété sous forme de double. |
| [ToInt](../../aspose.words.properties/documentproperty/toint/)() | Renvoie la valeur de la propriété sous forme d'entier. |
| override [ToString](../../aspose.words.properties/documentproperty/tostring/)() | Renvoie la valeur de la propriété sous forme de chaîne formatée selon les paramètres régionaux actuels. |

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

* class [DocumentPropertyCollection](../documentpropertycollection/)
* espace de noms [Aspose.Words.Properties](../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../)
