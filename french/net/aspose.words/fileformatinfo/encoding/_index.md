---
title: FileFormatInfo.Encoding
second_title: Référence de l'API Aspose.Words pour .NET
description: FileFormatInfo propriété. Obtient lencodage détecté sil est applicable au format de document actuel. Détecte pour le moment lencodage uniquement pour les documents HTML.
type: docs
weight: 10
url: /fr/net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

Obtient l'encodage détecté s'il est applicable au format de document actuel. Détecte pour le moment l'encodage uniquement pour les documents HTML.

```csharp
public Encoding Encoding { get; }
```

### Exemples

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
* espace de noms [Aspose.Words](../../fileformatinfo/)
* Assemblée [Aspose.Words](../../../)


