---
title: Font.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Position de la police  ajustez facilement l'alignement du texte en points pour un contrôle précis de votre typographie. Sublimez votre design grâce à un positionnement flexible !
type: docs
weight: 310
url: /fr/net/aspose.words/font/position/
---
## Font.Position property

Obtient ou définit la position du texte (en points) par rapport à la ligne de base. Un nombre positif élève le texte et un nombre négatif l'abaisse.

```csharp
public double Position { get; set; }
```

## Exemples

Montre comment formater du texte pour décaler sa position.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Élevez cette séquence de texte de 5 points au-dessus de la ligne de base.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// Abaissez cette séquence de texte de 10 points en dessous de la ligne de base.
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

// Ajouter une série de texte normal.
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// Ajoutez une série de texte qui apparaît en indice.
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// Ajoutez une série de texte qui apparaît en exposant.
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
