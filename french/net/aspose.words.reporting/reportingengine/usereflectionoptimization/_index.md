---
title: ReportingEngine.UseReflectionOptimization
linktitle: UseReflectionOptimization
articleTitle: UseReflectionOptimization
second_title: Aspose.Words pour .NET
description: Optimisez les appels de membres de types personnalisés avec la propriété UseReflectionOptimization de ReportingEngine. Améliorez les performances grâce à la génération dynamique de classes pour une efficacité accrue.
type: docs
weight: 60
url: /fr/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Obtient ou définit une valeur indiquant si les appels de membres de type personnalisé effectués via l'API de réflexion sont optimisés par la génération de classes dynamiques ou non. La valeur par défaut est`vrai` .

```csharp
public static bool UseReflectionOptimization { get; set; }
```

## Remarques

Dans certains cas, il est préférable de désactiver cette optimisation. Par exemple, si vous traitez en permanence de petites collections d'éléments de données, la surcharge liée à la génération de classes dynamiques peut être plus importante que celle liée aux appels d'API de réflexion directe. Cette option est sans effet lorsqu'elle est exécutée sur iOS et que l'optimisation de la réflexion n'est pas utilisée.

### Voir également

* class [ReportingEngine](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)
