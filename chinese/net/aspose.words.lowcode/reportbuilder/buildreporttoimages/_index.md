---
title: ReportBuilder.BuildReportToImages
linktitle: BuildReportToImages
articleTitle: BuildReportToImages
second_title: Aspose.Words for .NET
description: 使用 ReportBuilder 的 BuildReportToImages 方法轻松转换您的模板文档，将来自各种来源的数据组合成令人惊叹的图像。
type: docs
weight: 30
url: /zh/net/aspose.words.lowcode/reportbuilder/buildreporttoimages/
---
## BuildReportToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreporttoimages_1}

使用来自多个来源的数据填充模板文档。 将输出呈现为图像。

```csharp
public static Stream[] BuildReportToImages(string inputFileName, ImageSaveOptions saveOptions, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| saveOptions | ImageSaveOptions | 输出的保存选项。 |
| data | Object[] | 数据源对象数组。 |
| dataSourceNames | String[] | 用于引用模板内的数据源对象的名称数组。 |
| reportBuilderOptions | ReportBuilderOptions | 附加报告构建选项。 |

## 例子

展示如何使用数据源填充文档。

```csharp
public void BuildReportDataSource()
{
    // 有几种方法可以用数据源填充文档：
    string doc = MyDir + "Report building.docx";

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.1.docx", sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.2.docx", new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.3.docx", sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.4.docx", SaveFormat.Docx, sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.5.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.6.docx", SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.7.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.8.docx", new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(doc, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    ReportBuilder.Create(reportBuilderContext)
        .From(doc)
        .To(ArtifactsDir + "LowCode.BuildReportDataSource.9.docx")
        .Execute();
}

public class MessageTestClass
{
    public string Name { get; set; }
    public string Message { get; set; }

    public MessageTestClass(string name, string message)
    {
        Name = name;
        Message = message;
    }
}
```

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## BuildReportToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreporttoimages}

使用来自多个来源的数据填充模板文档。 将输出呈现为图像。

```csharp
public static Stream[] BuildReportToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入文件流。 |
| saveOptions | ImageSaveOptions | 输出的保存选项。 |
| data | Object[] | 数据源对象数组。 |
| dataSourceNames | String[] | 用于引用模板内的数据源对象的名称数组。 |
| reportBuilderOptions | ReportBuilderOptions | 附加报告构建选项。 |

## 例子

展示如何使用来自流的文档将数据源填充到文档中。

```csharp
// 有几种方法可以使用流中的文档将数据源填充到文档中：
MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

using (FileStream streamIn = new FileStream(MyDir + "Report building.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, new object[] { sender }, new[] { "s" });

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, sender, "s");

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.4.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.Create(reportBuilderContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
