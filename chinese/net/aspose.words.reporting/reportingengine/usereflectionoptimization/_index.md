---
title: ReportingEngine.UseReflectionOptimization
linktitle: UseReflectionOptimization
articleTitle: UseReflectionOptimization
second_title: Aspose.Words for .NET
description: 使用 ReportingEngine 的 UseReflectionOptimization 属性优化自定义类型成员调用。通过动态类生成增强性能，从而提高效率。
type: docs
weight: 60
url: /zh/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

获取或设置一个值，指示通过反射 API 执行的自定义类型成员调用是否使用动态类生成进行优化。默认值为`真的`.

```csharp
public static bool UseReflectionOptimization { get; set; }
```

## 评论

在某些情况下，最好禁用此优化。例如，如果您一直在处理小型数据项集合，那么动态类生成的开销可能比直接调用反射 API 的开销更明显。 在 iOS 上运行时，如果未使用反射优化，则此选项无效。

### 也可以看看

* class [ReportingEngine](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)
