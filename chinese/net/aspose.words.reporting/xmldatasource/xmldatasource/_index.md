---
title: XmlDataSource
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words for .NET
description: 使用 XmlDataSource 构造函数轻松创建强大的数据源，使用优化的默认选项加载 XML 数据以实现无缝集成。
type: docs
weight: 10
url: /zh/net/aspose.words.reporting/xmldatasource/xmldatasource/
---
## XmlDataSource(*string*) {#constructor_4}

使用 XML 数据加载的默认选项，从 XML 文件创建新的数据源。

```csharp
public XmlDataSource(string xmlPath)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlPath | String | 用作数据源的 XML 文件的路径。 |

## 例子

展示如何使用 XML 作为数据源（字符串）。

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

### 也可以看看

* class [XmlDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## XmlDataSource(*Stream*) {#constructor}

使用 XML 数据加载的默认选项，通过 XML 流中的数据创建新的数据源。

```csharp
public XmlDataSource(Stream xmlStream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlStream | Stream | 用作数据源的 XML 数据流。 |

## 例子

展示如何使用 XML 作为数据源（流）。

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### 也可以看看

* class [XmlDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## XmlDataSource(*string, string*) {#constructor_6}

使用 XML Schema Definition 文件创建一个包含 XML 文件中数据的新数据源。默认选项 用于加载 XML 数据。

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlPath | String | 用作数据源的 XML 文件的路径。 |
| xmlSchemaPath | String | 为 XML 文件提供架构的 XML 架构定义文件的路径。 |

### 也可以看看

* class [XmlDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream*) {#constructor_2}

使用 XML Schema Definition 流创建一个包含 XML 流数据的新数据源。默认选项 用于加载 XML 数据。

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlStream | Stream | 用作数据源的 XML 数据流。 |
| xmlSchemaStream | Stream | XML 模式定义流为 XML 数据提供模式。 |

### 也可以看看

* class [XmlDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## XmlDataSource(*string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_5}

使用指定的 XML 数据加载选项，从 XML 文件创建新的数据源。

```csharp
public XmlDataSource(string xmlPath, XmlDataLoadOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlPath | String | 用作数据源的 XML 文件的路径。 |
| options | XmlDataLoadOptions | XML 数据加载选项。 |

### 也可以看看

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_1}

使用指定的 XML 数据加载选项，从 XML 流中创建新的数据源。

```csharp
public XmlDataSource(Stream xmlStream, XmlDataLoadOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlStream | Stream | 用作数据源的 XML 数据流。 |
| options | XmlDataLoadOptions | XML 数据加载选项。 |

### 也可以看看

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## XmlDataSource(*string, string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_7}

使用 XML 架构定义文件，使用 XML 文件中的数据创建新的数据源。指定的 选项用于加载 XML 数据。

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath, XmlDataLoadOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlPath | String | 用作数据源的 XML 文件的路径。 |
| xmlSchemaPath | String | 为 XML 文件提供架构的 XML 架构定义文件的路径。 |
| options | XmlDataLoadOptions | XML 数据加载选项。 |

### 也可以看看

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_3}

使用 XML Schema Definition 流创建一个包含 XML 流数据的新数据源。指定的 选项用于加载 XML 数据。

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream, XmlDataLoadOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlStream | Stream | 用作数据源的 XML 数据流。 |
| xmlSchemaStream | Stream | XML 模式定义流为 XML 数据提供模式。 |
| options | XmlDataLoadOptions | XML 数据加载选项。 |

### 也可以看看

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)
