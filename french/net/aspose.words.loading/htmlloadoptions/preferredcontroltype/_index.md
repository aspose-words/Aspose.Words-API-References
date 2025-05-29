---
title: HtmlLoadOptions.PreferredControlType
linktitle: PreferredControlType
articleTitle: PreferredControlType
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PreferredControlType de HtmlLoadOptions pour personnaliser les types de nœuds de document pour les entrées importées et sélectionner des éléments. Optimisez vos formulaires sans effort !
type: docs
weight: 50
url: /fr/net/aspose.words.loading/htmlloadoptions/preferredcontroltype/
---
## HtmlLoadOptions.PreferredControlType property

Obtient ou définit le type préféré de nœuds de document qui représenteront les éléments &lt;input&gt; et &lt;select&gt; importés. La valeur par défaut estFormField .

```csharp
public HtmlControlType PreferredControlType { get; set; }
```

## Remarques

Veuillez noter que la définition de cette propriété ne garantit pas que tous les contrôles importés seront du type spécifié. Si un contrôle HTML n'est pas représentable avec des nœuds de document du type préféré, Aspose.Words utilisera un type compatible[`HtmlControlType`](../../htmlcontroltype/) pour ce contrôle.

## Exemples

Montre comment définir le type préféré de nœuds de document qui représenteront les éléments &lt;input&gt; et &lt;select&gt; importés.

```csharp
const string html = @"
    <html>
        <select name='ComboBox' size='1'>
            <option value='val1'>item1</option>
            <option value='val2'></option>
        </select>
    </html>
";

HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
htmlLoadOptions.PreferredControlType = HtmlControlType.StructuredDocumentTag;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), htmlLoadOptions);
NodeCollection nodes = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

StructuredDocumentTag tag = (StructuredDocumentTag) nodes[0];
```

### Voir également

* enum [HtmlControlType](../../htmlcontroltype/)
* class [HtmlLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
