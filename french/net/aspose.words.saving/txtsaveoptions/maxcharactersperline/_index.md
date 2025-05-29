---
title: TxtSaveOptions.MaxCharactersPerLine
linktitle: MaxCharactersPerLine
articleTitle: MaxCharactersPerLine
second_title: Aspose.Words pour .NET
description: Découvrez TxtSaveOptions MaxCharactersPerLine, définissez facilement des limites de caractères par ligne pour une meilleure mise en forme du texte. La valeur par défaut est 0 pour un nombre illimité de caractères.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/txtsaveoptions/maxcharactersperline/
---
## TxtSaveOptions.MaxCharactersPerLine property

Obtient ou définit une valeur entière qui spécifie le nombre maximal de caractères par ligne. La valeur par défaut est 0, ce qui signifie aucune limite.

```csharp
public int MaxCharactersPerLine { get; set; }
```

## Exemples

Montre comment définir le nombre maximal de caractères par ligne.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Définissez 30 caractères comme maximum autorisé par ligne.
TxtSaveOptions saveOptions = new TxtSaveOptions { MaxCharactersPerLine = 30 };

doc.Save(ArtifactsDir + "TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

### Voir également

* class [TxtSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
