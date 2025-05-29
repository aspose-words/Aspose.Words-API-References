---
title: FileFormatInfo.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: Aspose.Words pour .NET
description: Découvrez si votre document contient des macros VBA grâce à la propriété FileFormatInfo HasMacros. Assurez la sécurité et la fonctionnalité de vos documents dès aujourd'hui !
type: docs
weight: 30
url: /fr/net/aspose.words/fileformatinfo/hasmacros/
---
## FileFormatInfo.HasMacros property

Retours`vrai` si ce document contient des macros VBA.

```csharp
public bool HasMacros { get; }
```

## Exemples

Montre comment vérifier la présence d'une macro VBA sans charger le document.

```csharp
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Macro.docm");
Assert.IsTrue(fileFormatInfo.HasMacros);
```

### Voir également

* class [FileFormatInfo](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
