---
title: ShapeBase.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase AllowOverlap, contrôlez les interactions des formes en activant ou en désactivant le chevauchement avec d'autres formes pour une flexibilité de conception améliorée.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

Obtient ou définit une valeur qui spécifie si cette forme peut chevaucher d'autres formes.

```csharp
public bool AllowOverlap { get; set; }
```

## Remarques

Cette propriété affecte le comportement de la forme dans Microsoft Word. Aspose.Words ignore la valeur de cette propriété.

Cette propriété s'applique uniquement aux formes de niveau supérieur.

La valeur par défaut est`vrai`.

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

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
