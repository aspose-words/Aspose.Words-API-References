---
title: MergeFormatMode Enum
linktitle: MergeFormatMode
articleTitle: MergeFormatMode
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.LowCode.MergeFormatMode pour optimiser la fusion de documents. Améliorez le contrôle de la mise en forme lors de la combinaison simple de plusieurs fichiers.
type: docs
weight: 4290
url: /fr/net/aspose.words.lowcode/mergeformatmode/
---
## MergeFormatMode enumeration

Spécifie comment la mise en forme est fusionnée lors de la combinaison de plusieurs documents.

```csharp
public enum MergeFormatMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| MergeFormatting | `0` | Combinez la mise en forme des documents fusionnés. |
| KeepSourceFormatting | `1` | Signifie que le document source conservera sa mise en forme d'origine, comme les styles de police, les tailles, les couleurs, les retraits et tout autre élément de mise en forme appliqué à son contenu. |
| KeepSourceLayout | `2` | Conserver la mise en page des documents originaux dans le document final. |

## Exemples

Montre comment fusionner des documents en un seul document de sortie.

```csharp
//Il existe plusieurs façons de fusionner des documents :
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Voir également

* espace de noms [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../)
