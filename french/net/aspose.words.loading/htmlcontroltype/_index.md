---
title: HtmlControlType Enum
linktitle: HtmlControlType
articleTitle: HtmlControlType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.HtmlControlType pour une importation transparente des éléments d'entrée et de sélection HTML, améliorant ainsi vos capacités de traitement de documents.
type: docs
weight: 4060
url: /fr/net/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enumeration

Type de nœuds de document qui représentent les éléments &lt;input&gt; et &lt;select&gt; importés depuis HTML.

```csharp
public enum HtmlControlType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| FormField | `0` | Un champ de formulaire. |
| StructuredDocumentTag | `1` | Une balise de document structurée |

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

* espace de noms [Aspose.Words.Loading](../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../)
