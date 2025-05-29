---
title: ReportingEngine.Options
linktitle: Options
articleTitle: Options
second_title: .NET için Aspose.Words
description: En iyi performans ve kontrol için esnek bayraklarla rapor oluşturma davranışlarını kolayca özelleştirmek amacıyla ReportingEngine Seçenekleri özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.reporting/reportingengine/options/
---
## ReportingEngine.Options property

Bu davranışın kontrol edildiği bir bayrak kümesini alır veya ayarlar[`ReportingEngine`](../) Bir rapor oluştururken örneği.

```csharp
public ReportBuildOptions Options { get; set; }
```

## Örnekler

Eksik üyelere nasıl izin verileceğini gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

### Ayrıca bakınız

* enum [ReportBuildOptions](../../reportbuildoptions/)
* class [ReportingEngine](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)
