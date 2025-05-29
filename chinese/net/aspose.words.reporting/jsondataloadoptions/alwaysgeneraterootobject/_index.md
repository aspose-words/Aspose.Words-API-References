---
title: JsonDataLoadOptions.AlwaysGenerateRootObject
linktitle: AlwaysGenerateRootObject
articleTitle: AlwaysGenerateRootObject
second_title: Aspose.Words for .NET
description: 了解 JsonDataLoadOptions AlwaysGenerateRootObject 属性如何通过确保一致的根对象实现无缝集成来增强 JSON 数据处理。
type: docs
weight: 20
url: /zh/net/aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/
---
## JsonDataLoadOptions.AlwaysGenerateRootObject property

获取或设置一个标志，指示生成的数据源是否始终包含 JSON 根元素的对象。如果 JSON 根元素包含单个复杂属性，则默认情况下不会创建此类对象。

```csharp
public bool AlwaysGenerateRootObject { get; set; }
```

## 评论

默认值为`错误的`.

## 例子

展示如何使用 JSON 作为数据源（字符串）。

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"},
    AlwaysGenerateRootObject = true,
    PreserveSpaces = true,
    SimpleValueParseMode = JsonSimpleValueParseMode.Loose
};

JsonDataSource dataSource = new JsonDataSource(MyDir + "List of people.json", options);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataString.docx");
```

### 也可以看看

* class [JsonDataLoadOptions](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)
