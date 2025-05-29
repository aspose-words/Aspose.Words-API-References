---
title: CleanupOptions Class
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.CleanupOptions pour personnaliser le nettoyage de vos documents. Améliorez votre flux de travail grâce à des paramètres personnalisés pour des documents plus propres et plus efficaces.
type: docs
weight: 400
url: /fr/net/aspose.words/cleanupoptions/
---
## CleanupOptions class

Permet de spécifier des options pour le nettoyage des documents.

Pour en savoir plus, visitez le[Nettoyer un document](https://docs.aspose.com/words/net/clean-up-a-document/) article de documentation.

```csharp
public class CleanupOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [CleanupOptions](cleanupoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DuplicateStyle](../../aspose.words/cleanupoptions/duplicatestyle/) { get; set; } | Obtient/définit un indicateur indiquant si les styles en double doivent être supprimés du document. La valeur par défaut est`FAUX` . |
| [UnusedBuiltinStyles](../../aspose.words/cleanupoptions/unusedbuiltinstyles/) { get; set; } | Spécifie que non utilisé[`BuiltIn`](../style/builtin/) les styles doivent être supprimés du document. |
| [UnusedLists](../../aspose.words/cleanupoptions/unusedlists/) { get; set; } | Spécifie si la liste inutilisée et les définitions de liste doivent être supprimées du document. La valeur par défaut est`vrai` . |
| [UnusedStyles](../../aspose.words/cleanupoptions/unusedstyles/) { get; set; } | Spécifie si les styles inutilisés doivent être supprimés du document. La valeur par défaut est`vrai` . |

## Exemples

Montre comment supprimer tous les styles personnalisés inutilisés d'un document.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// Combiné aux styles intégrés, le document dispose désormais de huit styles.
// Un style personnalisé est marqué comme « utilisé » tant qu'il y a du texte dans le document
// formaté dans ce style. Cela signifie que les quatre styles ajoutés sont actuellement inutilisés.
Assert.AreEqual(8, doc.Styles.Count);

// Appliquez un style de caractère personnalisé, puis un style de liste personnalisé. Cela les marquera comme « utilisés ».
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Il y a maintenant un style de caractère inutilisé et un style de liste inutilisé.
// La méthode Cleanup(), lorsqu'elle est configurée avec un objet CleanupOptions, peut cibler les styles inutilisés et les supprimer.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // La suppression de chaque nœud auquel un style personnalisé est appliqué le marque à nouveau comme « inutilisé ».
// Réexécutez la méthode Cleanup pour les supprimer.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
