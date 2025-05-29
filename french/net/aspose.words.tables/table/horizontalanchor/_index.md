---
title: Table.HorizontalAnchor
linktitle: HorizontalAnchor
articleTitle: HorizontalAnchor
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Table HorizontalAnchor pour optimiser le positionnement des tableaux flottants. Personnalisez facilement l'alignement horizontal pour un meilleur contrôle de la mise en page.
type: docs
weight: 170
url: /fr/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

Obtient l'objet de base à partir duquel le positionnement horizontal du tableau flottant doit être calculé. La valeur par défaut estColumn .

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
```

## Exemples

Montre comment travailler avec les propriétés des tables flottantes.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // Seules Marge, Page, Colonne sont disponibles dans RelativeHorizontalPosition pour le setter HorizontalAnchor.
    // L'ArgumentException sera levée pour toute autre valeur.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Seules Marge, Page, Paragraphe sont disponibles dans RelativeVerticalPosition pour le setter VerticalAnchor.
    // L'ArgumentException sera levée pour toute autre valeur.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Voir également

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
