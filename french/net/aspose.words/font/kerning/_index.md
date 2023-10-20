---
title: Font.Kerning
linktitle: Kerning
articleTitle: Kerning
second_title: Aspose.Words pour .NET
description: Font Kerning propriété. Obtient ou définit la taille de police à laquelle le crénage commence en C#.
type: docs
weight: 180
url: /fr/net/aspose.words/font/kerning/
---
## Font.Kerning property

Obtient ou définit la taille de police à laquelle le crénage commence.

```csharp
public double Kerning { get; set; }
```

## Exemples

Montre comment spécifier la taille de police à laquelle le crénage commence à prendre effet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// Définit la taille de police du générateur et la taille minimale à laquelle le crénage prendra effet.
// La taille de la police tombe en dessous du seuil de crénage, donc l'exécution ci-dessous n'aura pas de crénage.
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// Définit le seuil de crénage pour que la taille de police actuelle du générateur soit au-dessus.
// Tout texte que nous ajoutons à partir de ce point aura un crénage appliqué. Les espaces entre les caractères
// sera ajusté, ce qui entraînera normalement un texte légèrement plus esthétique.
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
