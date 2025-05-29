---
title: HtmlLoadOptions.BlockImportMode
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété BlockImportMode de HtmlLoadOptions pour personnaliser l'importation d'éléments au niveau du bloc. Contrôlez la fusion pour une gestion optimale du contenu !
type: docs
weight: 20
url: /fr/net/aspose.words.loading/htmlloadoptions/blockimportmode/
---
## HtmlLoadOptions.BlockImportMode property

Obtient ou définit une valeur qui spécifie comment les propriétés des éléments de niveau bloc sont importées. La valeur par défaut estMerge .

```csharp
public BlockImportMode BlockImportMode { get; set; }
```

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

* enum [BlockImportMode](../../blockimportmode/)
* class [HtmlLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
