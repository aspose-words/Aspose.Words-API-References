---
title: TxtLoadOptions.AutoNumberingDetection
linktitle: AutoNumberingDetection
articleTitle: AutoNumberingDetection
second_title: Aspose.Words pour .NET
description: TxtLoadOptions AutoNumberingDetection propriété. Obtient ou définit une valeur booléenne indiquant que la détection automatique de la numérotation sera effectuée lors du chargement dun document. La valeur par défaut estvrai  en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

Obtient ou définit une valeur booléenne indiquant que la détection automatique de la numérotation sera effectuée lors du chargement d'un document. La valeur par défaut est`vrai` .

```csharp
public bool AutoNumberingDetection { get; set; }
```

## Exemples

Montre comment désactiver la détection automatique de la numérotation.

```csharp
TxtLoadOptions options = new TxtLoadOptions { AutoNumberingDetection = false };
Document doc = new Document(MyDir + "Number detection.txt", options);
```

### Voir également

* class [TxtLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
