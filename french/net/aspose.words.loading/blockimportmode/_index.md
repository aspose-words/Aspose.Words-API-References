---
title: BlockImportMode Enum
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words pour .NET
description: Aspose.Words.Loading.BlockImportMode énumération. Spécifie comment les propriétés des éléments de niveau bloc sont importées à partir de documents HTML en C#.
type: docs
weight: 3560
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
| Preserve | `1` | Les propriétés des blocs parents sont importées dans une structure logique spéciale et sont stockées séparément des nœuds du document . |

## Exemples

Montre comment les propriétés des éléments de niveau bloc sont importées à partir de documents HTML.

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
// Définit le nouveau mode d'importation des éléments HTML au niveau du bloc.
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### Voir également

* espace de noms [Aspose.Words.Loading](../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../)
