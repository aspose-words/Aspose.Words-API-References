---
title: HtmlLoadOptions.BlockImportMode
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words pour .NET
description: HtmlLoadOptions BlockImportMode propriété. Obtient ou définit une valeur qui spécifie la manière dont les propriétés des éléments de niveau bloc sont importées. La valeur par défaut estMerge  en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.loading/htmlloadoptions/blockimportmode/
---
## HtmlLoadOptions.BlockImportMode property

Obtient ou définit une valeur qui spécifie la manière dont les propriétés des éléments de niveau bloc sont importées. La valeur par défaut estMerge .

```csharp
public BlockImportMode BlockImportMode { get; set; }
```

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

* enum [BlockImportMode](../../blockimportmode/)
* class [HtmlLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
