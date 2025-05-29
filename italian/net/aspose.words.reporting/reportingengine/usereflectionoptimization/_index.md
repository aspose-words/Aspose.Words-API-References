---
title: ReportingEngine.UseReflectionOptimization
linktitle: UseReflectionOptimization
articleTitle: UseReflectionOptimization
second_title: Aspose.Words per .NET
description: Ottimizza le invocazioni dei membri di tipo personalizzato con la proprietà UseReflectionOptimization di ReportingEngine. Migliora le prestazioni con la generazione dinamica di classi per una maggiore efficienza.
type: docs
weight: 60
url: /it/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Ottiene o imposta un valore che indica se le invocazioni dei membri di tipo personalizzato eseguite tramite l'API di riflessione sono ottimizzate utilizzando la generazione dinamica di classi o meno. Il valore predefinito è`VERO` .

```csharp
public static bool UseReflectionOptimization { get; set; }
```

## Osservazioni

In alcuni scenari è preferibile disabilitare questa ottimizzazione. Ad esempio, se si gestiscono costantemente piccole raccolte di dati, il sovraccarico dovuto alla generazione di classi dinamiche può essere più evidente rispetto a quello dovuto alle chiamate API di riflessione diretta. L'opzione non ha effetto se eseguita su iOS e l'ottimizzazione della riflessione non viene utilizzata.

### Guarda anche

* class [ReportingEngine](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)
