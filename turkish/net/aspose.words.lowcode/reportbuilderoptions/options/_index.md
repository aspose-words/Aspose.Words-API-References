---
title: ReportBuilderOptions.Options
linktitle: Options
articleTitle: Options
second_title: .NET için Aspose.Words
description: ReportingEngine'inizin davranışını özelleştirmek, esnek kontrol ve iyileştirilmiş işlevsellik ile rapor oluşturmayı geliştirmek için ReportBuilderOptions özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.lowcode/reportbuilderoptions/options/
---
## ReportBuilderOptions.Options property

Bu davranışın kontrol edildiği bir bayrak kümesini alır veya ayarlar[`ReportingEngine`](../../../aspose.words.reporting/reportingengine/) Bir rapor oluştururken örneği.

```csharp
public ReportBuildOptions Options { get; set; }
```

## Örnekler

Belgenin verilerle nasıl doldurulacağını gösterir.

```csharp
public void BuildReportData()
{
    // Belgeyi verilerle doldurmanın birkaç yolu vardır:
    string doc = MyDir + "Reporting engine template - If greedy.docx";

    AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.1.docx", obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.2.docx", obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.3.docx", SaveFormat.Docx, obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.4.docx", SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}

public class AsposeData
{
    public List<string> List { get; set; }
}
```

### Ayrıca bakınız

* enum [ReportBuildOptions](../../../aspose.words.reporting/reportbuildoptions/)
* class [ReportBuilderOptions](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
