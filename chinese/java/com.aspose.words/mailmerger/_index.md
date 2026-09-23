---
title: "MailMerger"
linktitle: "MailMerger"
second_title: "Aspose.Words for Java"
description: "提供用于使用简单邮件合并和带区域的邮件合并操作在 Java 中填充模板数据的方法。"
type: docs
weight: 446
url: /zh/java/com.aspose.words/mailmerger/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class MailMerger extends Processor
```

提供用于使用简单邮件合并和带区域的邮件合并操作填充模板数据的方法。
## 方法

| 方法 | 描述 |
| --- | --- |
| [create(MailMergerContext context)](#create-com.aspose.words.MailMergerContext) | 创建邮件合并处理器的新实例。 |
| [execute()](#execute) | 执行处理器操作。 |
| [execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataRow dataRow)](#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow) |  |
| [execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) |  |
| [execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable)](#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object) |  |
| [execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) |  |
| [execute(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataRow dataRow)](#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataRow) |  |
| [execute(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) |  |
| [execute(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable)](#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [execute(InputStream inputStream, OutputStream outputStream, int saveFormat, String[] fieldNames, Object[] fieldValues)](#execute-java.io.InputStream-java.io.OutputStream-int-java.lang.String---java.lang.Object) |  |
| [execute(InputStream inputStream, OutputStream outputStream, int saveFormat, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#execute-java.io.InputStream-java.io.OutputStream-int-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow) |  |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) | 从 DataRow 执行邮件合并到文档中。 |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | 从 DataRow 执行邮件合并到文档中。 |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object) | 对单条记录执行邮件合并操作。 |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) | 对单条记录执行邮件合并操作。 |
| [execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow)](#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataRow) | 从 DataRow 执行邮件合并到文档中。 |
| [execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable) | 从 DataTable 执行邮件合并到文档中。 |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-int-java.lang.String---java.lang.Object) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-int-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-java.lang.String---java.lang.Object) | 对单条记录执行邮件合并操作。 |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow) |  |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) | 从 DataRow 执行邮件合并到文档中并将结果渲染为图像。 |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | 从 DataRow 执行邮件合并到文档中并将结果渲染为图像。 |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object) | 对单条记录执行邮件合并操作并将结果渲染为图像。 |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) | 对单条记录执行邮件合并操作并将结果渲染为图像。 |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow) |  |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) | 从 DataRow 执行邮件合并到文档中并将结果渲染为图像。 |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | 从 DataRow 执行邮件合并到文档中并将结果渲染为图像。 |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object) | 对单条记录执行邮件合并操作并将结果渲染为图像。 |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) | 对单条记录执行邮件合并操作并将结果渲染为图像。 |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataSet dataSet)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) | 从 DataSet 执行带区域的邮件合并到文档中。 |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | 从 DataTable 执行带区域的邮件合并到文档中。 |
| [executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataSet) | 从 DataSet 执行带区域的邮件合并到文档中。 |
| [executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable) | 从 DataTable 执行带区域的邮件合并到文档中。 |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) | 从 DataSet 执行带区域的邮件合并到文档中并将结果渲染为图像。 |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | 从 DataTable 执行带区域的邮件合并到文档中并将结果渲染为图像。 |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) | 从 DataSet 执行带区域的邮件合并到文档中并将结果渲染为图像。 |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | 从 DataTable 执行带区域的邮件合并到文档中并将结果渲染为图像。 |
| [from(InputStream input)](#from-java.io.InputStream) | 指定用于处理的输入文档。 |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | 指定用于处理的输入文档。 |
| [from(String input)](#from-java.lang.String) | 指定用于处理的输入文档。 |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | 指定用于处理的输入文档。 |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | 指定处理器的输出文件。 |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | 指定处理器的输出文件。 |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(MailMergerContext context) {#create-com.aspose.words.MailMergerContext}
```
public static MailMerger create(MailMergerContext context)
```


创建邮件合并处理器的新实例。

 **Examples:** 

展示如何使用上下文对单条记录执行邮件合并操作。

```

 // There is a several ways to do mail merge operation:
 String doc = getMyDir() + "Mail merge.doc";

 String[] fieldNames = new String[]{"FirstName", "Location", "SpecialCharsInName()"};
 String[] fieldValues = new String[]{"James Bond", "London", "Classified"};

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setSimpleDataSource(fieldNames, fieldValues);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContext.docx")
         .execute();
 
```

展示如何使用上下文从流中对单条记录执行邮件合并操作。

```

 // There is a several ways to do mail merge operation using documents from the stream:
 String[] fieldNames = new String[]{"FirstName", "Location", "SpecialCharsInName()"};
 String[] fieldValues = new String[]{"James Bond", "London", "Classified"};

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setSimpleDataSource(fieldNames, fieldValues);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStream.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

展示如何使用上下文从 DataRow 执行邮件合并操作。

```

 // There is a several ways to do mail merge operation from a DataRow:
 String doc = getMyDir() + "Mail merge.doc";

 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});
 DataRow dataRow = dataTable.getRows().get(0);

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setSimpleDataSource(dataRow);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContextDataRow.docx")
         .execute();
 
```

展示如何使用上下文从流中的文档使用 DataRow 执行邮件合并操作。

```

 // There is a several ways to do mail merge operation from a DataRow using documents from the stream:
 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});
 DataRow dataRow = dataTable.getRows().get(0);

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setSimpleDataSource(dataRow);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStreamDataRow.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

展示如何使用上下文从 DataTable 执行邮件合并操作。

```

 // There is a several ways to do mail merge operation from a DataTable:
 String doc = getMyDir() + "Mail merge.doc";

 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setSimpleDataSource(dataTable);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContextDataTable.docx")
         .execute();
 
```

展示如何在上下文中使用来自流的文档从 DataTable 执行邮件合并操作。

```

 // There is a several ways to do mail merge operation from a DataTable using documents from the stream:
 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setSimpleDataSource(dataTable);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStreamDataTable.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

展示如何在上下文中从 DataTable 执行带区域的邮件合并操作。

```

 // There is a several ways to do mail merge with regions operation from a DataTable:
 String doc = getMyDir() + "Mail merge with regions.docx";

 DataTable dataTable = new DataTable("MyTable");
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("LastName");
 dataTable.getRows().add(new Object[]{"John", "Doe"});
 dataTable.getRows().add(new Object[]{"", ""});
 dataTable.getRows().add(new Object[]{"Jane", "Doe"});

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setRegionsDataSource(dataTable);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContextWithRegionsDataTable.docx")
         .execute();
 
```

展示如何在上下文中使用来自流的文档从 DataTable 执行带区域的邮件合并操作。

```

 // There is a several ways to do mail merge with regions operation from a DataTable using documents from the stream:
 DataTable dataTable = new DataTable("MyTable");
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("LastName");
 dataTable.getRows().add(new Object[]{"John", "Doe"});
 dataTable.getRows().add(new Object[]{"", ""});
 dataTable.getRows().add(new Object[]{"Jane", "Doe"});

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setRegionsDataSource(dataTable);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStreamWithRegionsDataTable.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

展示如何在上下文中从 DataSet 执行带区域的邮件合并操作。

```

 // There is a several ways to do mail merge with regions operation from a DataSet:
 String doc = getMyDir() + "Mail merge with regions data set.docx";

 DataTable tableCustomers = new DataTable("Customers");
 tableCustomers.getColumns().add("CustomerID");
 tableCustomers.getColumns().add("CustomerName");
 tableCustomers.getRows().add(new Object[]{1, "John Doe"});
 tableCustomers.getRows().add(new Object[]{2, "Jane Doe"});

 DataTable tableOrders = new DataTable("Orders");
 tableOrders.getColumns().add("CustomerID");
 tableOrders.getColumns().add("ItemName");
 tableOrders.getColumns().add("Quantity");
 tableOrders.getRows().add(new Object[]{1, "Hawaiian", 2});
 tableOrders.getRows().add(new Object[]{2, "Pepperoni", 1});
 tableOrders.getRows().add(new Object[]{2, "Chicago", 1});

 DataSet dataSet = new DataSet();
 dataSet.getTables().add(tableCustomers);
 dataSet.getTables().add(tableOrders);
 dataSet.getRelations().add(tableCustomers.getColumns().get("CustomerID"), tableOrders.getColumns().get("CustomerID"));

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setRegionsDataSource(dataSet);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContextWithRegionsDataTable.docx")
         .execute();
 
```

展示如何在上下文中使用来自流的文档从 DataSet 执行带区域的邮件合并操作。

```

 // There is a several ways to do mail merge with regions operation from a DataSet using documents from the stream:
 DataTable tableCustomers = new DataTable("Customers");
 tableCustomers.getColumns().add("CustomerID");
 tableCustomers.getColumns().add("CustomerName");
 tableCustomers.getRows().add(new Object[]{1, "John Doe"});
 tableCustomers.getRows().add(new Object[]{2, "Jane Doe"});

 DataTable tableOrders = new DataTable("Orders");
 tableOrders.getColumns().add("CustomerID");
 tableOrders.getColumns().add("ItemName");
 tableOrders.getColumns().add("Quantity");
 tableOrders.getRows().add(new Object[]{1, "Hawaiian", 2});
 tableOrders.getRows().add(new Object[]{2, "Pepperoni", 1});
 tableOrders.getRows().add(new Object[]{2, "Chicago", 1});

 DataSet dataSet = new DataSet();
 dataSet.getTables().add(tableCustomers);
 dataSet.getTables().add(tableOrders);
 dataSet.getRelations().add(tableCustomers.getColumns().get("CustomerID"), tableOrders.getColumns().get("CustomerID"));

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setRegionsDataSource(dataSet);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStreamWithRegionsDataSet.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| context | [MailMergerContext](../../com.aspose.words/mailmergercontext/) |  |

**Returns:**
[MailMerger](../../com.aspose.words/mailmerger/)
### execute() {#execute}
```
public void execute()
```


执行处理器操作。

 **Examples:** 

展示如何在上下文中将文档合并为单个输出文档。

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

展示如何在上下文中将来自流的文档合并为单个输出文档。

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 try (FileInputStream firstStreamIn = new FileInputStream(inputDoc1)) {
     try (FileInputStream secondStreamIn = new FileInputStream(inputDoc2)) {
         OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
         {
             saveOptions.setPassword("Aspose.Words");
         }
         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.1.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, saveOptions)
                     .execute();
         }

         LoadOptions firstLoadOptions = new LoadOptions();
         {
             firstLoadOptions.setIgnoreOleData(true);
         }
         LoadOptions secondLoadOptions = new LoadOptions();
         {
             secondLoadOptions.setIgnoreOleData(false);
         }
         try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.2.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn, firstLoadOptions)
                     .from(secondStreamIn, secondLoadOptions)
                     .to(streamOut1, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

展示如何在上下文中使用一行代码转换文档。

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

展示如何在上下文中使用一行代码将来自流的文档转换。

```

 String doc = getMyDir() + "Document.docx";
 ConverterContext converterContext = new ConverterContext();

 try (FileInputStream streamIn = new FileInputStream(doc)) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.1.docx")) {
         Converter.create(converterContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.RTF)
                 .execute();
     }

     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
     {
         saveOptions.setPassword("Aspose.Words");
     }
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(true);
     }
     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.2.docx")) {
         Converter.create(converterContext)
                 .from(streamIn, loadOptions)
                 .to(streamOut1, saveOptions)
                 .execute();
     }
 }
 
```

### execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataRow dataRow) {#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions) {#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions}
```
public static void execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |

### execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable) {#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |

### execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object}
```
public static void execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| fieldNames | java.lang.String[] |  |
| fieldValues | java.lang.Object[] |  |

### execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static void execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| fieldNames | java.lang.String[] |  |
| fieldValues | java.lang.Object[] |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |

### execute(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataRow dataRow) {#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataRow dataRow)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### execute(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions) {#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions}
```
public static void execute(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |

### execute(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable) {#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### execute(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void execute(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |

### execute(InputStream inputStream, OutputStream outputStream, int saveFormat, String[] fieldNames, Object[] fieldValues) {#execute-java.io.InputStream-java.io.OutputStream-int-java.lang.String---java.lang.Object}
```
public static void execute(InputStream inputStream, OutputStream outputStream, int saveFormat, String[] fieldNames, Object[] fieldValues)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| fieldNames | java.lang.String[] |  |
| fieldValues | java.lang.Object[] |  |

### execute(InputStream inputStream, OutputStream outputStream, int saveFormat, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#execute-java.io.InputStream-java.io.OutputStream-int-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static void execute(InputStream inputStream, OutputStream outputStream, int saveFormat, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| fieldNames | java.lang.String[] |  |
| fieldValues | java.lang.Object[] |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)
```


从 DataRow 执行邮件合并到文档中。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 输出的保存选项。 |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | 包含要插入邮件合并字段的数据的行。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | 邮件合并选项。 |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```


从 DataRow 执行邮件合并到文档中。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 输出的保存选项。 |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | 包含要插入邮件合并字段的数据的表。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | 邮件合并选项。 |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```


对单条记录执行邮件合并操作。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 输出的保存选项。 |
| fieldNames | java.lang.String[] | 合并字段名的数组。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| fieldValues | java.lang.Object[] | 要插入合并字段的值数组。此数组中的元素数量必须与 fieldNames 中的元素数量相同。 |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```


对单条记录执行邮件合并操作。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 输出的保存选项。 |
| fieldNames | java.lang.String[] | 合并字段名的数组。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| fieldValues | java.lang.Object[] | 要插入合并字段的值数组。此数组中的元素数量必须与 fieldNames 中的元素数量相同。 |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | 邮件合并选项。 |

### execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow) {#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow)
```


从 DataRow 执行邮件合并到文档中。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

 **Examples:** 

展示如何从 DataRow 执行邮件合并操作。

```

 // There is a several ways to do mail merge operation from a DataRow:
 String doc = getMyDir() + "Mail merge.doc";

 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});
 DataRow dataRow = dataTable.getRows().get(0);

 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMergeDataRow.1.docx", dataRow);
 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMergeDataRow.2.docx", SaveFormat.DOCX, dataRow);
 MailMergeOptions options = new MailMergeOptions();
 options.setTrimWhitespaces(true);
 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMergeDataRow.3.docx", SaveFormat.DOCX, dataRow, options);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | 包含要插入邮件合并字段的数据的行。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |

### execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable) {#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable)
```


从 DataTable 执行邮件合并到文档中。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

 **Examples:** 

展示如何从 DataTable 执行邮件合并操作。

```

 // There is a several ways to do mail merge operation from a DataTable:
 String doc = getMyDir() + "Mail merge.doc";

 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});

 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMergeDataTable.1.docx", dataTable);
 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMergeDataTable.2.docx", SaveFormat.DOCX, dataTable);
 MailMergeOptions options = new MailMergeOptions();
 options.setTrimWhitespaces(true);
 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMergeDataTable.3.docx", SaveFormat.DOCX, dataTable, options);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | 包含要插入邮件合并字段的数据的表。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |

### execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow) {#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |

### execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable) {#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |

### execute(String inputFileName, String outputFileName, int saveFormat, String[] fieldNames, Object[] fieldValues) {#execute-java.lang.String-java.lang.String-int-java.lang.String---java.lang.Object}
```
public static void execute(String inputFileName, String outputFileName, int saveFormat, String[] fieldNames, Object[] fieldValues)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| fieldNames | java.lang.String[] |  |
| fieldValues | java.lang.Object[] |  |

### execute(String inputFileName, String outputFileName, int saveFormat, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-int-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, int saveFormat, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| fieldNames | java.lang.String[] |  |
| fieldValues | java.lang.Object[] |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |

### execute(String inputFileName, String outputFileName, String[] fieldNames, Object[] fieldValues) {#execute-java.lang.String-java.lang.String-java.lang.String---java.lang.Object}
```
public static void execute(String inputFileName, String outputFileName, String[] fieldNames, Object[] fieldValues)
```


对单条记录执行邮件合并操作。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

 **Examples:** 

展示如何对单个记录执行邮件合并操作。

```

 // There is a several ways to do mail merge operation:
 String doc = getMyDir() + "Mail merge.doc";

 String[] fieldNames = new String[]{"FirstName", "Location", "SpecialCharsInName()"};
 String[] fieldValues = new String[]{"James Bond", "London", "Classified"};

 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMerge.2.docx", SaveFormat.DOCX, fieldNames, fieldValues);
 MailMergeOptions options = new MailMergeOptions();
 options.setTrimWhitespaces(true);
 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMerge.3.docx", SaveFormat.DOCX, fieldNames, fieldValues, options);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| fieldNames | java.lang.String[] | 合并字段名的数组。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| fieldValues | java.lang.Object[] | 要插入合并字段的值数组。此数组中的元素数量必须与 fieldNames 中的元素数量相同。 |

### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)
```


从 DataRow 执行邮件合并到文档中并将结果渲染为图像。

 **Examples:** 

展示如何从 DataRow 使用流中的文档执行邮件合并操作并将结果保存为图像。

```

 // There is a several ways to do mail merge operation from a DataRow using documents from the stream:
 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});
 DataRow dataRow = dataTable.getRows().get(0);

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     OutputStream[] images = MailMerger.executeToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), dataRow);
     MailMergeOptions options = new MailMergeOptions();
     options.setTrimWhitespaces(true);
     images = MailMerger.executeToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), dataRow, options);
 }
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入文件流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | 包含要插入邮件合并字段的数据的行。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | 邮件合并选项。 |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```


从 DataRow 执行邮件合并到文档中并将结果渲染为图像。

 **Examples:** 

展示如何从 DataTable 使用流中的文档执行邮件合并操作并保存为图像。

```

 // There is a several ways to do mail merge operation from a DataTable using documents from the stream and save result to images:
 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     OutputStream[] images = MailMerger.executeToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), dataTable);
     MailMergeOptions options = new MailMergeOptions();
     options.setTrimWhitespaces(true);
     images = MailMerger.executeToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), dataTable, options);
 }
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入文件流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | 包含要插入邮件合并字段的数据的表。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | 邮件合并选项。 |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```


对单条记录执行邮件合并操作并将结果渲染为图像。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入文件流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| fieldNames | java.lang.String[] | 合并字段名的数组。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| fieldValues | java.lang.Object[] | 要插入合并字段的值数组。此数组中的元素数量必须与 fieldNames 中的元素数量相同。 |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```


对单条记录执行邮件合并操作并将结果渲染为图像。

 **Examples:** 

展示如何从流中对单个记录执行邮件合并操作并将结果保存为图像。

```

 // There is a several ways to do mail merge operation using documents from the stream:
 String[] fieldNames = new String[]{"FirstName", "Location", "SpecialCharsInName()"};
 String[] fieldValues = new String[]{"James Bond", "London", "Classified"};

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     OutputStream[] images = MailMerger.executeToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), fieldNames, fieldValues);

     MailMergeOptions mailMergeOptions = new MailMergeOptions();
     mailMergeOptions.setTrimWhitespaces(true);
     images = MailMerger.executeToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), fieldNames, fieldValues, mailMergeOptions);
 }
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入文件流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| fieldNames | java.lang.String[] | 合并字段名的数组。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| fieldValues | java.lang.Object[] | 要插入合并字段的值数组。此数组中的元素数量必须与 fieldNames 中的元素数量相同。 |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | 邮件合并选项。 |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)
```


从 DataRow 执行邮件合并到文档中并将结果渲染为图像。

 **Examples:** 

展示如何从 DataRow 执行邮件合并操作并将结果保存为图像。

```

 // There is a several ways to do mail merge operation from a DataRow:
 String doc = getMyDir() + "Mail merge.doc";

 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});
 DataRow dataRow = dataTable.getRows().get(0);

 OutputStream[] images = MailMerger.executeToImages(doc, new ImageSaveOptions(SaveFormat.PNG), dataRow);
 MailMergeOptions options = new MailMergeOptions();
 options.setTrimWhitespaces(true);
 images = MailMerger.executeToImages(doc, new ImageSaveOptions(SaveFormat.PNG), dataRow, options);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | 包含要插入邮件合并字段的数据的行。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | 邮件合并选项。 |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```


从 DataRow 执行邮件合并到文档中并将结果渲染为图像。

 **Examples:** 

展示如何从 DataTable 执行邮件合并操作并将结果保存为图像。

```

 // There is a several ways to do mail merge operation from a DataTable:
 String doc = getMyDir() + "Mail merge.doc";

 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});

 OutputStream[] images = MailMerger.executeToImages(doc, new ImageSaveOptions(SaveFormat.PNG), dataTable);
 MailMergeOptions options = new MailMergeOptions();
 options.setTrimWhitespaces(true);
 images = MailMerger.executeToImages(doc, new ImageSaveOptions(SaveFormat.PNG), dataTable, options);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | 包含要插入邮件合并字段的数据的表。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | 邮件合并选项。 |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```


对单条记录执行邮件合并操作并将结果渲染为图像。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| fieldNames | java.lang.String[] | 合并字段名的数组。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| fieldValues | java.lang.Object[] | 要插入合并字段的值数组。此数组中的元素数量必须与 fieldNames 中的元素数量相同。 |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```


对单条记录执行邮件合并操作并将结果渲染为图像。

 **Examples:** 

展示如何对单个记录执行邮件合并操作并将结果保存为图像。

```

 // There is a several ways to do mail merge operation:
 String doc = getMyDir() + "Mail merge.doc";

 String[] fieldNames = new String[]{"FirstName", "Location", "SpecialCharsInName()"};
 String[] fieldValues = new String[]{"James Bond", "London", "Classified"};

 OutputStream[] images = MailMerger.executeToImages(doc, new ImageSaveOptions(SaveFormat.PNG), fieldNames, fieldValues);
 MailMergeOptions mailMergeOptions = new MailMergeOptions();
 mailMergeOptions.setTrimWhitespaces(true);
 images = MailMerger.executeToImages(doc, new ImageSaveOptions(SaveFormat.PNG), fieldNames, fieldValues, mailMergeOptions);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| fieldNames | java.lang.String[] | 合并字段名的数组。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| fieldValues | java.lang.Object[] | 要插入合并字段的值数组。此数组中的元素数量必须与 fieldNames 中的元素数量相同。 |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | 邮件合并选项。 |

**Returns:**
java.io.OutputStream[]
### executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |

### executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |

### executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |

### executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataSet dataSet) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataSet dataSet)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |

### executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |

### executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)
```


从 DataSet 执行带区域的邮件合并到文档中。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 输出的保存选项。 |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | 包含要插入合并字段数据的 DataSet。 |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | 邮件合并选项。 |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```


从 DataTable 执行带区域的邮件合并到文档中。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 输出的保存选项。 |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | 包含要插入邮件合并字段的数据的表。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | 邮件合并选项。 |

### executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet)
```


从 DataSet 执行带区域的邮件合并到文档中。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

 **Examples:** 

展示如何从 DataSet 执行带区域的邮件合并操作。

```

 // There is a several ways to do mail merge with regions operation from a DataSet:
 String doc = getMyDir() + "Mail merge with regions data set.docx";

 DataTable tableCustomers = new DataTable("Customers");
 tableCustomers.getColumns().add("CustomerID");
 tableCustomers.getColumns().add("CustomerName");
 tableCustomers.getRows().add(new Object[]{1, "John Doe"});
 tableCustomers.getRows().add(new Object[]{2, "Jane Doe"});

 DataTable tableOrders = new DataTable("Orders");
 tableOrders.getColumns().add("CustomerID");
 tableOrders.getColumns().add("ItemName");
 tableOrders.getColumns().add("Quantity");
 tableOrders.getRows().add(new Object[]{1, "Hawaiian", 2});
 tableOrders.getRows().add(new Object[]{2, "Pepperoni", 1});
 tableOrders.getRows().add(new Object[]{2, "Chicago", 1});

 DataSet dataSet = new DataSet();
 dataSet.getTables().add(tableCustomers);
 dataSet.getTables().add(tableOrders);
 dataSet.getRelations().add(tableCustomers.getColumns().get("CustomerID"), tableOrders.getColumns().get("CustomerID"));

 MailMerger.executeWithRegions(doc, getArtifactsDir() + "LowCode.MailMergeWithRegionsDataSet.1.docx", dataSet);
 MailMerger.executeWithRegions(doc, getArtifactsDir() + "LowCode.MailMergeWithRegionsDataSet.2.docx", SaveFormat.DOCX, dataSet);
 MailMergeOptions options = new MailMergeOptions();
 options.setTrimWhitespaces(true);
 MailMerger.executeWithRegions(doc, getArtifactsDir() + "LowCode.MailMergeWithRegionsDataSet.3.docx", SaveFormat.DOCX, dataSet, options);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | 包含要插入合并字段数据的 DataSet。 |

### executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable)
```


从 DataTable 执行带区域的邮件合并到文档中。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

 **Examples:** 

展示如何从 DataTable 执行带区域的邮件合并操作。

```

 // There is a several ways to do mail merge with regions operation from a DataTable:
 String doc = getMyDir() + "Mail merge with regions.docx";

 DataTable dataTable = new DataTable("MyTable");
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("LastName");
 dataTable.getRows().add(new Object[]{"John", "Doe"});
 dataTable.getRows().add(new Object[]{"", ""});
 dataTable.getRows().add(new Object[]{"Jane", "Doe"});

 MailMerger.executeWithRegions(doc, getArtifactsDir() + "LowCode.MailMergeWithRegionsDataTable.1.docx", dataTable);
 MailMerger.executeWithRegions(doc, getArtifactsDir() + "LowCode.MailMergeWithRegionsDataTable.2.docx", SaveFormat.DOCX, dataTable);
 MailMergeOptions options = new MailMergeOptions();
 options.setTrimWhitespaces(true);
 MailMerger.executeWithRegions(doc, getArtifactsDir() + "LowCode.MailMergeWithRegionsDataTable.3.docx", SaveFormat.DOCX, dataTable, options);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | 邮件合并操作的数据源。该表必须设置 TableName 属性。 |

### executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet) {#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |

### executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |

### executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable) {#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |

### executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataSet dataSet) {#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet}
```
public static OutputStream[] executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions) {#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)
```


从 DataSet 执行带区域的邮件合并到文档中并将结果渲染为图像。

 **Examples:** 

展示如何从 DataSet 使用流中的文档执行带区域的邮件合并操作并将结果保存为图像。

```

 // There is a several ways to do mail merge with regions operation from a DataSet using documents from the stream:
 DataTable tableCustomers = new DataTable("Customers");
 tableCustomers.getColumns().add("CustomerID");
 tableCustomers.getColumns().add("CustomerName");
 tableCustomers.getRows().add(new Object[]{1, "John Doe"});
 tableCustomers.getRows().add(new Object[]{2, "Jane Doe"});

 DataTable tableOrders = new DataTable("Orders");
 tableOrders.getColumns().add("CustomerID");
 tableOrders.getColumns().add("ItemName");
 tableOrders.getColumns().add("Quantity");
 tableOrders.getRows().add(new Object[]{1, "Hawaiian", 2});
 tableOrders.getRows().add(new Object[]{2, "Pepperoni", 1});
 tableOrders.getRows().add(new Object[]{2, "Chicago", 1});

 DataSet dataSet = new DataSet();
 dataSet.getTables().add(tableCustomers);
 dataSet.getTables().add(tableOrders);
 dataSet.getRelations().add(tableCustomers.getColumns().get("CustomerID"), tableOrders.getColumns().get("CustomerID"));

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     OutputStream[] images = MailMerger.executeWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), dataSet);
     MailMergeOptions options = new MailMergeOptions();
     options.setTrimWhitespaces(true);
     images = MailMerger.executeWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), dataSet, options);
 }
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入文件流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | 包含要插入合并字段数据的 DataSet。 |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | 邮件合并选项。 |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```


从 DataTable 执行带区域的邮件合并到文档中并将结果渲染为图像。

 **Examples:** 

展示如何从 DataTable 使用流中的文档执行带区域的邮件合并操作并将结果保存为图像。

```

 // There is a several ways to do mail merge with regions operation from a DataTable using documents from the stream:
 DataTable dataTable = new DataTable("MyTable");
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("LastName");
 dataTable.getRows().add(new Object[]{"John", "Doe"});
 dataTable.getRows().add(new Object[]{"", ""});
 dataTable.getRows().add(new Object[]{"Jane", "Doe"});

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     OutputStream[] images = MailMerger.executeWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), dataTable);
     MailMergeOptions options = new MailMergeOptions();
     options.setTrimWhitespaces(true);
     images = MailMerger.executeWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), dataTable, options);
 }
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入文件流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | 包含要插入邮件合并字段的数据的表。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | 邮件合并选项。 |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet) {#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet}
```
public static OutputStream[] executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions) {#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)
```


从 DataSet 执行带区域的邮件合并到文档中并将结果渲染为图像。

 **Examples:** 

展示如何从 DataSet 执行带区域的邮件合并操作并将结果保存为图像。

```

 // There is a several ways to do mail merge with regions operation from a DataSet:
 String doc = getMyDir() + "Mail merge with regions data set.docx";

 DataTable tableCustomers = new DataTable("Customers");
 tableCustomers.getColumns().add("CustomerID");
 tableCustomers.getColumns().add("CustomerName");
 tableCustomers.getRows().add(new Object[]{1, "John Doe"});
 tableCustomers.getRows().add(new Object[]{2, "Jane Doe"});

 DataTable tableOrders = new DataTable("Orders");
 tableOrders.getColumns().add("CustomerID");
 tableOrders.getColumns().add("ItemName");
 tableOrders.getColumns().add("Quantity");
 tableOrders.getRows().add(new Object[]{1, "Hawaiian", 2});
 tableOrders.getRows().add(new Object[]{2, "Pepperoni", 1});
 tableOrders.getRows().add(new Object[]{2, "Chicago", 1});

 DataSet dataSet = new DataSet();
 dataSet.getTables().add(tableCustomers);
 dataSet.getTables().add(tableOrders);
 dataSet.getRelations().add(tableCustomers.getColumns().get("CustomerID"), tableOrders.getColumns().get("CustomerID"));

 OutputStream[] images = MailMerger.executeWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.PNG), dataSet);
 MailMergeOptions options = new MailMergeOptions();
 options.setTrimWhitespaces(true);
 images = MailMerger.executeWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.PNG), dataSet, options);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | 包含要插入合并字段数据的 DataSet。 |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | 邮件合并选项。 |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```


从 DataTable 执行带区域的邮件合并到文档中并将结果渲染为图像。

 **Examples:** 

展示如何从 DataTable 执行带区域的邮件合并操作并将结果保存为图像。

```

 // There is a several ways to do mail merge with regions operation from a DataTable:
 String doc = getMyDir() + "Mail merge with regions.docx";

 DataTable dataTable = new DataTable("MyTable");
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("LastName");
 dataTable.getRows().add(new Object[]{"John", "Doe"});
 dataTable.getRows().add(new Object[]{"", ""});
 dataTable.getRows().add(new Object[]{"Jane", "Doe"});

 OutputStream[] images = MailMerger.executeWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.PNG), dataTable);
 MailMergeOptions options = new MailMergeOptions();
 options.setTrimWhitespaces(true);
 images = MailMerger.executeWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.PNG), dataTable, options);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | 包含要插入邮件合并字段的数据的表。字段名不区分大小写。如果遇到文档中未找到的字段名，将被忽略。 |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | 邮件合并选项。 |

**Returns:**
java.io.OutputStream[]
### from(InputStream input) {#from-java.io.InputStream}
```
public Processor from(InputStream input)
```


指定用于处理的输入文档。

 **Remarks:** 

如果处理器仅接受单个文件作为输入，则只会处理最后指定的文件。 [Merger](../../com.aspose.words/merger/) 处理器接受多个文件作为输入，结果是所有指定的文档将被合并。 [Converter](../../com.aspose.words/converter/) 处理器仅接受单个文件作为输入，因此只会转换最后指定的文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输入 | java.io.InputStream | 输入文档流。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


指定用于处理的输入文档。

 **Remarks:** 

如果处理器仅接受单个文件作为输入，则只会处理最后指定的文件。 [Merger](../../com.aspose.words/merger/) 处理器接受多个文件作为输入，结果是所有指定的文档将被合并。 [Converter](../../com.aspose.words/converter/) 处理器仅接受单个文件作为输入，因此只会转换最后指定的文件。

 **Examples:** 

展示如何在上下文中将来自流的文档合并为单个输出文档。

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 try (FileInputStream firstStreamIn = new FileInputStream(inputDoc1)) {
     try (FileInputStream secondStreamIn = new FileInputStream(inputDoc2)) {
         OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
         {
             saveOptions.setPassword("Aspose.Words");
         }
         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.1.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, saveOptions)
                     .execute();
         }

         LoadOptions firstLoadOptions = new LoadOptions();
         {
             firstLoadOptions.setIgnoreOleData(true);
         }
         LoadOptions secondLoadOptions = new LoadOptions();
         {
             secondLoadOptions.setIgnoreOleData(false);
         }
         try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.2.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn, firstLoadOptions)
                     .from(secondStreamIn, secondLoadOptions)
                     .to(streamOut1, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

展示如何在上下文中使用一行代码将来自流的文档转换。

```

 String doc = getMyDir() + "Document.docx";
 ConverterContext converterContext = new ConverterContext();

 try (FileInputStream streamIn = new FileInputStream(doc)) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.1.docx")) {
         Converter.create(converterContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.RTF)
                 .execute();
     }

     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
     {
         saveOptions.setPassword("Aspose.Words");
     }
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(true);
     }
     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.2.docx")) {
         Converter.create(converterContext)
                 .from(streamIn, loadOptions)
                 .to(streamOut1, saveOptions)
                 .execute();
     }
 }
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输入 | java.io.InputStream | 输入文档流。 |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | 用于加载文档的可选加载选项。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


指定用于处理的输入文档。

 **Remarks:** 

如果处理器仅接受单个文件作为输入，则只会处理最后指定的文件。 [Merger](../../com.aspose.words/merger/) 处理器接受多个文件作为输入，结果是所有指定的文档将被合并。 [Converter](../../com.aspose.words/converter/) 处理器仅接受单个文件作为输入，因此只会转换最后指定的文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输入 | java.lang.String | 输入文档文件名。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


指定用于处理的输入文档。

 **Remarks:** 

如果处理器仅接受单个文件作为输入，则只会处理最后指定的文件。 [Merger](../../com.aspose.words/merger/) 处理器接受多个文件作为输入，结果是所有指定的文档将被合并。 [Converter](../../com.aspose.words/converter/) 处理器仅接受单个文件作为输入，因此只会转换最后指定的文件。

 **Examples:** 

展示如何在上下文中将文档合并为单个输出文档。

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

展示如何在上下文中使用一行代码转换文档。

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输入 | java.lang.String | 输入文档文件名。 |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | 用于加载文档的可选加载选项。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


指定处理器的输出文件。

 **Remarks:** 

如果输出包含多个文件，则使用指定的输出文件名按照规则 'outputFile\\_partIndex.extension' 为每个部分生成文件名。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.lang.String | 输出文件名。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


指定处理器的输出文件。

 **Remarks:** 

如果输出包含多个文件，则使用指定的输出文件名按照规则 'outputFile\\_partIndex.extension' 为每个部分生成文件名。

 **Examples:** 

展示如何在上下文中将文档合并为单个输出文档。

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

展示如何在上下文中使用一行代码转换文档。

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 可选的保存选项。如果未指定，保存格式将由文件扩展名决定。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
