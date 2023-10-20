---
title: LoadOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words pour .NET
description: LoadOptions Encoding propriété. Obtient ou définit lencodage qui sera utilisé pour charger un document HTML TXT ou CHM si lencodage nest pas spécifié à lintérieur du document. Peut êtrenul . La valeur par défaut estnul  en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Obtient ou définit l'encodage qui sera utilisé pour charger un document HTML, TXT ou CHM si l'encodage n'est pas spécifié à l'intérieur du document. Peut être`nul` . La valeur par défaut est`nul` .

```csharp
public Encoding Encoding { get; set; }
```

## Remarques

Cette propriété est utilisée uniquement lors du chargement de documents HTML, TXT ou CHM.

Si l'encodage n'est pas spécifié à l'intérieur du document et que cette propriété est`nul`le système essaiera de détecter automatiquement l'encodage to .

## Exemples

Montre comment définir l’encodage avec lequel ouvrir un document.

```csharp
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.ASCII
};

// Charge le document en passant l'objet LoadOptions, puis vérifie le contenu du document.
Document doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.True(doc.ToString(SaveFormat.Text).Contains("This is a sample text in English."));
```

### Voir également

* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
