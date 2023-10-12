---
title: ReportingEngine.UseReflectionOptimization
second_title: Aspose.Words für .NET-API-Referenz
description: ReportingEngine eigendom. Ruft einen Wert ab oder legt diesen fest der angibt ob Aufrufe von benutzerdefinierten Typmitgliedern die über die ReflectionAPI ausgeführt werden mithilfe der dynamischen Klassengenerierung optimiert sind oder nicht. Der Standardwert istWAHR .
type: docs
weight: 70
url: /de/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Ruft einen Wert ab oder legt diesen fest, der angibt, ob Aufrufe von benutzerdefinierten Typmitgliedern, die über die Reflection-API ausgeführt werden, mithilfe der dynamischen Klassengenerierung optimiert sind oder nicht. Der Standardwert ist`WAHR` .

```csharp
public static bool UseReflectionOptimization { get; set; }
```

### Bemerkungen

Es gibt einige Szenarien, in denen es vorzuziehen ist, diese Optimierung zu deaktivieren. Wenn Sie beispielsweise ständig mit kleinen Sammlungen von Datenelementen arbeiten, kann ein Overhead der dynamischen Klassengenerierung auffälliger sein als ein Overhead direkter Reflektion-API-Aufrufe. Die Option hat keine Auswirkung, wenn sie ausgeführt wird iOS- und Reflexionsoptimierung werden nicht verwendet.

### Siehe auch

* class [ReportingEngine](../)
* namensraum [Aspose.Words.Reporting](../../reportingengine/)
* Montage [Aspose.Words](../../../)


