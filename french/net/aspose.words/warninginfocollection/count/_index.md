---
title: WarningInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words pour .NET
description: Découvrez la propriété WarningInfoCollection Count pour accéder facilement au nombre total d'éléments de votre collection pour une gestion efficace des données.
type: docs
weight: 20
url: /fr/net/aspose.words/warninginfocollection/count/
---
## WarningInfoCollection.Count property

Obtient le nombre d'éléments contenus dans la collection.

```csharp
public int Count { get; }
```

## Exemples

Montre comment obtenir des avertissements sur les formats non pris en charge.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### Voir également

* class [WarningInfoCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
