---
title: "MailMerger"
linktitle: "MailMerger"
second_title: "Aspose.Words Java için"
description: "Java'da basit posta birleştirme ve bölge tabanlı posta birleştirme işlemlerini kullanarak şablonu veriyle doldurmak için tasarlanmış yöntemler sağlar."
type: docs
weight: 446
url: /tr/java/com.aspose.words/mailmerger/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class MailMerger extends Processor
```

Basit posta birleştirme ve bölge tabanlı posta birleştirme işlemlerini kullanarak şablonu veriyle doldurmayı amaçlayan yöntemler sağlar.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [create(MailMergerContext context)](#create-com.aspose.words.MailMergerContext) | Posta birleştirici işlemcisinin yeni bir örneğini oluşturur. |
| [execute()](#execute) | İşlemci eylemini çalıştır. |
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
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) | Bir DataRow'dan belgeye posta birleştirme gerçekleştirir. |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Bir DataRow'dan belgeye posta birleştirme gerçekleştirir. |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object) | Tek bir kayıt için posta birleştirme işlemi gerçekleştirir. |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) | Tek bir kayıt için posta birleştirme işlemi gerçekleştirir. |
| [execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow)](#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataRow) | Bir DataRow'dan belgeye posta birleştirme gerçekleştirir. |
| [execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Bir DataTable'dan belgeye posta birleştirme gerçekleştirir. |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-int-java.lang.String---java.lang.Object) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-int-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-java.lang.String---java.lang.Object) | Tek bir kayıt için posta birleştirme işlemi gerçekleştirir. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow) |  |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) | Bir DataRow'dan belgeye posta birleştirme gerçekleştirir ve sonucu görüntülere render eder. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Bir DataRow'dan belgeye posta birleştirme gerçekleştirir ve sonucu görüntülere render eder. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object) | Tek bir kayıt için posta birleştirme işlemi gerçekleştirir ve sonucu görüntülere render eder. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) | Tek bir kayıt için posta birleştirme işlemi gerçekleştirir ve sonucu görüntülere render eder. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow) |  |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) | Bir DataRow'dan belgeye posta birleştirme gerçekleştirir ve sonucu görüntülere render eder. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Bir DataRow'dan belgeye posta birleştirme gerçekleştirir ve sonucu görüntülere render eder. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object) | Tek bir kayıt için posta birleştirme işlemi gerçekleştirir ve sonucu görüntülere render eder. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) | Tek bir kayıt için posta birleştirme işlemi gerçekleştirir ve sonucu görüntülere render eder. |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataSet dataSet)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) | Bir DataSet'ten belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir. |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Bir DataTable'dan belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir. |
| [executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataSet) | Bir DataSet'ten belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir. |
| [executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Bir DataTable'dan belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir. |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) | Bir DataSet'ten belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir ve sonucu görüntülere render eder. |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Bir DataTable'dan belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir ve sonucu görüntülere render eder. |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) | Bir DataSet'ten belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir ve sonucu görüntülere render eder. |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Bir DataTable'dan belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir ve sonucu görüntülere render eder. |
| [from(InputStream input)](#from-java.io.InputStream) | İşleme için giriş belgesini belirtir. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | İşleme için giriş belgesini belirtir. |
| [from(String input)](#from-java.lang.String) | İşleme için giriş belgesini belirtir. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | İşleme için giriş belgesini belirtir. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | İşlemci için çıktı dosyasını belirtir. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | İşlemci için çıktı dosyasını belirtir. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(MailMergerContext context) {#create-com.aspose.words.MailMergerContext}
```
public static MailMerger create(MailMergerContext context)
```


Posta birleştirici işlemcisinin yeni bir örneğini oluşturur.

 **Examples:** 

Bağlam kullanarak tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

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

Bağlam kullanarak akıştan tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

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

Bağlam kullanarak bir DataRow'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

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

Bağlam kullanarak akıştan belgelerle bir DataRow'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

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

Bağlamı kullanarak bir DataTable'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

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

Bağlamı kullanarak akıştan belgelerle bir DataTable'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

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

Bağlamı kullanarak bir DataTable'dan bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

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

Bağlamı kullanarak akıştan belgelerle bir DataTable'dan bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

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

Bağlamı kullanarak bir DataSet'ten bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

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

Bağlamı kullanarak akıştan belgelerle bir DataSet'ten bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| context | [MailMergerContext](../../com.aspose.words/mailmergercontext/) |  |

**Returns:**
[MailMerger](../../com.aspose.words/mailmerger/)
### execute() {#execute}
```
public void execute()
```


İşlemci eylemini çalıştır.

 **Examples:** 

Bağlamı kullanarak belgeleri tek bir çıktı belgesine birleştirmenin nasıl yapılacağını gösterir.

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

Bağlamı kullanarak akıştan belgeleri tek bir çıktı belgesine birleştirmenin nasıl yapılacağını gösterir.

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

Bağlamı kullanarak tek bir kod satırıyla belgeleri dönüştürmenin nasıl yapılacağını gösterir.

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

Bağlamı kullanarak akıştan belgeleri tek bir kod satırıyla dönüştürmenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)
```


Bir DataRow'dan belgeye posta birleştirme gerçekleştirir.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| outputFileName | java.lang.String | Çıktı dosya adı. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Çıktının kaydetme seçenekleri. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Posta birleştirme alanlarına eklenecek verileri içeren satır. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Posta birleştirme seçenekleri. |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```


Bir DataRow'dan belgeye posta birleştirme gerçekleştirir.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| outputFileName | java.lang.String | Çıktı dosya adı. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Çıktının kaydetme seçenekleri. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Posta birleştirme seçenekleri. |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```


Tek bir kayıt için posta birleştirme işlemi gerçekleştirir.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| outputFileName | java.lang.String | Çıktı dosya adı. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Çıktının kaydetme seçenekleri. |
| fieldNames | java.lang.String[] | Birleştirme alan adlarının dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| fieldValues | java.lang.Object[] | Birleştirme alanlarına eklenecek değerlerin dizisi. Bu dizideki eleman sayısı, fieldNames içindeki eleman sayısı ile aynı olmalıdır. |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```


Tek bir kayıt için posta birleştirme işlemi gerçekleştirir.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| outputFileName | java.lang.String | Çıktı dosya adı. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Çıktının kaydetme seçenekleri. |
| fieldNames | java.lang.String[] | Birleştirme alan adlarının dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| fieldValues | java.lang.Object[] | Birleştirme alanlarına eklenecek değerlerin dizisi. Bu dizideki eleman sayısı, fieldNames içindeki eleman sayısı ile aynı olmalıdır. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Posta birleştirme seçenekleri. |

### execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow) {#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow)
```


Bir DataRow'dan belgeye posta birleştirme gerçekleştirir.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

 **Examples:** 

Bir DataRow'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| outputFileName | java.lang.String | Çıktı dosya adı. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Posta birleştirme alanlarına eklenecek verileri içeren satır. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |

### execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable) {#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable)
```


Bir DataTable'dan belgeye posta birleştirme gerçekleştirir.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

 **Examples:** 

Bir DataTable'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| outputFileName | java.lang.String | Çıktı dosya adı. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |

### execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow) {#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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


Tek bir kayıt için posta birleştirme işlemi gerçekleştirir.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

 **Examples:** 

Tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| outputFileName | java.lang.String | Çıktı dosya adı. |
| fieldNames | java.lang.String[] | Birleştirme alan adlarının dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| fieldValues | java.lang.Object[] | Birleştirme alanlarına eklenecek değerlerin dizisi. Bu dizideki eleman sayısı, fieldNames içindeki eleman sayısı ile aynı olmalıdır. |

### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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


Bir DataRow'dan belgeye posta birleştirme gerçekleştirir ve sonucu görüntülere render eder.

 **Examples:** 

Akıştan belgeler kullanarak ve sonucu görüntülere kaydederek bir DataRow'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream | Girdi dosya akışı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının kaydetme seçenekleri. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Posta birleştirme alanlarına eklenecek verileri içeren satır. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Posta birleştirme seçenekleri. |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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


Bir DataRow'dan belgeye posta birleştirme gerçekleştirir ve sonucu görüntülere render eder.

 **Examples:** 

Akıştan belgeler kullanarak ve görüntülere kaydederek bir DataTable'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream | Girdi dosya akışı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının kaydetme seçenekleri. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Posta birleştirme seçenekleri. |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```


Tek bir kayıt için posta birleştirme işlemi gerçekleştirir ve sonucu görüntülere render eder.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream | Girdi dosya akışı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının kaydetme seçenekleri. |
| fieldNames | java.lang.String[] | Birleştirme alan adlarının dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| fieldValues | java.lang.Object[] | Birleştirme alanlarına eklenecek değerlerin dizisi. Bu dizideki eleman sayısı, fieldNames içindeki eleman sayısı ile aynı olmalıdır. |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```


Tek bir kayıt için posta birleştirme işlemi gerçekleştirir ve sonucu görüntülere render eder.

 **Examples:** 

Akıştan tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını ve sonucun görüntülere kaydedilmesini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream | Girdi dosya akışı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının kaydetme seçenekleri. |
| fieldNames | java.lang.String[] | Birleştirme alan adlarının dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| fieldValues | java.lang.Object[] | Birleştirme alanlarına eklenecek değerlerin dizisi. Bu dizideki eleman sayısı, fieldNames içindeki eleman sayısı ile aynı olmalıdır. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Posta birleştirme seçenekleri. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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


Bir DataRow'dan belgeye posta birleştirme gerçekleştirir ve sonucu görüntülere render eder.

 **Examples:** 

Bir DataRow'dan posta birleştirme işleminin nasıl yapılacağını ve sonucun görüntülere kaydedilmesini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının kaydetme seçenekleri. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Posta birleştirme alanlarına eklenecek verileri içeren satır. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Posta birleştirme seçenekleri. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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


Bir DataRow'dan belgeye posta birleştirme gerçekleştirir ve sonucu görüntülere render eder.

 **Examples:** 

Bir DataTable'dan posta birleştirme işleminin nasıl yapılacağını ve sonucun görüntülere kaydedilmesini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının kaydetme seçenekleri. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Posta birleştirme seçenekleri. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```


Tek bir kayıt için posta birleştirme işlemi gerçekleştirir ve sonucu görüntülere render eder.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının kaydetme seçenekleri. |
| fieldNames | java.lang.String[] | Birleştirme alan adlarının dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| fieldValues | java.lang.Object[] | Birleştirme alanlarına eklenecek değerlerin dizisi. Bu dizideki eleman sayısı, fieldNames içindeki eleman sayısı ile aynı olmalıdır. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```


Tek bir kayıt için posta birleştirme işlemi gerçekleştirir ve sonucu görüntülere render eder.

 **Examples:** 

Tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını ve sonucun görüntülere kaydedilmesini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının kaydetme seçenekleri. |
| fieldNames | java.lang.String[] | Birleştirme alan adlarının dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| fieldValues | java.lang.Object[] | Birleştirme alanlarına eklenecek değerlerin dizisi. Bu dizideki eleman sayısı, fieldNames içindeki eleman sayısı ile aynı olmalıdır. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Posta birleştirme seçenekleri. |

**Returns:**
java.io.OutputStream[]
### executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)
```


Bir DataSet'ten belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| outputFileName | java.lang.String | Çıktı dosya adı. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Çıktının kaydetme seçenekleri. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | Posta birleştirme alanlarına eklenecek verileri içeren DataSet. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Posta birleştirme seçenekleri. |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```


Bir DataTable'dan belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| outputFileName | java.lang.String | Çıktı dosya adı. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Çıktının kaydetme seçenekleri. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Posta birleştirme seçenekleri. |

### executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet)
```


Bir DataSet'ten belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

 **Examples:** 

Bir DataSet'ten bölge tabanlı posta birleştirme işleminin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| outputFileName | java.lang.String | Çıktı dosya adı. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | Posta birleştirme alanlarına eklenecek verileri içeren DataSet. |

### executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable)
```


Bir DataTable'dan belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

 **Examples:** 

Bir DataTable'dan bölge tabanlı posta birleştirme işleminin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| outputFileName | java.lang.String | Çıktı dosya adı. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Posta birleştirme işlemi için veri kaynağı. Tablonun TableName özelliği ayarlanmış olmalıdır. |

### executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet) {#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
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


Bir DataSet'ten belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir ve sonucu görüntülere render eder.

 **Examples:** 

Akıştan belgeler kullanarak ve sonucu görüntülere kaydederek bir DataSet'ten bölge tabanlı posta birleştirme işleminin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream | Girdi dosya akışı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının kaydetme seçenekleri. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | Posta birleştirme alanlarına eklenecek verileri içeren DataSet. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Posta birleştirme seçenekleri. |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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


Bir DataTable'dan belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir ve sonucu görüntülere render eder.

 **Examples:** 

Akıştan belgeler kullanarak ve sonucu görüntülere kaydederek bir DataTable'dan bölge tabanlı posta birleştirme işleminin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream | Girdi dosya akışı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının kaydetme seçenekleri. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Posta birleştirme seçenekleri. |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet) {#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet}
```
public static OutputStream[] executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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


Bir DataSet'ten belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir ve sonucu görüntülere render eder.

 **Examples:** 

Bir DataSet'ten bölge tabanlı posta birleştirme işleminin nasıl yapılacağını ve sonucun görüntülere kaydedilmesini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının kaydetme seçenekleri. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | Posta birleştirme alanlarına eklenecek verileri içeren DataSet. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Posta birleştirme seçenekleri. |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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


Bir DataTable'dan belgeye posta birleştirme bölgeleriyle birlikte posta birleştirme gerçekleştirir ve sonucu görüntülere render eder.

 **Examples:** 

Bir DataTable'dan bölge tabanlı posta birleştirme işleminin nasıl yapılacağını ve sonucun görüntülere kaydedilmesini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFileName | java.lang.String | Girdi dosya adı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının kaydetme seçenekleri. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunamayan bir alan adıyla karşılaşıldığında, göz ardı edilir. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Posta birleştirme seçenekleri. |

**Returns:**
java.io.OutputStream[]
### from(InputStream input) {#from-java.io.InputStream}
```
public Processor from(InputStream input)
```


İşleme için giriş belgesini belirtir.

 **Remarks:** 

İşlemci yalnızca bir dosyayı girdi olarak kabul ediyorsa, yalnızca son belirtilen dosya işlenecektir. [Merger](../../com.aspose.words/merger/) işlemcisi birden fazla dosyayı girdi olarak kabul eder, bu nedenle belirtilen tüm belgeler birleştirilecektir. [Converter](../../com.aspose.words/converter/) işlemcisi yalnızca bir dosyayı girdi olarak kabul eder, bu yüzden yalnızca son belirtilen dosya dönüştürülecektir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| girdi | java.io.InputStream | Girdi belge akışı. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


İşleme için giriş belgesini belirtir.

 **Remarks:** 

İşlemci yalnızca bir dosyayı girdi olarak kabul ediyorsa, yalnızca son belirtilen dosya işlenecektir. [Merger](../../com.aspose.words/merger/) işlemcisi birden fazla dosyayı girdi olarak kabul eder, bu nedenle belirtilen tüm belgeler birleştirilecektir. [Converter](../../com.aspose.words/converter/) işlemcisi yalnızca bir dosyayı girdi olarak kabul eder, bu yüzden yalnızca son belirtilen dosya dönüştürülecektir.

 **Examples:** 

Bağlamı kullanarak akıştan belgeleri tek bir çıktı belgesine birleştirmenin nasıl yapılacağını gösterir.

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

Bağlamı kullanarak akıştan belgeleri tek bir kod satırıyla dönüştürmenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| girdi | java.io.InputStream | Girdi belge akışı. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Belgeyi yüklemek için kullanılan isteğe bağlı yükleme seçenekleri. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


İşleme için giriş belgesini belirtir.

 **Remarks:** 

İşlemci yalnızca bir dosyayı girdi olarak kabul ediyorsa, yalnızca son belirtilen dosya işlenecektir. [Merger](../../com.aspose.words/merger/) işlemcisi birden fazla dosyayı girdi olarak kabul eder, bu nedenle belirtilen tüm belgeler birleştirilecektir. [Converter](../../com.aspose.words/converter/) işlemcisi yalnızca bir dosyayı girdi olarak kabul eder, bu yüzden yalnızca son belirtilen dosya dönüştürülecektir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| girdi | java.lang.String | Girdi belge dosya adı. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


İşleme için giriş belgesini belirtir.

 **Remarks:** 

İşlemci yalnızca bir dosyayı girdi olarak kabul ediyorsa, yalnızca son belirtilen dosya işlenecektir. [Merger](../../com.aspose.words/merger/) işlemcisi birden fazla dosyayı girdi olarak kabul eder, bu nedenle belirtilen tüm belgeler birleştirilecektir. [Converter](../../com.aspose.words/converter/) işlemcisi yalnızca bir dosyayı girdi olarak kabul eder, bu yüzden yalnızca son belirtilen dosya dönüştürülecektir.

 **Examples:** 

Bağlamı kullanarak belgeleri tek bir çıktı belgesine birleştirmenin nasıl yapılacağını gösterir.

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

Bağlamı kullanarak tek bir kod satırıyla belgeleri dönüştürmenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| girdi | java.lang.String | Girdi belge dosya adı. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Belgeyi yüklemek için kullanılan isteğe bağlı yükleme seçenekleri. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


İşlemci için çıktı dosyasını belirtir.

 **Remarks:** 

Çıktı birden fazla dosyadan oluşuyorsa, belirtilen çıktı dosya adı, her bölüm için 'outputFile\_partIndex.extension' kuralına göre dosya adı oluşturmak için kullanılır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.lang.String | Çıktı dosya adı. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


İşlemci için çıktı dosyasını belirtir.

 **Remarks:** 

Çıktı birden fazla dosyadan oluşuyorsa, belirtilen çıktı dosya adı, her bölüm için 'outputFile\_partIndex.extension' kuralına göre dosya adı oluşturmak için kullanılır.

 **Examples:** 

Bağlamı kullanarak belgeleri tek bir çıktı belgesine birleştirmenin nasıl yapılacağını gösterir.

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

Bağlamı kullanarak tek bir kod satırıyla belgeleri dönüştürmenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.lang.String | Çıktı dosya adı. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | İsteğe bağlı kaydetme seçenekleri. Belirtilmezse, kaydetme biçimi dosya uzantısına göre belirlenir. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
