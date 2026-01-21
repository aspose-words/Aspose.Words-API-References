---
title: MailMerger
linktitle: MailMerger
second_title: Aspose.Words for Java
description: Provides methods intended to fill template with data using simple mail merge and mail merge with regions operations in Java.
type: docs
weight: 445
url: /java/com.aspose.words/mailmerger/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class MailMerger extends Processor
```

Provides methods intended to fill template with data using simple mail merge and mail merge with regions operations.
## Methods

| Method | Description |
| --- | --- |
| [create(MailMergerContext context)](#create-com.aspose.words.MailMergerContext) | Creates new instance of the mail merger processor. |
| [execute()](#execute) | Execute the processor action. |
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
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) | Performs mail merge from a DataRow into the document. |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Performs mail merge from a DataRow into the document. |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object) | Performs a mail merge operation for a single record. |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) | Performs a mail merge operation for a single record. |
| [execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow)](#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataRow) | Performs mail merge from a DataRow into the document. |
| [execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Performs mail merge from a DataTable into the document. |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-int-java.lang.String---java.lang.Object) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-int-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-java.lang.String---java.lang.Object) | Performs a mail merge operation for a single record. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow) |  |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) | Performs mail merge from a DataRow into the document and renders the result to images. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Performs mail merge from a DataRow into the document and renders the result to images. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object) | Performs a mail merge operation for a single record and renders the result to images. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) | Performs a mail merge operation for a single record and renders the result to images. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow) |  |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) | Performs mail merge from a DataRow into the document and renders the result to images. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Performs mail merge from a DataRow into the document and renders the result to images. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object) | Performs a mail merge operation for a single record and renders the result to images. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) | Performs a mail merge operation for a single record and renders the result to images. |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataSet dataSet)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) | Performs mail merge from a DataSet into the document with mail merge regions. |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Performs mail merge from a DataTable into the document with mail merge regions. |
| [executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataSet) | Performs mail merge from a DataSet into a document with mail merge regions. |
| [executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Performs mail merge from a DataTable into the document with mail merge regions. |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) | Performs mail merge from a DataSet into the document with mail merge regions and renders the result to images. |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Performs mail merge from a DataTable into the document with mail merge regions and renders the result to images. |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) | Performs mail merge from a DataSet into the document with mail merge regions and renders the result to images. |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Performs mail merge from a DataTable into the document with mail merge regions and renders the result to images. |
| [from(InputStream input)](#from-java.io.InputStream) | Specifies input document for processing. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Specifies input document for processing. |
| [from(String input)](#from-java.lang.String) | Specifies input document for processing. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Specifies input document for processing. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Specifies output file for the processor. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Specifies output file for the processor. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(MailMergerContext context) {#create-com.aspose.words.MailMergerContext}
```
public static MailMerger create(MailMergerContext context)
```


Creates new instance of the mail merger processor.

 **Examples:** 

Shows how to do mail merge operation for a single record using context.

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

Shows how to do mail merge operation from a DataTable using context.

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

Shows how to do mail merge operation from a DataRow using context.

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

Shows how to do mail merge with regions operation from a DataTable using context.

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

Shows how to do mail merge operation for a single record from the stream using context.

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

Shows how to do mail merge operation from a DataTable using documents from the stream using context.

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

Shows how to do mail merge operation from a DataRow using documents from the stream using context.

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

Shows how to do mail merge with regions operation from a DataTable using documents from the stream using context.

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

Shows how to do mail merge with regions operation from a DataSet using context.

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

Shows how to do mail merge with regions operation from a DataSet using documents from the stream using context.

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
| Parameter | Type | Description |
| --- | --- | --- |
| context | [MailMergerContext](../../com.aspose.words/mailmergercontext/) |  |

**Returns:**
[MailMerger](../../com.aspose.words/mailmerger/)
### execute() {#execute}
```
public void execute()
```


Execute the processor action.

 **Examples:** 

Shows how to convert documents with a single line of code using context.

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

Shows how to convert documents from a stream with a single line of code using context.

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

Shows how to merge documents into a single output document using context.

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

Shows how to merge documents from stream into a single output document using context.

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

### execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataRow dataRow) {#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)
```


Performs mail merge from a DataRow into the document.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The output's save options. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Row that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```


Performs mail merge from a DataRow into the document.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The output's save options. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```


Performs a mail merge operation for a single record.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The output's save options. |
| fieldNames | java.lang.String[] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| fieldValues | java.lang.Object[] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```


Performs a mail merge operation for a single record.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The output's save options. |
| fieldNames | java.lang.String[] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| fieldValues | java.lang.Object[] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |

### execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow) {#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow)
```


Performs mail merge from a DataRow into the document.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

 **Examples:** 

Shows how to do mail merge operation from a DataRow.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Row that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

### execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable) {#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable)
```


Performs mail merge from a DataTable into the document.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

 **Examples:** 

Shows how to do mail merge operation from a DataTable.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

### execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow) {#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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


Performs a mail merge operation for a single record.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

 **Examples:** 

Shows how to do mail merge operation for a single record.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| fieldNames | java.lang.String[] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| fieldValues | java.lang.Object[] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |

### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| Parameter | Type | Description |
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


Performs mail merge from a DataRow into the document and renders the result to images.

 **Examples:** 

Shows how to do mail merge operation from a DataRow using documents from the stream and save result to images.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input file stream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The output's save options. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Row that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parameter | Type | Description |
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


Performs mail merge from a DataRow into the document and renders the result to images.

 **Examples:** 

Shows how to do mail merge operation from a DataTable using documents from the stream and save to images.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input file stream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The output's save options. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```


Performs a mail merge operation for a single record and renders the result to images.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input file stream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The output's save options. |
| fieldNames | java.lang.String[] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| fieldValues | java.lang.Object[] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```


Performs a mail merge operation for a single record and renders the result to images.

 **Examples:** 

Shows how to do mail merge operation for a single record from the stream and save result to images.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input file stream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The output's save options. |
| fieldNames | java.lang.String[] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| fieldValues | java.lang.Object[] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| Parameter | Type | Description |
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


Performs mail merge from a DataRow into the document and renders the result to images.

 **Examples:** 

Shows how to do mail merge operation from a DataRow and save result to images.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The output's save options. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Row that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parameter | Type | Description |
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


Performs mail merge from a DataRow into the document and renders the result to images.

 **Examples:** 

Shows how to do mail merge operation from a DataTable and save result to images.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The output's save options. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```


Performs a mail merge operation for a single record and renders the result to images.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The output's save options. |
| fieldNames | java.lang.String[] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| fieldValues | java.lang.Object[] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```


Performs a mail merge operation for a single record and renders the result to images.

 **Examples:** 

Shows how to do mail merge operation for a single record and save result to images.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The output's save options. |
| fieldNames | java.lang.String[] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| fieldValues | java.lang.Object[] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |

**Returns:**
java.io.OutputStream[]
### executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)
```


Performs mail merge from a DataSet into the document with mail merge regions.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The output's save options. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | DataSet that contains data to be inserted into mail merge fields. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```


Performs mail merge from a DataTable into the document with mail merge regions.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The output's save options. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |

### executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet)
```


Performs mail merge from a DataSet into a document with mail merge regions.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

 **Examples:** 

Shows how to do mail merge with regions operation from a DataSet.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | DataSet that contains data to be inserted into mail merge fields. |

### executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable)
```


Performs mail merge from a DataTable into the document with mail merge regions.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

 **Examples:** 

Shows how to do mail merge with regions operation from a DataTable.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Data source for the mail merge operation. The table must have its TableName property set. |

### executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet) {#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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


Performs mail merge from a DataSet into the document with mail merge regions and renders the result to images.

 **Examples:** 

Shows how to do mail merge with regions operation from a DataSet using documents from the stream and save result to images.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input file stream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The output's save options. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | DataSet that contains data to be inserted into mail merge fields. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parameter | Type | Description |
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


Performs mail merge from a DataTable into the document with mail merge regions and renders the result to images.

 **Examples:** 

Shows how to do mail merge with regions operation from a DataTable using documents from the stream and save result to images.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input file stream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The output's save options. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet) {#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet}
```
public static OutputStream[] executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)
```




**Parameters:**
| Parameter | Type | Description |
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


Performs mail merge from a DataSet into the document with mail merge regions and renders the result to images.

 **Examples:** 

Shows how to do mail merge with regions operation from a DataSet and save result to images.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The output's save options. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | DataSet that contains data to be inserted into mail merge fields. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parameter | Type | Description |
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


Performs mail merge from a DataTable into the document with mail merge regions and renders the result to images.

 **Examples:** 

Shows how to do mail merge with regions operation from a DataTable and save result to images.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The output's save options. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |

**Returns:**
java.io.OutputStream[]
### from(InputStream input) {#from-java.io.InputStream}
```
public Processor from(InputStream input)
```


Specifies input document for processing.

 **Remarks:** 

If the processor accepts only one file as an input, only the last specified file will be processed. [Merger](../../com.aspose.words/merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [Converter](../../com.aspose.words/converter/) processor accepts only one file as an input, so only the last specified file will be converted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| input | java.io.InputStream | Input document stream. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Specifies input document for processing.

 **Remarks:** 

If the processor accepts only one file as an input, only the last specified file will be processed. [Merger](../../com.aspose.words/merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [Converter](../../com.aspose.words/converter/) processor accepts only one file as an input, so only the last specified file will be converted.

 **Examples:** 

Shows how to convert documents from a stream with a single line of code using context.

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

Shows how to merge documents from stream into a single output document using context.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| input | java.io.InputStream | Input document stream. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Optional load options used to load the document. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


Specifies input document for processing.

 **Remarks:** 

If the processor accepts only one file as an input, only the last specified file will be processed. [Merger](../../com.aspose.words/merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [Converter](../../com.aspose.words/converter/) processor accepts only one file as an input, so only the last specified file will be converted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| input | java.lang.String | Input document file name. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Specifies input document for processing.

 **Remarks:** 

If the processor accepts only one file as an input, only the last specified file will be processed. [Merger](../../com.aspose.words/merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [Converter](../../com.aspose.words/converter/) processor accepts only one file as an input, so only the last specified file will be converted.

 **Examples:** 

Shows how to convert documents with a single line of code using context.

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

Shows how to merge documents into a single output document using context.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| input | java.lang.String | Input document file name. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Optional load options used to load the document. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


Specifies output file for the processor.

 **Remarks:** 

If the output consists of multiple files, the specified output file name is used to generate the file name for each part following the rule: 'outputFile\_partIndex.extension'.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.lang.String | Output file name. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Specifies output file for the processor.

 **Remarks:** 

If the output consists of multiple files, the specified output file name is used to generate the file name for each part following the rule: 'outputFile\_partIndex.extension'.

 **Examples:** 

Shows how to convert documents with a single line of code using context.

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

Shows how to merge documents into a single output document using context.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.lang.String | Output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Optional save options. If not specified, save format is determined by the file extension. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
