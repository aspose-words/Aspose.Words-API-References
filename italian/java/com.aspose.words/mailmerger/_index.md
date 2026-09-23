---
title: "MailMerger"
linktitle: "MailMerger"
second_title: "Aspose.Words per Java"
description: "Fornisce metodi destinati a riempire il modello con dati utilizzando operazioni di unione semplice e unione con regioni in Java."
type: docs
weight: 446
url: /it/java/com.aspose.words/mailmerger/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class MailMerger extends Processor
```

Fornisce metodi destinati a riempire il modello con i dati utilizzando operazioni di mail merge semplice e mail merge con regioni.
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [create(MailMergerContext context)](#create-com.aspose.words.MailMergerContext) | Crea una nuova istanza del processore di mail merge. |
| [execute()](#execute) | Esegui l'azione del processore. |
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
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) | Esegue l'unione della posta da un DataRow nel documento. |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Esegue l'unione della posta da un DataRow nel documento. |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object) | Esegue un'operazione di mail merge per un singolo record. |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) | Esegue un'operazione di mail merge per un singolo record. |
| [execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow)](#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataRow) | Esegue l'unione della posta da un DataRow nel documento. |
| [execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Esegue l'unione della posta da un DataTable nel documento. |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-int-java.lang.String---java.lang.Object) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#execute-java.lang.String-java.lang.String-int-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) |  |
| [execute(String inputFileName, String outputFileName, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-java.lang.String---java.lang.Object) | Esegue un'operazione di mail merge per un singolo record. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow) |  |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) | Esegue l'unione della posta da un DataRow nel documento e rende il risultato in immagini. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Esegue l'unione della posta da un DataRow nel documento e rende il risultato in immagini. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object) | Esegue un'operazione di mail merge per un singolo record e rende il risultato in immagini. |
| [executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) | Esegue un'operazione di mail merge per un singolo record e rende il risultato in immagini. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow) |  |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions) | Esegue l'unione della posta da un DataRow nel documento e rende il risultato in immagini. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Esegue l'unione della posta da un DataRow nel documento e rende il risultato in immagini. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object) | Esegue un'operazione di mail merge per un singolo record e rende il risultato in immagini. |
| [executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)](#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions) | Esegue un'operazione di mail merge per un singolo record e rende il risultato in immagini. |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataSet dataSet)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) | Esegue l'unione della posta da un DataSet nel documento con regioni di mail merge. |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Esegue l'unione della posta da un DataTable nel documento con regioni di mail merge. |
| [executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataSet) | Esegue l'unione della posta da un DataSet in un documento con regioni di mail merge. |
| [executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Esegue l'unione della posta da un DataTable nel documento con regioni di mail merge. |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) |  |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) | Esegue l'unione della posta da un DataSet nel documento con regioni di mail merge e rende il risultato in immagini. |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Esegue l'unione della posta da un DataTable nel documento con regioni di mail merge e rende il risultato in immagini. |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions) | Esegue l'unione della posta da un DataSet nel documento con regioni di mail merge e rende il risultato in immagini. |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)](#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions) | Esegue l'unione della posta da un DataTable nel documento con regioni di mail merge e rende il risultato in immagini. |
| [from(InputStream input)](#from-java.io.InputStream) | Specifica il documento di input per l'elaborazione. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Specifica il documento di input per l'elaborazione. |
| [from(String input)](#from-java.lang.String) | Specifica il documento di input per l'elaborazione. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Specifica il documento di input per l'elaborazione. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Specifica il file di output per il processore. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Specifica il file di output per il processore. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(MailMergerContext context) {#create-com.aspose.words.MailMergerContext}
```
public static MailMerger create(MailMergerContext context)
```


Crea una nuova istanza del processore di mail merge.

 **Examples:** 

Mostra come eseguire un'operazione di mail merge per un singolo record usando il contesto.

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

Mostra come eseguire un'operazione di mail merge per un singolo record dallo stream usando il contesto.

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

Mostra come eseguire un'operazione di mail merge da un DataRow usando il contesto.

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

Mostra come eseguire un'operazione di mail merge da un DataRow usando documenti dallo stream con il contesto.

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

Mostra come eseguire l'operazione di stampa unione da una DataTable usando il contesto.

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

Mostra come eseguire l'operazione di stampa unione da una DataTable usando documenti dallo stream con il contesto.

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

Mostra come eseguire l'operazione di stampa unione con regioni da una DataTable usando il contesto.

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

Mostra come eseguire l'operazione di stampa unione con regioni da una DataTable usando documenti dallo stream con il contesto.

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

Mostra come eseguire l'operazione di stampa unione con regioni da un DataSet usando il contesto.

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

Mostra come eseguire l'operazione di stampa unione con regioni da un DataSet usando documenti dallo stream con il contesto.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| context | [MailMergerContext](../../com.aspose.words/mailmergercontext/) |  |

**Returns:**
[MailMerger](../../com.aspose.words/mailmerger/)
### execute() {#execute}
```
public void execute()
```


Esegui l'azione del processore.

 **Examples:** 

Mostra come unire documenti in un unico documento di output usando il contesto.

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

Mostra come unire documenti dallo stream in un unico documento di output usando il contesto.

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

Mostra come convertire documenti con una singola riga di codice usando il contesto.

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

Mostra come convertire documenti dallo stream con una singola riga di codice usando il contesto.

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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataRow-com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataRow dataRow, MailMergeOptions mailMergeOptions)
```


Esegue l'unione della posta da un DataRow nel documento.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| outputFileName | java.lang.String | Il nome file di output. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Le opzioni di salvataggio dell'output. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Riga che contiene i dati da inserire nei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Opzioni di stampa unione. |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```


Esegue l'unione della posta da un DataRow nel documento.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| outputFileName | java.lang.String | Il nome file di output. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Le opzioni di salvataggio dell'output. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Tabella che contiene i dati da inserire nei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Opzioni di stampa unione. |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```


Esegue un'operazione di mail merge per un singolo record.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| outputFileName | java.lang.String | Il nome file di output. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Le opzioni di salvataggio dell'output. |
| fieldNames | java.lang.String[] | Array di nomi dei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| fieldValues | java.lang.Object[] | Array di valori da inserire nei campi di stampa unione. Il numero di elementi in questo array deve essere lo stesso del numero di elementi in fieldNames. |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```


Esegue un'operazione di mail merge per un singolo record.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| outputFileName | java.lang.String | Il nome file di output. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Le opzioni di salvataggio dell'output. |
| fieldNames | java.lang.String[] | Array di nomi dei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| fieldValues | java.lang.Object[] | Array di valori da inserire nei campi di stampa unione. Il numero di elementi in questo array deve essere lo stesso del numero di elementi in fieldNames. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Opzioni di stampa unione. |

### execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow) {#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow)
```


Esegue l'unione della posta da un DataRow nel documento.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

 **Examples:** 

Mostra come eseguire l'operazione di stampa unione da una DataRow.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| outputFileName | java.lang.String | Il nome file di output. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Riga che contiene i dati da inserire nei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |

### execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable) {#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable)
```


Esegue l'unione della posta da un DataTable nel documento.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

 **Examples:** 

Mostra come eseguire l'operazione di stampa unione da una DataTable.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| outputFileName | java.lang.String | Il nome file di output. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Tabella che contiene i dati da inserire nei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |

### execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow) {#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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


Esegue un'operazione di mail merge per un singolo record.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

 **Examples:** 

Mostra come eseguire l'operazione di stampa unione per un singolo record.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| outputFileName | java.lang.String | Il nome file di output. |
| fieldNames | java.lang.String[] | Array di nomi dei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| fieldValues | java.lang.Object[] | Array di valori da inserire nei campi di stampa unione. Il numero di elementi in questo array deve essere lo stesso del numero di elementi in fieldNames. |

### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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


Esegue l'unione della posta da un DataRow nel documento e rende il risultato in immagini.

 **Examples:** 

Mostra come eseguire l'operazione di stampa unione da una DataRow usando documenti dallo stream e salvare il risultato in immagini.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | java.io.InputStream | Lo stream del file di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio dell'output. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Riga che contiene i dati da inserire nei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Opzioni di stampa unione. |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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


Esegue l'unione della posta da un DataRow nel documento e rende il risultato in immagini.

 **Examples:** 

Mostra come eseguire l'operazione di stampa unione da una DataTable usando documenti dallo stream e salvare in immagini.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | java.io.InputStream | Lo stream del file di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio dell'output. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Tabella che contiene i dati da inserire nei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Opzioni di stampa unione. |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```


Esegue un'operazione di mail merge per un singolo record e rende il risultato in immagini.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | java.io.InputStream | Lo stream del file di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio dell'output. |
| fieldNames | java.lang.String[] | Array di nomi dei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| fieldValues | java.lang.Object[] | Array di valori da inserire nei campi di stampa unione. Il numero di elementi in questo array deve essere lo stesso del numero di elementi in fieldNames. |

**Returns:**
java.io.OutputStream[]
### executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#executeToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeToImages(InputStream inputStream, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```


Esegue un'operazione di mail merge per un singolo record e rende il risultato in immagini.

 **Examples:** 

Mostra come eseguire l'operazione di stampa unione per un singolo record dallo stream e salvare il risultato in immagini.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | java.io.InputStream | Lo stream del file di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio dell'output. |
| fieldNames | java.lang.String[] | Array di nomi dei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| fieldValues | java.lang.Object[] | Array di valori da inserire nei campi di stampa unione. Il numero di elementi in questo array deve essere lo stesso del numero di elementi in fieldNames. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Opzioni di stampa unione. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataRow}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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


Esegue l'unione della posta da un DataRow nel documento e rende il risultato in immagini.

 **Examples:** 

Mostra come eseguire l'operazione di stampa unione da una DataRow e salvare il risultato in immagini.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio dell'output. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Riga che contiene i dati da inserire nei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Opzioni di stampa unione. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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


Esegue l'unione della posta da un DataRow nel documento e rende il risultato in immagini.

 **Examples:** 

Mostra come eseguire l'operazione di stampa unione da una DataTable e salvare il risultato in immagini.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio dell'output. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Tabella che contiene i dati da inserire nei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Opzioni di stampa unione. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues)
```


Esegue un'operazione di mail merge per un singolo record e rende il risultato in immagini.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio dell'output. |
| fieldNames | java.lang.String[] | Array di nomi dei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| fieldValues | java.lang.Object[] | Array di valori da inserire nei campi di stampa unione. Il numero di elementi in questo array deve essere lo stesso del numero di elementi in fieldNames. |

**Returns:**
java.io.OutputStream[]
### executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions) {#executeToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String---java.lang.Object---com.aspose.words.MailMergeOptions}
```
public static OutputStream[] executeToImages(String inputFileName, ImageSaveOptions saveOptions, String[] fieldNames, Object[] fieldValues, MailMergeOptions mailMergeOptions)
```


Esegue un'operazione di mail merge per un singolo record e rende il risultato in immagini.

 **Examples:** 

Mostra come eseguire l'operazione di stampa unione per un singolo record e salvare il risultato in immagini.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio dell'output. |
| fieldNames | java.lang.String[] | Array di nomi dei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| fieldValues | java.lang.Object[] | Array di valori da inserire nei campi di stampa unione. Il numero di elementi in questo array deve essere lo stesso del numero di elementi in fieldNames. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Opzioni di stampa unione. |

**Returns:**
java.io.OutputStream[]
### executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, System.Data.DataSet dataSet)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataSet-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataSet dataSet, MailMergeOptions mailMergeOptions)
```


Esegue l'unione della posta da un DataSet nel documento con regioni di mail merge.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| outputFileName | java.lang.String | Il nome file di output. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Le opzioni di salvataggio dell'output. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | DataSet che contiene i dati da inserire nei campi di stampa unione. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Opzioni di stampa unione. |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.net.System.Data.DataTable-com.aspose.words.MailMergeOptions}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, System.Data.DataTable dataTable, MailMergeOptions mailMergeOptions)
```


Esegue l'unione della posta da un DataTable nel documento con regioni di mail merge.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| outputFileName | java.lang.String | Il nome file di output. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Le opzioni di salvataggio dell'output. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Tabella che contiene i dati da inserire nei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Opzioni di stampa unione. |

### executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet)
```


Esegue l'unione della posta da un DataSet in un documento con regioni di mail merge.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

 **Examples:** 

Mostra come eseguire l'operazione di stampa unione con regioni da un DataSet.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| outputFileName | java.lang.String | Il nome file di output. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | DataSet che contiene i dati da inserire nei campi di stampa unione. |

### executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable)
```


Esegue l'unione della posta da un DataTable nel documento con regioni di mail merge.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

 **Examples:** 

Mostra come eseguire l'operazione di stampa unione con regioni da una DataTable.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| outputFileName | java.lang.String | Il nome file di output. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Origine dati per l'operazione di stampa unione. La tabella deve avere impostata la proprietà TableName. |

### executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet) {#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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


Esegue l'unione della posta da un DataSet nel documento con regioni di mail merge e rende il risultato in immagini.

 **Examples:** 

Mostra come eseguire l'operazione di stampa unione con regioni da un DataSet usando documenti dallo stream e salvare il risultato in immagini.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | java.io.InputStream | Lo stream del file di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio dell'output. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | DataSet che contiene i dati da inserire nei campi di stampa unione. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Opzioni di stampa unione. |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegionsToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeWithRegionsToImages(InputStream inputStream, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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


Esegue l'unione della posta da un DataTable nel documento con regioni di mail merge e rende il risultato in immagini.

 **Examples:** 

Mostra come eseguire l'operazione di stampa unione con regioni da una DataTable usando documenti dallo stream e salvare il risultato in immagini.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | java.io.InputStream | Lo stream del file di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio dell'output. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Tabella che contiene i dati da inserire nei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Opzioni di stampa unione. |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet) {#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataSet}
```
public static OutputStream[] executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataSet dataSet)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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


Esegue l'unione della posta da un DataSet nel documento con regioni di mail merge e rende il risultato in immagini.

 **Examples:** 

Mostra come eseguire l'operazione di stampa unione con regioni da un DataSet e salvare il risultato in immagini.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio dell'output. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | DataSet che contiene i dati da inserire nei campi di stampa unione. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Opzioni di stampa unione. |

**Returns:**
java.io.OutputStream[]
### executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable) {#executeWithRegionsToImages-java.lang.String-com.aspose.words.ImageSaveOptions-com.aspose.words.net.System.Data.DataTable}
```
public static OutputStream[] executeWithRegionsToImages(String inputFileName, ImageSaveOptions saveOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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


Esegue l'unione della posta da un DataTable nel documento con regioni di mail merge e rende il risultato in immagini.

 **Examples:** 

Mostra come eseguire l'operazione di stampa unione con regioni da una DataTable e salvare il risultato in immagini.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | java.lang.String | Il nome file di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio dell'output. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Tabella che contiene i dati da inserire nei campi di stampa unione. I nomi dei campi non distinguono maiuscole/minuscole. Se viene incontrato un nome di campo non presente nel documento, viene ignorato. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Opzioni di stampa unione. |

**Returns:**
java.io.OutputStream[]
### from(InputStream input) {#from-java.io.InputStream}
```
public Processor from(InputStream input)
```


Specifica il documento di input per l'elaborazione.

 **Remarks:** 

Se il processore accetta solo un file come input, verrà elaborato solo l'ultimo file specificato. Il processore [Merger](../../com.aspose.words/merger/) accetta più file come input, quindi tutti i documenti specificati verranno uniti. Il processore [Converter](../../com.aspose.words/converter/) accetta solo un file come input, quindi solo l'ultimo file specificato verrà convertito.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| input | java.io.InputStream | Stream del documento di input. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Specifica il documento di input per l'elaborazione.

 **Remarks:** 

Se il processore accetta solo un file come input, verrà elaborato solo l'ultimo file specificato. Il processore [Merger](../../com.aspose.words/merger/) accetta più file come input, quindi tutti i documenti specificati verranno uniti. Il processore [Converter](../../com.aspose.words/converter/) accetta solo un file come input, quindi solo l'ultimo file specificato verrà convertito.

 **Examples:** 

Mostra come unire documenti dallo stream in un unico documento di output usando il contesto.

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

Mostra come convertire documenti dallo stream con una singola riga di codice usando il contesto.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| input | java.io.InputStream | Stream del documento di input. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Opzioni di caricamento opzionali usate per caricare il documento. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


Specifica il documento di input per l'elaborazione.

 **Remarks:** 

Se il processore accetta solo un file come input, verrà elaborato solo l'ultimo file specificato. Il processore [Merger](../../com.aspose.words/merger/) accetta più file come input, quindi tutti i documenti specificati verranno uniti. Il processore [Converter](../../com.aspose.words/converter/) accetta solo un file come input, quindi solo l'ultimo file specificato verrà convertito.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| input | java.lang.String | Nome file del documento di input. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Specifica il documento di input per l'elaborazione.

 **Remarks:** 

Se il processore accetta solo un file come input, verrà elaborato solo l'ultimo file specificato. Il processore [Merger](../../com.aspose.words/merger/) accetta più file come input, quindi tutti i documenti specificati verranno uniti. Il processore [Converter](../../com.aspose.words/converter/) accetta solo un file come input, quindi solo l'ultimo file specificato verrà convertito.

 **Examples:** 

Mostra come unire documenti in un unico documento di output usando il contesto.

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

Mostra come convertire documenti con una singola riga di codice usando il contesto.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| input | java.lang.String | Nome file del documento di input. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Opzioni di caricamento opzionali usate per caricare il documento. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


Specifica il file di output per il processore.

 **Remarks:** 

Se l'output consiste di più file, il nome file di output specificato viene usato per generare il nome file per ogni parte secondo la regola: 'outputFile\_partIndex.extension'.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.lang.String | Nome file di output. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Specifica il file di output per il processore.

 **Remarks:** 

Se l'output consiste di più file, il nome file di output specificato viene usato per generare il nome file per ogni parte secondo la regola: 'outputFile\_partIndex.extension'.

 **Examples:** 

Mostra come unire documenti in un unico documento di output usando il contesto.

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

Mostra come convertire documenti con una singola riga di codice usando il contesto.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.lang.String | Nome file di output. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Opzioni di salvataggio opzionali. Se non specificate, il formato di salvataggio è determinato dall'estensione del file. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
