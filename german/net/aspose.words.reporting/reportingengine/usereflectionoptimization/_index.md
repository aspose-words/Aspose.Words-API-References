---
title: ReportingEngine.UseReflectionOptimization
linktitle: UseReflectionOptimization
articleTitle: UseReflectionOptimization
second_title: Aspose.Words für .NET
description: Optimieren Sie den Aufruf benutzerdefinierter Typmitglieder mit der UseReflectionOptimization-Eigenschaft von ReportingEngine. Verbessern Sie die Leistung durch dynamische Klassengenerierung für mehr Effizienz.
type: docs
weight: 60
url: /de/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Ruft einen Wert ab oder legt ihn fest, der angibt, ob Aufrufe von benutzerdefinierten Typmembern über die Reflection-API mithilfe der dynamischen Klassengenerierung optimiert werden. Der Standardwert ist`WAHR` .

```csharp
public static bool UseReflectionOptimization { get; set; }
```

## Bemerkungen

In einigen Szenarien ist es ratsam, diese Optimierung zu deaktivieren. Wenn Sie beispielsweise ständig mit kleinen Datenmengen arbeiten, kann der Aufwand für die dynamische Klassengenerierung deutlicher spürbar sein als der Aufwand für direkte Reflexions-API-Aufrufe. Die Option ist wirkungslos, wenn sie unter iOS ausgeführt wird und keine Reflexionsoptimierung verwendet wird.

### Siehe auch

* class [ReportingEngine](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)
