---
title: StyleCollection.Count
second_title: Référence de l'API Aspose.Words pour .NET
description: StyleCollection propriété. Obtient le nombre de styles dans la collection.
type: docs
weight: 10
url: /fr/net/aspose.words/stylecollection/count/
---
## StyleCollection.Count property

Obtient le nombre de styles dans la collection.

```csharp
public int Count { get; }
```

### Exemples

Montre comment ajouter un style à la collection de styles d'un document.

```csharp
Document doc = new Document();
StyleCollection styles = doc.Styles;

// Définissez les paramètres par défaut pour les nouveaux styles que nous pourrons ajouter ultérieurement à cette collection.
styles.DefaultFont.Name = "Courier New";

// Si nous ajoutons un style du "StyleType.Paragraph", la collection appliquera les valeurs de
// sa propriété "DefaultParagraphFormat" à la propriété "ParagraphFormat" du style.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;

// Ajoutez un style, puis vérifiez qu'il possède les paramètres par défaut.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Voir également

* class [StyleCollection](../)
* espace de noms [Aspose.Words](../../stylecollection/)
* Assemblée [Aspose.Words](../../../)


