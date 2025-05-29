---
title: MarkdownSaveOptions.OfficeMathExportMode
linktitle: OfficeMathExportMode
articleTitle: OfficeMathExportMode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété OfficeMathExportMode de MarkdownSaveOptions pour personnaliser la sortie OfficeMath. Optimisez vos fichiers grâce à des paramètres d'exportation flexibles !
type: docs
weight: 120
url: /fr/net/aspose.words.saving/markdownsaveoptions/officemathexportmode/
---
## MarkdownSaveOptions.OfficeMathExportMode property

Spécifie comment OfficeMath sera écrit dans le fichier de sortie. La valeur par défaut estText .

```csharp
public MarkdownOfficeMathExportMode OfficeMathExportMode { get; set; }
```

## Exemples

Montre comment OfficeMath sera écrit dans le document.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### Voir également

* enum [MarkdownOfficeMathExportMode](../../markdownofficemathexportmode/)
* class [MarkdownSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
