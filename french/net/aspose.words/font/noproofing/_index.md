---
title: Font.NoProofing
second_title: Référence de l'API Aspose.Words pour .NET
description: Font propriété. Vrai lorsque les caractères formatés ne doivent pas être vérifiés orthographiquement.
type: docs
weight: 280
url: /fr/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

Vrai lorsque les caractères formatés ne doivent pas être vérifiés orthographiquement.

```csharp
public bool NoProofing { get; set; }
```

### Exemples

Montre comment empêcher la vérification orthographique du texte par Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normalement, Microsoft Word met l'accent sur les fautes d'orthographe avec un soulignement rouge irrégulier.
// Nous pouvons désactiver le drapeau "NoProofing" pour créer une portion de texte qui
// contourne le correcteur orthographique tout en le désactivant complètement.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../font/)
* Assemblée [Aspose.Words](../../../)


