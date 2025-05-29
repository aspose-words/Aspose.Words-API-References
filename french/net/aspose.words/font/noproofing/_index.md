---
title: Font.NoProofing
linktitle: NoProofing
articleTitle: NoProofing
second_title: Aspose.Words pour .NET
description: Découvrez Font NoProofing. Supprimez la vérification orthographique du texte formaté pour des designs plus nets. Améliorez vos documents avec précision et professionnalisme !
type: docs
weight: 280
url: /fr/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

Vrai lorsque les caractères formatés ne doivent pas être vérifiés orthographiquement.

```csharp
public bool NoProofing { get; set; }
```

## Exemples

Montre comment empêcher la vérification orthographique du texte par Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normalement, Microsoft Word met en évidence les fautes d'orthographe avec un soulignement rouge irrégulier.
// Nous pouvons désactiver l'indicateur « NoProofing » pour créer une partie de texte qui
// contourne le correcteur orthographique tout en le désactivant complètement.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
