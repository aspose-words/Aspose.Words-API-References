---
title: XmlDataSource Class
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words for .NET
description: Aspose.Words.Reporting.XmlDataSource class. Provides access to data of an XML file or stream to be used within a report in C#.
type: docs
weight: 5350
url: /net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

Provides access to data of an XML file or stream to be used within a report.

To learn more, visit the [LINQ Reporting Engine](https://docs.aspose.com/words/net/linq-reporting-engine/) documentation article.

```csharp
public class XmlDataSource
```

## Constructors

| Name | Description |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(*Stream*) | Creates a new data source with data from an XML stream using default options for XML data loading. |
| [XmlDataSource](xmldatasource/#constructor_4)(*string*) | Creates a new data source with data from an XML file using default options for XML data loading. |
| [XmlDataSource](xmldatasource/#constructor_2)(*Stream, Stream*) | Creates a new data source with data from an XML stream using an XML Schema Definition stream. Default options are used for XML data loading. |
| [XmlDataSource](xmldatasource/#constructor_1)(*Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Creates a new data source with data from an XML stream using the specified options for XML data loading. |
| [XmlDataSource](xmldatasource/#constructor_6)(*string, string*) | Creates a new data source with data from an XML file using an XML Schema Definition file. Default options are used for XML data loading. |
| [XmlDataSource](xmldatasource/#constructor_5)(*string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Creates a new data source with data from an XML file using the specified options for XML data loading. |
| [XmlDataSource](xmldatasource/#constructor_3)(*Stream, Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Creates a new data source with data from an XML stream using an XML Schema Definition stream. The specified options are used for XML data loading. |
| [XmlDataSource](xmldatasource/#constructor_7)(*string, string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Creates a new data source with data from an XML file using an XML Schema Definition file. The specified options are used for XML data loading. |

## Remarks

To access data of the corresponding file or stream while generating a report, pass an instance of this class as a data source to one of [`ReportingEngine`](../reportingengine/).BuildReport overloads.

In template documents, if a top-level XML element contains only a list of elements of the same type, an `XmlDataSource` instance should be treated in the same way as if it was a DataTable instance. Otherwise, an `XmlDataSource` instance should be treated in the same way as if it was a DataRow instance. For more information, see template syntax reference (https://docs.aspose.com/display/wordsnet/Template+Syntax).

When XML Schema Definition is passed to a constructor of this class, data types of values of simple XML elements and attributes are determined according to the schema. So in template documents, you can work with typed values rather than just strings.

When XML Schema Definition is not passed to a constructor of this class, data types of values of simple XML elements and attributes are determined automatically upon their string representations. So in template documents, you can work with typed values in this case as well. The engine is capable to automatically recognize values of the following types:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Note that for automatic recognition of data types to work, string representations of values of simple XML elements and attributes should be formed using invariant culture settings.

To override default behavior of XML data loading, initialize and pass a [`XmlDataLoadOptions`](../xmldataloadoptions/) instance to a constructor of this class.

## Examples

Show how to use XML as a data source (string).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

Show how to use XML as a data source (stream).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### See Also

* namespace [Aspose.Words.Reporting](../../aspose.words.reporting/)
* assembly [Aspose.Words](../../)
