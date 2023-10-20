---
title: Font.DoubleStrikeThrough
linktitle: DoubleStrikeThrough
articleTitle: DoubleStrikeThrough
second_title: Aspose.Words pour .NET
description: Font DoubleStrikeThrough propriété. Vrai si la police est formatée en texte double barré en C#.
type: docs
weight: 90
url: /fr/net/aspose.words/font/doublestrikethrough/
---
## Font.DoubleStrikeThrough property

Vrai si la police est formatée en texte double barré.

```csharp
public bool DoubleStrikeThrough { get; set; }
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
