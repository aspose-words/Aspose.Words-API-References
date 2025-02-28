---
title: XmlDataSource
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words for .NET
description: Create a powerful data source effortlessly with the XmlDataSource constructor, loading XML data using optimized default options for seamless integration.
type: docs
weight: 10
url: /net/aspose.words.reporting/xmldatasource/xmldatasource/
---
## XmlDataSource(*string*) {#constructor_4}

Creates a new data source with data from an XML file using default options for XML data loading.

```csharp
public XmlDataSource(string xmlPath)
```

| Parameter | Type | Description |
| --- | --- | --- |
| xmlPath | String | The path to the XML file to be used as the data source. |

## Examples

Show how to use XML as a data source (string).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

### See Also

* class [XmlDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)

---

## XmlDataSource(*Stream*) {#constructor}

Creates a new data source with data from an XML stream using default options for XML data loading.

```csharp
public XmlDataSource(Stream xmlStream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| xmlStream | Stream | The stream of XML data to be used as the data source. |

## Examples

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

* class [XmlDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)

---

## XmlDataSource(*string, string*) {#constructor_6}

Creates a new data source with data from an XML file using an XML Schema Definition file. Default options are used for XML data loading.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath)
```

| Parameter | Type | Description |
| --- | --- | --- |
| xmlPath | String | The path to the XML file to be used as the data source. |
| xmlSchemaPath | String | The path to the XML Schema Definition file that provides schema for the XML file. |

### See Also

* class [XmlDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream*) {#constructor_2}

Creates a new data source with data from an XML stream using an XML Schema Definition stream. Default options are used for XML data loading.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| xmlStream | Stream | The stream of XML data to be used as the data source. |
| xmlSchemaStream | Stream | The stream of XML Schema Definition that provides schema for the XML data. |

### See Also

* class [XmlDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)

---

## XmlDataSource(*string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_5}

Creates a new data source with data from an XML file using the specified options for XML data loading.

```csharp
public XmlDataSource(string xmlPath, XmlDataLoadOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| xmlPath | String | The path to the XML file to be used as the data source. |
| options | XmlDataLoadOptions | Options for XML data loading. |

### See Also

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_1}

Creates a new data source with data from an XML stream using the specified options for XML data loading.

```csharp
public XmlDataSource(Stream xmlStream, XmlDataLoadOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| xmlStream | Stream | The stream of XML data to be used as the data source. |
| options | XmlDataLoadOptions | Options for XML data loading. |

### See Also

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)

---

## XmlDataSource(*string, string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_7}

Creates a new data source with data from an XML file using an XML Schema Definition file. The specified options are used for XML data loading.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath, XmlDataLoadOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| xmlPath | String | The path to the XML file to be used as the data source. |
| xmlSchemaPath | String | The path to the XML Schema Definition file that provides schema for the XML file. |
| options | XmlDataLoadOptions | Options for XML data loading. |

### See Also

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_3}

Creates a new data source with data from an XML stream using an XML Schema Definition stream. The specified options are used for XML data loading.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream, XmlDataLoadOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| xmlStream | Stream | The stream of XML data to be used as the data source. |
| xmlSchemaStream | Stream | The stream of XML Schema Definition that provides schema for the XML data. |
| options | XmlDataLoadOptions | Options for XML data loading. |

### See Also

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)
