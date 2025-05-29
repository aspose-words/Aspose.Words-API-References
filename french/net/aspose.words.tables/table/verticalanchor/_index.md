---
title: Table.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Table VerticalAnchor pour optimiser le positionnement des tableaux flottants. Apprenez à améliorer le contrôle de la mise en page grâce à sa valeur Marge par défaut.
type: docs
weight: 340
url: /fr/net/aspose.words.tables/table/verticalanchor/
---
## Table.VerticalAnchor property

Obtient l'objet de base à partir duquel le positionnement vertical du tableau flottant doit être calculé. La valeur par défaut estMargin .

```csharp
public RelativeVerticalPosition VerticalAnchor { get; set; }
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

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
