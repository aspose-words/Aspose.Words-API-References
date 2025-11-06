---
title: ReportBuilder Class
linktitle: ReportBuilder
articleTitle: ReportBuilder
second_title: Aspose.Words for .NET
description: Effortlessly create dynamic reports with Aspose.Words LowCode ReportBuilder. Utilize LINQ Reporting Engine to fill templates with data seamlessly.
type: docs
weight: 4390
url: /net/aspose.words.lowcode/reportbuilder/
---
## ReportBuilder class

Provides methods intended to fill template with data using LINQ Reporting Engine.

```csharp
public class ReportBuilder : Processor
```

## Methods

| Name | Description |
| --- | --- |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create)() | Creates new instance of the report builder processor. |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create_1)(*[ReportBuilderContext](../reportbuildercontext/)*) | Creates new instance of the report builder processor. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Execute the processor action. |
| [Execute](../../aspose.words.lowcode/processor/execute/)(*CancellationToken*) | Execute the processor action allowing canceling document processing task using specified cancellation token. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream*) | Specifies input document for processing. |
| [From](../../aspose.words.lowcode/processor/from/)(*string*) | Specifies input document for processing. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifies input document for processing. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifies input document for processing. |
| [To](../../aspose.words.lowcode/processor/to/)(*string*) | Specifies output file for the processor. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Specifies output Document streams list. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifies output Document streams list. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Specifies output stream for the processor. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifies output stream for the processor. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Specifies output file for the processor. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifies output file for the processor. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_24)(*string, string, object*) | Populates the template document with data from the specified source, generating a completed report with additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object*) | Populates the template document with data from the specified source, generating a completed report with specified output format and additional options, from input and output streams. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_6)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object*) | Populates the template document with data from the specified source, generating a completed report with specified output format and additional options, from input and output streams. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_25)(*string, string, object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from the specified source, generating a completed report with additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_26)(*string, string, object, string*) | Populates the template document with data from the specified source, generating a completed report with a named data source reference and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_28)(*string, string, object[], string[]*) | Populates the template document with data from multiple sources, generating a completed report with additional options. This overload automatically determines the save format based on the output file extension. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_12)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object*) | Populates the template document with data from the specified source, generating a completed report with specified output format and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_18)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object*) | Populates the template document with data from the specified source, generating a completed report with specified output format and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from the specified source, generating a completed report with specified output format and additional options, from input and output streams. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_2)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, string*) | Populates the template document with data from the specified source, generating a completed report with a named data source reference and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_4)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object[], string[]*) | Populates the template document with data from multiple sources, generating a completed report with specified output format and additional options from the specified input and output file streams. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_7)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from the specified source, generating a completed report with specified output format and additional options, from input and output streams. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_8)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string*) | Populates the template document with data from the specified source, generating a completed report with a named data source reference and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_10)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[]*) | Populates the template document with data from multiple sources, generating a completed report with specified output format and additional options from the specified input and output file streams. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_27)(*string, string, object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from the specified source, generating a completed report with a named data source reference and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_29)(*string, string, object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from multiple sources, generating a completed report with additional options. This overload automatically determines the save format based on the output file extension. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_13)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from the specified source, generating a completed report with specified output format and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_14)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, string*) | Populates the template document with data from the specified source, generating a completed report with specified output format, a named data source reference, and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_16)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object[], string[]*) | Populates the template document with data from multiple sources, generating a completed report with a specified output format and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_19)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from the specified source, generating a completed report with specified output format and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_20)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string*) | Populates the template document with data from the specified source, generating a completed report with specified output format, a named data source reference, and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_22)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[]*) | Populates the template document with data from multiple sources, generating a completed report with a specified output format and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_3)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from the specified source, generating a completed report with a named data source reference and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_5)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from multiple sources, generating a completed report with specified output format and additional options from the specified input and output file streams. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_9)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from the specified source, generating a completed report with a named data source reference and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_11)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from multiple sources, generating a completed report with specified output format and additional options from the specified input and output file streams. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_15)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from the specified source, generating a completed report with specified output format, a named data source reference, and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_17)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from multiple sources, generating a completed report with a specified output format and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_21)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from the specified source, generating a completed report with specified output format, a named data source reference, and additional options. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_23)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from multiple sources, generating a completed report with a specified output format and additional options. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[]*) | Populates the template document with data from multiple sources. Renders the output to images. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages_2)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[]*) | Populates the template document with data from multiple sources. Renders the output to images. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages_1)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from multiple sources. Renders the output to images. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages_3)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Populates the template document with data from multiple sources. Renders the output to images. |

### See Also

* class [Processor](../processor/)
* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
