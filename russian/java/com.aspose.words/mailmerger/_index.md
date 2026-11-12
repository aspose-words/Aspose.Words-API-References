---
title: "MailMerger"
linktitle: "MailMerger"
second_title: "Aspose.Words для Java"
description: "Предоставляет методы, предназначенные для заполнения шаблона данными с использованием простого слияния почты и операций слияния почты с регионами в Java."
type: docs
weight: 446
url: /ru/java/com.aspose.words/mailmerger/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class MailMerger extends Processor
```

Предоставляет методы, предназначенные для заполнения шаблона данными с использованием простого слияния почты и операций слияния почты с регионами.
## Методы

| Метод | Описание |
| --- | --- |
| [create(MailMergerContext context)](#create-com.aspose.words.MailMergerContext) | Создаёт новый экземпляр процессора слияния почты. |
| [execute()](#execute) | Выполнить действие процессора. |
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
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) | Выполняет слияние почты из DataRow в документ. |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Выполняет слияние почты из DataRow в документ. |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object) | Выполняет операцию слияния почты для одной записи. |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) | Выполняет операцию слияния почты для одной записи. |
| [execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow)](#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataRow) | Выполняет слияние почты из DataRow в документ. |
| [execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Выполняет слияние почты из DataTable в документ. |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-int-java.lang.String---java.lang.Object) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-int-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-java.lang.String---java.lang.Object) | Выполняет операцию слияния почты для одной записи. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow) |  |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) | Выполняет слияние почты из DataRow в документ и рендерит результат в изображения. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Выполняет слияние почты из DataRow в документ и рендерит результат в изображения. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object) | Выполняет операцию слияния почты для одной записи и рендерит результат в изображения. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) | Выполняет операцию слияния почты для одной записи и рендерит результат в изображения. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow) |  |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) | Выполняет слияние почты из DataRow в документ и рендерит результат в изображения. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Выполняет слияние почты из DataRow в документ и рендерит результат в изображения. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object) | Выполняет операцию слияния почты для одной записи и рендерит результат в изображения. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) | Выполняет операцию слияния почты для одной записи и рендерит результат в изображения. |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataSet dataSet)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) | Выполняет слияние почты из DataSet в документ с регионами слияния почты. |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Выполняет слияние почты из DataTable в документ с регионами слияния почты. |
| [executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataSet) | Выполняет слияние почты из DataSet в документ с регионами слияния почты. |
| [executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Выполняет слияние почты из DataTable в документ с регионами слияния почты. |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) | Выполняет слияние почты из DataSet в документ с регионами слияния почты и рендерит результат в изображения. |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Выполняет слияние почты из DataTable в документ с регионами слияния почты и рендерит результат в изображения. |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) | Выполняет слияние почты из DataSet в документ с регионами слияния почты и рендерит результат в изображения. |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Выполняет слияние почты из DataTable в документ с регионами слияния почты и рендерит результат в изображения. |
| [from(InputStream input)](#from-java.io.InputStream) | Указывает входной документ для обработки. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Указывает входной документ для обработки. |
| [from(String input)](#from-java.lang.String) | Указывает входной документ для обработки. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Указывает входной документ для обработки. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Указывает выходной файл для процессора. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Указывает выходной файл для процессора. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(MailMergerContext context) {#create-com.aspose.words.MailMergerContext}
```
public static MailMerger create(MailMergerContext context)
```


Создаёт новый экземпляр процессора слияния почты.

 **Examples:** 

Показывает, как выполнить операцию слияния почты для одной записи, используя контекст.

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

Показывает, как выполнить операцию слияния почты для одной записи из потока, используя контекст.

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

Показывает, как выполнить операцию слияния почты из DataRow, используя контекст.

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

Показывает, как выполнить операцию слияния почты из DataRow, используя документы из потока, используя контекст.

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

Показывает, как выполнить операцию слияния почты из DataTable, используя контекст.

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

Показывает, как выполнить операцию слияния почты из DataTable, используя документы из потока, с применением контекста.

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

Показывает, как выполнить операцию слияния почты с регионами из DataTable, используя контекст.

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

Показывает, как выполнить операцию слияния почты с регионами из DataTable, используя документы из потока, с применением контекста.

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

Показывает, как выполнить операцию слияния почты с регионами из DataSet, используя контекст.

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

Показывает, как выполнить операцию слияния почты с регионами из DataSet, используя документы из потока, с применением контекста.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| context | [MailMergerContext](../../com.aspose.words/mailmergercontext/) |  |

**Returns:**
[MailMerger](../../com.aspose.words/mailmerger/)
### execute() {#execute}
```
public void execute()
```


Выполнить действие процессора.

 **Examples:** 

Показывает, как объединить документы в один результирующий документ, используя контекст.

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

Показывает, как объединить документы из потока в один результирующий документ, используя контекст.

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

Показывает, как конвертировать документы одной строкой кода, используя контекст.

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

Показывает, как конвертировать документы из потока одной строкой кода, используя контекст.

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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)
```


Выполняет слияние почты из DataRow в документ.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения вывода. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Строка, содержащая данные для вставки в поля слияния почты. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Параметры слияния почты. |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```


Выполняет слияние почты из DataRow в документ.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения вывода. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Таблица, содержащая данные для вставки в поля слияния почты. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Параметры слияния почты. |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```


Выполняет операцию слияния почты для одной записи.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения вывода. |
| fieldNames | java.lang.String[] | Массив имён полей слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| fieldValues | java.lang.Object[] | Массив значений для вставки в поля слияния. Количество элементов в этом массиве должно совпадать с количеством элементов в fieldNames. |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```


Выполняет операцию слияния почты для одной записи.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения вывода. |
| fieldNames | java.lang.String[] | Массив имён полей слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| fieldValues | java.lang.Object[] | Массив значений для вставки в поля слияния. Количество элементов в этом массиве должно совпадать с количеством элементов в fieldNames. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Параметры слияния почты. |

### execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow) {#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow)
```


Выполняет слияние почты из DataRow в документ.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

 **Examples:** 

Показывает, как выполнить операцию слияния писем из DataRow.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Строка, содержащая данные для вставки в поля слияния почты. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |

### execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable) {#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable)
```


Выполняет слияние почты из DataTable в документ.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

 **Examples:** 

Показывает, как выполнить операцию слияния писем из DataTable.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Таблица, содержащая данные для вставки в поля слияния почты. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |

### execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow) {#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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


Выполняет операцию слияния почты для одной записи.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

 **Examples:** 

Показывает, как выполнить операцию слияния писем для одной записи.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| fieldNames | java.lang.String[] | Массив имён полей слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| fieldValues | java.lang.Object[] | Массив значений для вставки в поля слияния. Количество элементов в этом массиве должно совпадать с количеством элементов в fieldNames. |

### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| Параметр | Тип | Описание |
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


Выполняет слияние почты из DataRow в документ и рендерит результат в изображения.

 **Examples:** 

Показывает, как выполнить операцию слияния писем из DataRow, используя документы из потока, и сохранить результат в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения вывода. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Строка, содержащая данные для вставки в поля слияния почты. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Параметры слияния почты. |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Параметр | Тип | Описание |
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


Выполняет слияние почты из DataRow в документ и рендерит результат в изображения.

 **Examples:** 

Показывает, как выполнить операцию слияния писем из DataTable, используя документы из потока, и сохранить в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения вывода. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Таблица, содержащая данные для вставки в поля слияния почты. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Параметры слияния почты. |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```


Выполняет операцию слияния почты для одной записи и рендерит результат в изображения.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения вывода. |
| fieldNames | java.lang.String[] | Массив имён полей слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| fieldValues | java.lang.Object[] | Массив значений для вставки в поля слияния. Количество элементов в этом массиве должно совпадать с количеством элементов в fieldNames. |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```


Выполняет операцию слияния почты для одной записи и рендерит результат в изображения.

 **Examples:** 

Показывает, как выполнить операцию слияния писем для одной записи из потока и сохранить результат в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения вывода. |
| fieldNames | java.lang.String[] | Массив имён полей слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| fieldValues | java.lang.Object[] | Массив значений для вставки в поля слияния. Количество элементов в этом массиве должно совпадать с количеством элементов в fieldNames. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Параметры слияния почты. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| Параметр | Тип | Описание |
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


Выполняет слияние почты из DataRow в документ и рендерит результат в изображения.

 **Examples:** 

Показывает, как выполнить операцию слияния писем из DataRow и сохранить результат в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения вывода. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Строка, содержащая данные для вставки в поля слияния почты. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Параметры слияния почты. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Параметр | Тип | Описание |
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


Выполняет слияние почты из DataRow в документ и рендерит результат в изображения.

 **Examples:** 

Показывает, как выполнить операцию слияния писем из DataTable и сохранить результат в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения вывода. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Таблица, содержащая данные для вставки в поля слияния почты. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Параметры слияния почты. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```


Выполняет операцию слияния почты для одной записи и рендерит результат в изображения.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения вывода. |
| fieldNames | java.lang.String[] | Массив имён полей слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| fieldValues | java.lang.Object[] | Массив значений для вставки в поля слияния. Количество элементов в этом массиве должно совпадать с количеством элементов в fieldNames. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```


Выполняет операцию слияния почты для одной записи и рендерит результат в изображения.

 **Examples:** 

Показывает, как выполнить операцию слияния писем для одной записи и сохранить результат в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения вывода. |
| fieldNames | java.lang.String[] | Массив имён полей слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| fieldValues | java.lang.Object[] | Массив значений для вставки в поля слияния. Количество элементов в этом массиве должно совпадать с количеством элементов в fieldNames. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Параметры слияния почты. |

**Returns:**
java.io.OutputStream[]
### executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)
```


Выполняет слияние почты из DataSet в документ с регионами слияния почты.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения вывода. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | DataSet, содержащий данные для вставки в поля слияния писем. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Параметры слияния почты. |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```


Выполняет слияние почты из DataTable в документ с регионами слияния почты.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения вывода. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Таблица, содержащая данные для вставки в поля слияния почты. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Параметры слияния почты. |

### executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet)
```


Выполняет слияние почты из DataSet в документ с регионами слияния почты.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

 **Examples:** 

Показывает, как выполнить операцию слияния писем с регионами из DataSet.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | DataSet, содержащий данные для вставки в поля слияния писем. |

### executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable)
```


Выполняет слияние почты из DataTable в документ с регионами слияния почты.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

 **Examples:** 

Показывает, как выполнить операцию слияния писем с регионами из DataTable.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Источник данных для операции слияния писем. Таблица должна иметь установленное свойство TableName. |

### executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet) {#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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


Выполняет слияние почты из DataSet в документ с регионами слияния почты и рендерит результат в изображения.

 **Examples:** 

Показывает, как выполнить операцию слияния писем с регионами из DataSet, используя документы из потока, и сохранить результат в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения вывода. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | DataSet, содержащий данные для вставки в поля слияния писем. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Параметры слияния почты. |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Параметр | Тип | Описание |
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


Выполняет слияние почты из DataTable в документ с регионами слияния почты и рендерит результат в изображения.

 **Examples:** 

Показывает, как выполнить операцию слияния писем с регионами из DataTable, используя документы из потока, и сохранить результат в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения вывода. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Таблица, содержащая данные для вставки в поля слияния почты. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Параметры слияния почты. |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet) {#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet}
```
public static OutputStream[] executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)
```




**Parameters:**
| Параметр | Тип | Описание |
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


Выполняет слияние почты из DataSet в документ с регионами слияния почты и рендерит результат в изображения.

 **Examples:** 

Показывает, как выполнить операцию слияния писем с регионами из DataSet и сохранить результат в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения вывода. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | DataSet, содержащий данные для вставки в поля слияния писем. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Параметры слияния почты. |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Параметр | Тип | Описание |
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


Выполняет слияние почты из DataTable в документ с регионами слияния почты и рендерит результат в изображения.

 **Examples:** 

Показывает, как выполнить операцию слияния писем с регионами из DataTable и сохранить результат в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения вывода. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Таблица, содержащая данные для вставки в поля слияния почты. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Параметры слияния почты. |

**Returns:**
java.io.OutputStream[]
### from(InputStream input) {#from-java.io.InputStream}
```
public Processor from(InputStream input)
```


Указывает входной документ для обработки.

 **Remarks:** 

Если процессор принимает в качестве входа только один файл, будет обработан только последний указанный файл. Процессор [Merger](../../com.aspose.words/merger/) принимает несколько файлов в качестве входа, в результате все указанные документы будут объединены. Процессор [Converter](../../com.aspose.words/converter/) принимает в качестве входа только один файл, поэтому будет преобразован только последний указанный файл.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ввод | java.io.InputStream | Поток входного документа. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Указывает входной документ для обработки.

 **Remarks:** 

Если процессор принимает в качестве входа только один файл, будет обработан только последний указанный файл. Процессор [Merger](../../com.aspose.words/merger/) принимает несколько файлов в качестве входа, в результате все указанные документы будут объединены. Процессор [Converter](../../com.aspose.words/converter/) принимает в качестве входа только один файл, поэтому будет преобразован только последний указанный файл.

 **Examples:** 

Показывает, как объединить документы из потока в один результирующий документ, используя контекст.

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

Показывает, как конвертировать документы из потока одной строкой кода, используя контекст.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| ввод | java.io.InputStream | Поток входного документа. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Необязательные параметры загрузки, используемые для загрузки документа. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


Указывает входной документ для обработки.

 **Remarks:** 

Если процессор принимает в качестве входа только один файл, будет обработан только последний указанный файл. Процессор [Merger](../../com.aspose.words/merger/) принимает несколько файлов в качестве входа, в результате все указанные документы будут объединены. Процессор [Converter](../../com.aspose.words/converter/) принимает в качестве входа только один файл, поэтому будет преобразован только последний указанный файл.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ввод | java.lang.String | Имя файла входного документа. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Указывает входной документ для обработки.

 **Remarks:** 

Если процессор принимает в качестве входа только один файл, будет обработан только последний указанный файл. Процессор [Merger](../../com.aspose.words/merger/) принимает несколько файлов в качестве входа, в результате все указанные документы будут объединены. Процессор [Converter](../../com.aspose.words/converter/) принимает в качестве входа только один файл, поэтому будет преобразован только последний указанный файл.

 **Examples:** 

Показывает, как объединить документы в один результирующий документ, используя контекст.

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

Показывает, как конвертировать документы одной строкой кода, используя контекст.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| ввод | java.lang.String | Имя файла входного документа. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Необязательные параметры загрузки, используемые для загрузки документа. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


Указывает выходной файл для процессора.

 **Remarks:** 

Если вывод состоит из нескольких файлов, указанное имя выходного файла используется для генерации имени файла каждой части по правилу: 'outputFile\_partIndex.extension'.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.lang.String | Имя выходного файла. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Указывает выходной файл для процессора.

 **Remarks:** 

Если вывод состоит из нескольких файлов, указанное имя выходного файла используется для генерации имени файла каждой части по правилу: 'outputFile\_partIndex.extension'.

 **Examples:** 

Показывает, как объединить документы в один результирующий документ, используя контекст.

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

Показывает, как конвертировать документы одной строкой кода, используя контекст.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Необязательные параметры сохранения. Если не указано, формат сохраняемого файла определяется расширением. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
