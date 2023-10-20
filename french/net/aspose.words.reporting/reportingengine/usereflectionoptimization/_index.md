---
title: ReportingEngine.UseReflectionOptimization
linktitle: UseReflectionOptimization
articleTitle: UseReflectionOptimization
second_title: Aspose.Words pour .NET
description: ReportingEngine UseReflectionOptimization propriété. Obtient ou définit une valeur indiquant si les appels de membres de type personnalisé effectués via lAPI de réflexion sont optimisés à laide de la génération de classe dynamique ou non. La valeur par défaut estvrai  en C#.
type: docs
weight: 70
url: /fr/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Obtient ou définit une valeur indiquant si les appels de membres de type personnalisé effectués via l'API de réflexion sont optimisés à l'aide de la génération de classe dynamique ou non. La valeur par défaut est`vrai` .

```csharp
public static bool UseReflectionOptimization { get; set; }
```

## Remarques

Il existe certains scénarios dans lesquels il est préférable de désactiver cette optimisation. Par exemple, si vous traitez avec de petites collections d'éléments de données tout le temps, alors une surcharge de génération de classe dynamique peut être plus perceptible qu'une surcharge d'appels d'API de réflexion directe. L'option n'a aucun effet lorsqu'elle est exécutée sur L'optimisation iOS et la réflexion n'est pas utilisée.

### Voir également

* class [ReportingEngine](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)
