---
title: Font.Fill
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Remplissage de police pour améliorer l'apparence de votre texte avec un formatage de remplissage personnalisable pour un look soigné et professionnel.
type: docs
weight: 130
url: /fr/net/aspose.words/font/fill/
---
## Font.Fill property

Obtient le formatage de remplissage pour le[`Font`](../) .

```csharp
public Fill Fill { get; }
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

* class [Fill](../../../aspose.words.drawing/fill/)
* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
