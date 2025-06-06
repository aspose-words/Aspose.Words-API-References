---
title: Font.Subscript
linktitle: Subscript
articleTitle: Subscript
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Indice de police. Formatez facilement votre texte en indice pour une meilleure lisibilité et un style amélioré dans vos documents. Optimisez votre design dès aujourd'hui !
type: docs
weight: 440
url: /fr/net/aspose.words/font/subscript/
---
## Font.Subscript property

Vrai si la police est formatée en indice.

```csharp
public bool Subscript { get; set; }
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
