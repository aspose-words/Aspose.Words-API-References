---
title: Table.HorizontalAnchor
second_title: Référence de l'API Aspose.Words pour .NET
description: Table propriété. Obtient lobjet de base à partir duquel le positionnement horizontal de la table flottante doit être calculé. La valeur par défaut estColumn .
type: docs
weight: 170
url: /fr/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

Obtient l'objet de base à partir duquel le positionnement horizontal de la table flottante doit être calculé. La valeur par défaut estColumn .

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
```

### Exemples

Montre comment utiliser les propriétés des tables flottantes.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // Seules les marges, pages et colonnes sont disponibles dans RelativeHorizontalPosition pour le setter HorizontalAnchor.
    // L'ArgumentException sera levée pour toutes les autres valeurs.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Seules les marges, pages et paragraphes sont disponibles dans RelativeVerticalPosition pour le setter VerticalAnchor.
    // L'ArgumentException sera levée pour toutes les autres valeurs.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Voir également

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../table/)
* Assemblée [Aspose.Words](../../../)


