---
title: Table.VerticalAnchor
second_title: Référence de l'API Aspose.Words pour .NET
description: Table propriété. Obtient lobjet de base à partir duquel le positionnement vertical de la table flottante doit être calculé. La valeur par défaut estMargin .
type: docs
weight: 340
url: /fr/net/aspose.words.tables/table/verticalanchor/
---
## Table.VerticalAnchor property

Obtient l'objet de base à partir duquel le positionnement vertical de la table flottante doit être calculé. La valeur par défaut estMargin .

```csharp
public RelativeVerticalPosition VerticalAnchor { get; set; }
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

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../table/)
* Assemblée [Aspose.Words](../../../)


