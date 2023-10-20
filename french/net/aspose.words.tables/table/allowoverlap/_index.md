---
title: Table.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words pour .NET
description: Table AllowOverlap propriété. Obtient si une table flottante doit autoriser dautres objets flottants dans le document à chevaucher ses étendues lorsquils sont affichés. La valeur par défaut estvrai  en C#.
type: docs
weight: 70
url: /fr/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

Obtient si une table flottante doit autoriser d'autres objets flottants dans le document à chevaucher ses étendues lorsqu'ils sont affichés. La valeur par défaut est`vrai` .

```csharp
public bool AllowOverlap { get; }
```

## Exemples

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

* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
