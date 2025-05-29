---
title: Font.StrikeThrough
linktitle: StrikeThrough
articleTitle: StrikeThrough
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Police barrée. Formatez facilement votre texte avec le texte barré pour une mise en valeur visuelle claire dans vos créations. Améliorez la lisibilité dès aujourd'hui !
type: docs
weight: 400
url: /fr/net/aspose.words/font/strikethrough/
---
## Font.StrikeThrough property

Vrai si la police est formatée en texte barré.

```csharp
public bool StrikeThrough { get; set; }
```

## Exemples

Montre comment ajouter une ligne barrée au texte.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

Run run = new Run(doc, "Text with a single-line strikethrough.");
run.Font.StrikeThrough = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

run = new Run(doc, "Text with a double-line strikethrough.");
run.Font.DoubleStrikeThrough = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.StrikeThrough.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
