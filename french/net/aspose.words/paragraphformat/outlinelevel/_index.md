---
title: ParagraphFormat.OutlineLevel
second_title: Référence de l'API Aspose.Words pour .NET
description: ParagraphFormat propriété. Spécifie le niveau hiérarchique du paragraphe dans le document.
type: docs
weight: 240
url: /fr/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

Spécifie le niveau hiérarchique du paragraphe dans le document.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

### Exemples

Montre comment configurer les niveaux de plan de paragraphe pour créer du texte réductible.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Chaque paragraphe a un OutlineLevel, qui peut être n'importe quel nombre de 1 à 9, ou à la valeur "BodyText" par défaut.
// La définition de la propriété sur l'une des valeurs numérotées affichera une flèche vers la gauche
// du début du paragraphe.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Le niveau 1 est le niveau le plus élevé. S'il y a un paragraphe avec un niveau inférieur en dessous d'un paragraphe avec un niveau supérieur,
// réduire le paragraphe de niveau supérieur entraînera la réduction du paragraphe de niveau inférieur.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Deux paragraphes de même niveau ne se replieront pas,
// et les flèches ne réduisent pas les paragraphes vers lesquels elles pointent.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// La valeur "BodyText" par défaut est la plus basse, qu'un paragraphe de n'importe quel niveau peut réduire.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Voir également

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../paragraphformat/)
* Assemblée [Aspose.Words](../../../)


