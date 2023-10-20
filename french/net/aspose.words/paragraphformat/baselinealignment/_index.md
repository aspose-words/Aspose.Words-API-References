---
title: ParagraphFormat.BaselineAlignment
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words pour .NET
description: ParagraphFormat BaselineAlignment propriété. Obtient ou définit la position verticale des polices sur une ligne en C#.
type: docs
weight: 40
url: /fr/net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

Obtient ou définit la position verticale des polices sur une ligne.

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

## Exemples

Montre comment définir la position verticale des polices sur une ligne.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
if (format.BaselineAlignment == BaselineAlignment.Auto)
{                
    format.BaselineAlignment = BaselineAlignment.Top;
}

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### Voir également

* enum [BaselineAlignment](../../baselinealignment/)
* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
