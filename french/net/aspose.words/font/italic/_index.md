---
title: Font.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words pour .NET
description: Font Italic propriété. True si la police est au format italique en C#.
type: docs
weight: 160
url: /fr/net/aspose.words/font/italic/
---
## Font.Italic property

True si la police est au format italique.

```csharp
public bool Italic { get; set; }
```

## Exemples

Montre comment écrire du texte en italique à l’aide d’un générateur de documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Italic = true;
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "Font.Italic.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
