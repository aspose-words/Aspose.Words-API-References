---
title: ReportingEngine Class
linktitle: ReportingEngine
articleTitle: ReportingEngine
second_title: Aspose.Words for .NET
description: Unlock powerful document automation with Aspose.Words.ReportingEngine. Easily populate templates with data and customize settings for seamless reporting.
type: docs
weight: 5470
url: /net/aspose.words.reporting/reportingengine/
---
## ReportingEngine class

Provides routines to populate template documents with data and a set of settings to control these routines.

To learn more, visit the [LINQ Reporting Engine](https://docs.aspose.com/words/net/linq-reporting-engine/) documentation article.

```csharp
public class ReportingEngine
```

## Constructors

| Name | Description |
| --- | --- |
| [ReportingEngine](reportingengine/)() | Initializes a new instance of this class. |

## Properties

| Name | Description |
| --- | --- |
| [KnownTypes](../../aspose.words.reporting/reportingengine/knowntypes/) { get; } | Gets an unordered set (i.e. a collection of unique items) containing Type objects which fully or partially qualified names can be used within report templates processed by this engine instance to invoke the corresponding types' static members, perform type casts, etc. |
| [MissingMemberMessage](../../aspose.words.reporting/reportingengine/missingmembermessage/) { get; set; } | Gets or sets a string value printed instead of a template expression that represents a plain reference to a missing member of an object. The default value is an empty string. |
| [Options](../../aspose.words.reporting/reportingengine/options/) { get; set; } | Gets or sets a set of flags controlling behavior of this `ReportingEngine` instance while building a report. |
| static [UseReflectionOptimization](../../aspose.words.reporting/reportingengine/usereflectionoptimization/) { get; set; } | Gets or sets a value indicating whether invocations of custom type members performed via reflection API are optimized using dynamic class generation or not. The default value is `true`. |

## Methods

| Name | Description |
| --- | --- |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport)(*[Document](../../aspose.words/document/), object*) | Populates the specified template document with data from the specified source making it a ready report. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_1)(*[Document](../../aspose.words/document/), object, string*) | Populates the specified template document with data from the specified source making it a ready report. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_2)(*[Document](../../aspose.words/document/), object[], string[]*) | Populates the specified template document with data from the specified sources making it a ready report. |
| static [GetRestrictedTypes](../../aspose.words.reporting/reportingengine/getrestrictedtypes/)() | Returns types, which members as well as which derived types' members should be inaccessible by the engine through template syntax. |
| static [SetRestrictedTypes](../../aspose.words.reporting/reportingengine/setrestrictedtypes/)(*params Type[]*) | Specifies types, which members as well as which derived types' members should be inaccessible by the engine through template syntax. |

### See Also

* namespace [Aspose.Words.Reporting](../../aspose.words.reporting/)
* assembly [Aspose.Words](../../)
