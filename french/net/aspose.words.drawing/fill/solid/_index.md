---
title: Fill.Solid
second_title: Référence de l'API Aspose.Words pour .NET
description: Fill méthode. Définit le remplissage sur une couleur uniforme.
type: docs
weight: 200
url: /fr/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

Définit le remplissage sur une couleur uniforme.

```csharp
public void Solid()
```

### Remarques

Utilisez cette méthode pour reconvertir n'importe lequel des remplissages en remplissage solide.

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../fill/)
* Assemblée [Aspose.Words](../../../)

---

## Solid(Color) {#solid_1}

Définit le remplissage sur une couleur uniforme spécifiée.

```csharp
public void Solid(Color color)
```

### Remarques

Utilisez cette méthode pour reconvertir n'importe lequel des remplissages en remplissage solide.

### Exemples

Montre comment reconvertir n'importe lequel des remplissages en remplissage uni.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Obtient l'objet Fill pour la police de la première exécution.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Vérifie les propriétés de remplissage de la police.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Modifie le type de remplissage en Solide avec une couleur verte uniforme.
fill.Solid(Color.Green);
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../fill/)
* Assemblée [Aspose.Words](../../../)


