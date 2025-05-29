---
title: Fill.FillType
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words pour .NET
description: Découvrez comment définir efficacement la propriété FillType et améliorer votre conception avec des options de remplissage personnalisables pour un meilleur impact visuel.
type: docs
weight: 60
url: /fr/net/aspose.words.drawing/fill/filltype/
---
## Fill.FillType property

Obtient un type de remplissage.

```csharp
public FillType FillType { get; }
```

## Exemples

Montre comment reconvertir n'importe quel remplissage en remplissage solide.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Obtenir l'objet Fill pour la police de la première exécution.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Vérifiez les propriétés de remplissage de la police.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Changez le type de remplissage en Solide avec une couleur verte uniforme.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Voir également

* enum [FillType](../../filltype/)
* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
