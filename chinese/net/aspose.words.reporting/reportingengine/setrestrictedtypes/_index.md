---
title: ReportingEngine.SetRestrictedTypes
linktitle: SetRestrictedTypes
articleTitle: SetRestrictedTypes
second_title: Aspose.Words for .NET
description: 了解 ReportingEngine 中的 SetRestrictedTypes 方法如何通过限制模板语法中的成员访问来增强安全性，从而优化数据报告。
type: docs
weight: 80
url: /zh/net/aspose.words.reporting/reportingengine/setrestrictedtypes/
---
## ReportingEngine.SetRestrictedTypes method

指定类型，哪些成员以及哪些派生类型的成员应该不能被引擎通过模板语法访问。

```csharp
public static void SetRestrictedTypes(params Type[] types)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| types | Type[] | 受到限制的类型。 |

## 评论

限制类型应在第一次构建报告之前设置。之后`构建报告`调用时，受限类型无法修改，尝试修改时会抛出异常 。设置受限类型的最佳时机是应用程序启动时。

请注意，大量受限类型可能会影响性能，因此最好只限制那些 类型，访问哪些成员确实很敏感。

投掷ArgumentException在下列情况下：

-*types*为空。

- 其中之一*types*项目是`无效的`。

- 其中之一*types*items 表示不可见类型，即非公共类型或 具有非公共外部类型的公共嵌套类型。

- 其中之一*types* items 表示数组类型。

-*types*包含重复的条目。

## 例子

展示如何拒绝对不安全类型的成员的访问。

```csharp
Document doc =
    DocumentHelper.CreateSimpleDocument(
        "<<var [typeVar = \"\".GetType().BaseType]>><<[typeVar]>>");

// 请注意，您不能在构建报告期间或之后设置受限类型。
ReportingEngine.SetRestrictedTypes(typeof(System.Type));
// 我们设置“AllowMissingMembers”选项以避免在构建报告期间出现异常。
ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.AllowMissingMembers };
engine.BuildReport(doc, new object());

// 我们得到一个空字符串，因为我们无法访问 GetType() 方法。
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### 也可以看看

* class [ReportingEngine](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)
