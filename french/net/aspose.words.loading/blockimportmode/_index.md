---
title: BlockImportMode Enum
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words pour .NET
description: Découvrez comment l'énumération Aspose.Words.BlockImportMode améliore l'intégration des documents HTML en optimisant les importations de propriétés d'éléments au niveau du bloc pour des flux de travail transparents.
type: docs
weight: 4010
url: /fr/net/aspose.words.loading/blockimportmode/
---
## BlockImportMode enumeration

Spécifie comment les propriétés des éléments de niveau bloc sont importées à partir de documents HTML.

```csharp
public enum BlockImportMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Merge | `0` | Les propriétés des blocs parents sont fusionnées et stockées sur les éléments enfants (c'est-à-dire les paragraphes ou les tableaux). |
| Preserve | `1` | Les propriétés des blocs parents sont importées dans une structure logique spéciale et sont stockées séparément des nœuds de document. |

## Exemples

Montre comment les propriétés des éléments au niveau du bloc sont importées à partir de documents HTML.

```csharp
const string html = @"
<html>
    <div style='border:dotted'>
        <div style='border:solid'>
            <p>paragraph 1</p>
            <p>paragraph 2</p>
        </div>
    </div>
</html>";
MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(html));

HtmlLoadOptions loadOptions = new HtmlLoadOptions();
// Définissez le nouveau mode d'importation des éléments HTML au niveau du bloc.
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### Voir également

* espace de noms [Aspose.Words.Loading](../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../)
