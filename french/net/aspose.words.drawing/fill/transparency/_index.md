---
title: Fill.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words pour .NET
description: Ajustez la transparence du remplissage de 0,0 (opaque) à 1,0 (transparent) pour personnaliser les effets visuels de vos créations. Améliorez l'esthétique de votre projet dès aujourd'hui !
type: docs
weight: 200
url: /fr/net/aspose.words.drawing/fill/transparency/
---
## Fill.Transparency property

Obtient ou définit le degré de transparence du remplissage spécifié sous la forme d'une valeur comprise entre 0,0 (opaque) et 1,0 (clair).

```csharp
public double Transparency { get; set; }
```

## Remarques

Cette propriété est l'opposé de la propriété[`Opacity`](../opacity/).

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

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
