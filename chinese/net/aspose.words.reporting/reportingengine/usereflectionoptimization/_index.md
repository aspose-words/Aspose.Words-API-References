---
title: ReportingEngine.UseReflectionOptimization
second_title: Aspose.Words for .NET API 参考
description: ReportingEngine 财产. 获取或设置一个值该值指示通过反射 API 执行的自定义类型成员的调用是否使用动态类生成进行 优化默认值为真的.
type: docs
weight: 70
url: /zh/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

获取或设置一个值，该值指示通过反射 API 执行的自定义类型成员的调用是否使用动态类生成进行 优化。默认值为`真的`.

```csharp
public static bool UseReflectionOptimization { get; set; }
```

### 评论

在某些情况下最好禁用此优化。例如，如果您始终处理小型数据项集合，则动态类生成的开销可能比直接反射 API 调用的开销更明显。 该选项在运行时不起作用iOS和反射优化没有使用。

### 也可以看看

* class [ReportingEngine](../)
* 命名空间 [Aspose.Words.Reporting](../../reportingengine/)
* 部件 [Aspose.Words](../../../)


