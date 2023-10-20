---
title: Fill.Solid
linktitle: Solid
articleTitle: Solid
second_title: Aspose.Words pour .NET
description: Fill Solid méthode. Définit le remplissage sur une couleur uniforme en C#.
type: docs
weight: 250
url: /fr/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

Définit le remplissage sur une couleur uniforme.

```csharp
public void Solid()
```

## Remarques

Utilisez cette méthode pour reconvertir n'importe quel remplissage en remplissage solide.

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)

---

## Solid(*Color*) {#solid_1}

Définit le remplissage sur une couleur uniforme spécifiée.

```csharp
public void Solid(Color color)
```

## Remarques

Utilisez cette méthode pour reconvertir n'importe quel remplissage en remplissage solide.

## Exemples

Montre comment reconvertir n’importe quel remplissage en remplissage solide.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Récupère l'objet Fill pour la police de la première exécution.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Vérifiez les propriétés de remplissage de la police.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Change le type de remplissage en Solid avec une couleur verte uniforme.
fill.Solid(Color.Green);
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
