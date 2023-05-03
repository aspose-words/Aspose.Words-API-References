---
title: ReportingEngine.UseReflectionOptimization
linktitle: UseReflectionOptimization
articleTitle: UseReflectionOptimization
second_title: Aspose.Words for .NET API Reference
description: ReportingEngine UseReflectionOptimization property. Gets or sets a value indicating whether invocations of custom type members performed via reflection API are optimized using dynamic class generation or not. The default value is true in C#.
type: docs
weight: 70
url: /net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Gets or sets a value indicating whether invocations of custom type members performed via reflection API are optimized using dynamic class generation or not. The default value is `true`.

```csharp
public static bool UseReflectionOptimization { get; set; }
```

## Remarks

There are some scenarios where it is preferrable to disable this optimization. For example, if you are dealing with small collections of data items all the time, then an overhead of dynamic class generation can be more noticeable than an overhead of direct reflection API calls. The option does not have effect when run on iOS and reflection optimization is not used.

### See Also

* class [ReportingEngine](../)
* namespace [Aspose.Words.Reporting](../../reportingengine/)
* assembly [Aspose.Words](../../../)
