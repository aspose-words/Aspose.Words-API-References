---
title: ReportBuilder Class
linktitle: ReportBuilder
articleTitle: ReportBuilder
second_title: .NET için Aspose.Words
description: Aspose.Words LowCode ReportBuilder ile dinamik raporları zahmetsizce oluşturun. Şablonları verilerle sorunsuz bir şekilde doldurmak için LINQ Reporting Engine'i kullanın.
type: docs
weight: 4360
url: /tr/net/aspose.words.lowcode/reportbuilder/
---
## ReportBuilder class

LINQ Raporlama Motorunu kullanarak şablonu verilerle doldurmayı amaçlayan yöntemler sağlar.

```csharp
public class ReportBuilder : Processor
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create)() | Rapor oluşturucu işlemcisinin yeni bir örneğini oluşturur. |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create_1)(*[ReportBuilderContext](../reportbuildercontext/)*) | Rapor oluşturucu işlemcisinin yeni bir örneğini oluşturur. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | İşlemci eylemini yürüt. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | İşleme için giriş belgesini belirtir. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | İşleme için giriş belgesini belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Çıktı Belge akışları listesini belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Çıktı Belge akışları listesini belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | İşlemci için çıkış akışını belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | İşlemci için çıkış akışını belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | İşlemci için çıktı dosyasını belirtir. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | İşlemci için çıktı dosyasını belirtir. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_12)(*string, string, object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve ek seçeneklerle tamamlanmış bir rapor oluşturur. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve giriş ve çıkış akışlarından belirtilen çıktı biçimi ve ek seçeneklerle tamamlanmış bir rapor oluşturur. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve giriş ve çıkış akışlarından belirtilen çıktı biçimi ve ek seçeneklerle tamamlanmış bir rapor oluşturur. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_13)(*string, string, object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve adlandırılmış bir veri kaynağı referansı ve ek seçenekler içeren tamamlanmış bir rapor oluşturur. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_14)(*string, string, object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini birden fazla kaynaktan gelen verilerle doldurur ve ek seçeneklerle tamamlanmış bir rapor oluşturur. Bu aşırı yükleme, çıktı dosyası uzantısına göre kaydetme biçimini otomatik olarak belirler. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_6)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve belirtilen çıktı biçimi ve ek seçeneklerle tamamlanmış bir rapor oluşturur. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_9)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve belirtilen çıktı biçimi ve ek seçeneklerle tamamlanmış bir rapor oluşturur. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve adlandırılmış bir veri kaynağı referansı ve ek seçenekler içeren tamamlanmış bir rapor oluşturur. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_2)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini birden fazla kaynaktan gelen verilerle doldurur, belirtilen çıktı biçimi ve belirtilen giriş ve çıkış dosya akışlarından ek seçeneklerle tamamlanmış bir rapor oluşturur. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_4)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve adlandırılmış bir veri kaynağı referansı ve ek seçenekler içeren tamamlanmış bir rapor oluşturur. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_5)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini birden fazla kaynaktan gelen verilerle doldurur, belirtilen çıktı biçimi ve belirtilen giriş ve çıkış dosya akışlarından ek seçeneklerle tamamlanmış bir rapor oluşturur. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_7)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve belirtilen çıktı biçimi, adlandırılmış bir veri kaynağı referansı ve ek seçeneklerle tamamlanmış bir rapor oluşturur. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_8)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini birden fazla kaynaktan gelen verilerle doldurur ve belirtilen çıktı biçimi ve ek seçeneklerle tamamlanmış bir rapor oluşturur. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_10)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve belirtilen çıktı biçimi, adlandırılmış bir veri kaynağı referansı ve ek seçeneklerle tamamlanmış bir rapor oluşturur. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_11)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini birden fazla kaynaktan gelen verilerle doldurur ve belirtilen çıktı biçimi ve ek seçeneklerle tamamlanmış bir rapor oluşturur. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini birden fazla kaynaktan gelen verilerle doldurur. Çıktıyı resimlere dönüştürür. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages_1)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Şablon belgesini birden fazla kaynaktan gelen verilerle doldurur. Çıktıyı resimlere dönüştürür. |

### Ayrıca bakınız

* class [Processor](../processor/)
* ad alanı [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../)
