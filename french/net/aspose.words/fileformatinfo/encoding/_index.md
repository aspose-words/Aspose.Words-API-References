---
title: FileFormatInfo.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words pour .NET
description: Découvrez la propriété d'encodage FileFormatInfo pour identifier facilement l'encodage des documents. Prise en charge des formats HTML pour des résultats précis.
type: docs
weight: 10
url: /fr/net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

Obtient l'encodage détecté s'il s'applique au format de document actuel. Détecte actuellement l'encodage uniquement pour les documents HTML.

```csharp
public Encoding Encoding { get; }
```

## Exemples

Montre comment détecter l'encodage dans un fichier HTML.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// La propriété Encoding est utilisée uniquement lorsque nous créons un objet FileFormatInfo pour un document HTML.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Voir également

* class [FileFormatInfo](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
