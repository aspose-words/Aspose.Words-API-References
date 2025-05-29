---
title: Font.Kerning
linktitle: Kerning
articleTitle: Kerning
second_title: Aspose.Words pour .NET
description: Découvrez la fonction Crénage des polices et contrôlez le début du crénage pour une clarté et une mise en page optimales. Améliorez votre typographie avec précision !
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

Montre comment spécifier la taille de police à partir de laquelle le crénage commence à prendre effet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// Définissez la taille de la police du générateur et la taille minimale à laquelle le crénage prendra effet.
// La taille de la police tombe en dessous du seuil de crénage, donc l'exécution ci-dessous n'aura pas de crénage.
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// Définissez le seuil de crénage de sorte que la taille de police actuelle du générateur soit supérieure à celui-ci.
// Tout texte ajouté à partir de ce point sera soumis au crénage. Les espaces entre les caractères
// sera ajusté, ce qui donnera normalement un texte légèrement plus esthétique.
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
