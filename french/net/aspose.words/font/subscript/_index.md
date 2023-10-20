---
title: Font.Subscript
linktitle: Subscript
articleTitle: Subscript
second_title: Aspose.Words pour .NET
description: Font Subscript propriété. True si la police est formatée en indice en C#.
type: docs
weight: 430
url: /fr/net/aspose.words/font/subscript/
---
## Font.Subscript property

True si la police est formatée en indice.

```csharp
public bool Subscript { get; set; }
```

## Exemples

Montre comment formater le texte pour décaler sa position.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Élève cette séquence de texte de 5 points au-dessus de la ligne de base.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// Abaisse cette séquence de texte de 10 points en dessous de la ligne de base.
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

// Ajoute une séquence de texte normal.
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// Ajoute une séquence de texte qui apparaît en indice.
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// Ajoute une séquence de texte qui apparaît en exposant.
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
