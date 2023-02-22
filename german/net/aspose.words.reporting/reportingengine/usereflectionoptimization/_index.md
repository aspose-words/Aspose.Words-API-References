---
title: ReportingEngine.UseReflectionOptimization
second_title: Aspose.Words für .NET-API-Referenz
description: ReportingEngine eigendom. Ruft einen Wert ab oder legt einen Wert fest der angibt ob Aufrufe benutzerdefinierter Typmember die über die ReflektionsAPI ausgeführt werden mit dynamischer Klassengenerierung optimiert werden oder nicht. Der Standardwert ist true.
type: docs
weight: 70
url: /de/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob Aufrufe benutzerdefinierter Typmember, die über die Reflektions-API ausgeführt werden, mit dynamischer Klassengenerierung optimiert werden oder nicht. Der Standardwert ist true.

```csharp
public static bool UseReflectionOptimization { get; set; }
```

### Bemerkungen

Es gibt einige Szenarien, in denen es vorzuziehen ist, diese Optimierung zu deaktivieren. Wenn Sie beispielsweise die ganze Zeit mit kleinen Sammlungen von Datenelementen arbeiten, dann kann ein Overhead der dynamischen Klassengenerierung stärker spürbar sein als ein Overhead von direkten Reflection-API-Aufrufen. Die Option hat keine Auswirkung, wenn sie ausgeführt wird iOS und Reflection-Optimierung werden nicht verwendet.

### Siehe auch

* class [ReportingEngine](../)
* namensraum [Aspose.Words.Reporting](../../reportingengine/)
* Montage [Aspose.Words](../../../)


