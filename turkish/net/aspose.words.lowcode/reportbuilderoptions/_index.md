---
title: ReportBuilderOptions Class
linktitle: ReportBuilderOptions
articleTitle: ReportBuilderOptions
second_title: .NET için Aspose.Words
description: Kusursuz belge oluşturma için özelleştirilebilir seçeneklerle LINQ Raporlama Motoru deneyiminizi geliştirmek üzere tasarlanmış Aspose.Words LowCode ReportBuilderOptions sınıfını keşfedin.
type: docs
weight: 4380
url: /tr/net/aspose.words.lowcode/reportbuilderoptions/
---
## ReportBuilderOptions class

LINQ Raporlama Motoru işlevselliği için seçenekleri temsil eder.

```csharp
public class ReportBuilderOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ReportBuilderOptions](reportbuilderoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [KnownTypes](../../aspose.words.lowcode/reportbuilderoptions/knowntypes/) { get; } | Aşağıdakileri içeren sıralanmamış bir küme (yani benzersiz öğelerden oluşan bir koleksiyon) alır:Type Bu engine örneği tarafından işlenen rapor şablonları içerisinde ilgili türlerin statik üyelerini çağırmak, tür dönüştürmeleri gerçekleştirmek vb. için tam veya kısmen nitelikli adları kullanılabilen nesneler |
| [MissingMemberMessage](../../aspose.words.lowcode/reportbuilderoptions/missingmembermessage/) { get; set; } | Bir nesnenin eksik bir üyesine düz bir referansı temsil eden bir şablon ifadesi yerine yazdırılan bir dize değerini alır veya ayarlar. Varsayılan değer boş bir dizedir. |
| [Options](../../aspose.words.lowcode/reportbuilderoptions/options/) { get; set; } | Bu davranışın kontrol edildiği bir bayrak kümesini alır veya ayarlar[`ReportingEngine`](../../aspose.words.reporting/reportingengine/) Bir rapor oluştururken örneği. |

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

* ad alanı [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../)
