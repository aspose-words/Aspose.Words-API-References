---
title: WarningInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: Accédez facilement à des éléments spécifiques de WarningInfoCollection par index. Simplifiez la gestion de vos données grâce à notre fonctionnalité intuitive de propriétés !
type: docs
weight: 30
url: /fr/net/aspose.words/warninginfocollection/item/
---
## WarningInfoCollection indexer

Obtient un élément à l'index spécifié.

```csharp
public WarningInfo this[int index] { get; }
```

| Paramètre | La description |
| --- | --- |
| index | Index de base zéro de l'élément. |

## Exemples

Montre comment obtenir des avertissements sur les formats non pris en charge.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### Voir également

* class [WarningInfo](../../warninginfo/)
* class [WarningInfoCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
