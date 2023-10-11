---
title: Font.StrikeThrough
second_title: Référence de l'API Aspose.Words pour .NET
description: Font propriété. Vrai si la police est formatée en texte barré.
type: docs
weight: 390
url: /fr/net/aspose.words/font/strikethrough/
---
## Font.StrikeThrough property

Vrai si la police est formatée en texte barré.

```csharp
public bool StrikeThrough { get; set; }
```

### Exemples

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
* espace de noms [Aspose.Words](../../font/)
* Assemblée [Aspose.Words](../../../)


