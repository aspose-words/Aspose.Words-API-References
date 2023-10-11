---
title: ReportingEngine.UseReflectionOptimization
second_title: Aspose.Words per .NET API Reference
description: ReportingEngine proprietà. Ottiene o imposta un valore che indica se le chiamate di membri di tipo personalizzato eseguite tramite lAPI di riflessione sono ottimizzate utilizzando la generazione di classi dinamiche o meno. Il valore predefinito èVERO .
type: docs
weight: 70
url: /it/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Ottiene o imposta un valore che indica se le chiamate di membri di tipo personalizzato eseguite tramite l'API di riflessione sono ottimizzate utilizzando la generazione di classi dinamiche o meno. Il valore predefinito è`VERO` .

```csharp
public static bool UseReflectionOptimization { get; set; }
```

### Osservazioni

Esistono alcuni scenari in cui è preferibile disabilitare questa ottimizzazione. Ad esempio, se hai a che fare continuamente con piccole raccolte di elementi di dati, un sovraccarico della generazione di classi dinamiche può essere più evidente di un sovraccarico delle chiamate API di riflessione diretta. L'opzione non ha effetto quando viene eseguita su iOS e l'ottimizzazione della riflessione non vengono utilizzati.

### Guarda anche

* class [ReportingEngine](../)
* spazio dei nomi [Aspose.Words.Reporting](../../reportingengine/)
* assemblea [Aspose.Words](../../../)


