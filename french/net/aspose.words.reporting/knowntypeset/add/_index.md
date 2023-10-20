---
title: KnownTypeSet.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words pour .NET
description: KnownTypeSet Add méthode. Ajoute le spécifiéType sopposer à lensemble. JetésArgumentException in les cas suivants  en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.reporting/knowntypeset/add/
---
## KnownTypeSet.Add method

Ajoute le spécifiéType s'opposer à l'ensemble. JetésArgumentException in les cas suivants :

-*type* est`nul`.

-*type* représente un type vide.

-*type* représente un type invisible, c'est-à-dire un type non public ou un type public imbriqué qui a un type externe non public.

-*type* représente un type générique.

-*type* représente un type de tableau.

-*type* a déjà été ajouté à l'ensemble.

```csharp
public void Add(Type type)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| type | Type | UNType objet à ajouter. |

### Voir également

* class [KnownTypeSet](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)
