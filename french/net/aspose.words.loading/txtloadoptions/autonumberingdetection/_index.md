---
title: TxtLoadOptions.AutoNumberingDetection
linktitle: AutoNumberingDetection
articleTitle: AutoNumberingDetection
second_title: Aspose.Words pour .NET
description: Découvrez la propriété AutoNumberingDetection de TxtLoadOptions. Activez ou désactivez facilement la numérotation automatique pour un chargement fluide des documents. La valeur par défaut est « true ».
type: docs
weight: 20
url: /fr/net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

Obtient ou définit une valeur booléenne indiquant que la détection de numérotation automatique sera effectuée lors du chargement d'un document. La valeur par défaut est`vrai` .

```csharp
public bool AutoNumberingDetection { get; set; }
```

## Exemples

Montre comment désactiver la détection automatique de numérotation.

```csharp
TxtLoadOptions options = new TxtLoadOptions { AutoNumberingDetection = false };
Document doc = new Document(MyDir + "Number detection.txt", options);
```

### Voir également

* class [TxtLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
