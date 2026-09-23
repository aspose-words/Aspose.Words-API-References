---
title: "ReportBuilderContext"
linktitle: "ReportBuilderContext"
second_title: "Aspose.Words для Java"
description: "Контекст LINQ Reporting Engine в Java."
type: docs
weight: 572
url: /ru/java/com.aspose.words/reportbuildercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ReportBuilderContext extends ProcessorContext
```

Контекст LINQ Reporting Engine.

 **Examples:** 

Показывает, как заполнять документ источниками данных.

```

 public void buildReportDataSource() throws Exception {
     // There is a several ways to populate document with data sources:
     String doc = getMyDir() + "Report building.docx";

     MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.1.docx", sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.2.docx", new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.3.docx", sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.4.docx", SaveFormat.DOCX, sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.5.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.6.docx", SaveFormat.DOCX, sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.7.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"}, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.8.docx", new Object[]{sender}, new String[]{"s"}, options);

     options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(doc, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     ReportBuilder.create(reportBuilderContext)
             .from(doc)
             .to(getArtifactsDir() + "LowCode.BuildReportDataSource.9.docx")
             .execute();
 }

 public static class MessageTestClass {
     public String getName() {
         return mName;
     }

     public void setName(String value) {
         mName = value;
     }

     private String mName;

     public String getMessage() {
         return mMessage;
     }

     public void setMessage(String value) {
         mMessage = value;
     }

     private String mMessage;

     public MessageTestClass(String name, String message) {
         setName(name);
         setMessage(message);
     }
 }
 
```

Показывает, как заполнять документ источниками данных, используя документы из потока.

```

 // There is a several ways to populate document with data sources using documents from the stream:
 MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Report building.docx")) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.1.docx")) {
         ReportBuilder.buildReport(streamIn, streamOut, SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     }

     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.2.docx")) {
         ReportBuilder.buildReport(streamIn, streamOut1, SaveFormat.DOCX, sender, "s");
     }

     try (FileOutputStream streamOut2 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.3.docx")) {
         ReportBuilderOptions options = new ReportBuilderOptions();
         options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
         ReportBuilder.buildReport(streamIn, streamOut2, SaveFormat.DOCX, sender, "s", options);
     }

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     try (FileOutputStream streamOut3 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.4.docx")) {
         ReportBuilder.create(reportBuilderContext)
                 .from(streamIn)
                 .to(streamOut3, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [ReportBuilderContext()](#ReportBuilderContext) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [getDataSources()](#getDataSources) | Источники данных, используемые для построения отчёта. |
| [getFontSettings()](#getFontSettings) | Настройки шрифтов, используемые процессором. |
| [getLayoutOptions()](#getLayoutOptions) | Параметры макета документа, используемые процессором. |
| [getReportBuilderOptions()](#getReportBuilderOptions) | Параметры построения отчёта. |
| [getWarningCallback()](#getWarningCallback) | Обратный вызов предупреждения, используемый процессором. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Настройки шрифтов, используемые процессором. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Обратный вызов предупреждения, используемый процессором. |
### ReportBuilderContext() {#ReportBuilderContext}
```
public ReportBuilderContext()
```


Инициализирует новый экземпляр этого класса.

### getDataSources() {#getDataSources}
```
public LinkedHashMap getDataSources()
```


Источники данных, используемые для построения отчёта.

 **Remarks:** 

Ключ представляет источник данных, а значение — имя источника данных. Имя источника данных может быть null или пустой строкой; в таких случаях движок отчётов автоматически определит имя источника данных из указанного источника.

 **Examples:** 

Показывает, как заполнять документ источниками данных.

```

 public void buildReportDataSource() throws Exception {
     // There is a several ways to populate document with data sources:
     String doc = getMyDir() + "Report building.docx";

     MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.1.docx", sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.2.docx", new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.3.docx", sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.4.docx", SaveFormat.DOCX, sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.5.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.6.docx", SaveFormat.DOCX, sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.7.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"}, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.8.docx", new Object[]{sender}, new String[]{"s"}, options);

     options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(doc, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     ReportBuilder.create(reportBuilderContext)
             .from(doc)
             .to(getArtifactsDir() + "LowCode.BuildReportDataSource.9.docx")
             .execute();
 }

 public static class MessageTestClass {
     public String getName() {
         return mName;
     }

     public void setName(String value) {
         mName = value;
     }

     private String mName;

     public String getMessage() {
         return mMessage;
     }

     public void setMessage(String value) {
         mMessage = value;
     }

     private String mMessage;

     public MessageTestClass(String name, String message) {
         setName(name);
         setMessage(message);
     }
 }
 
```

Показывает, как заполнять документ источниками данных, используя документы из потока.

```

 // There is a several ways to populate document with data sources using documents from the stream:
 MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Report building.docx")) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.1.docx")) {
         ReportBuilder.buildReport(streamIn, streamOut, SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     }

     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.2.docx")) {
         ReportBuilder.buildReport(streamIn, streamOut1, SaveFormat.DOCX, sender, "s");
     }

     try (FileOutputStream streamOut2 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.3.docx")) {
         ReportBuilderOptions options = new ReportBuilderOptions();
         options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
         ReportBuilder.buildReport(streamIn, streamOut2, SaveFormat.DOCX, sender, "s", options);
     }

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     try (FileOutputStream streamOut3 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.4.docx")) {
         ReportBuilder.create(reportBuilderContext)
                 .from(streamIn)
                 .to(streamOut3, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Returns:**
java.util.LinkedHashMap — соответствующее значение java.util.HashMap.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Настройки шрифтов, используемые процессором.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


Параметры макета документа, используемые процессором.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getReportBuilderOptions() {#getReportBuilderOptions}
```
public ReportBuilderOptions getReportBuilderOptions()
```


Параметры построения отчёта.

 **Examples:** 

Показывает, как заполнять документ источниками данных.

```

 public void buildReportDataSource() throws Exception {
     // There is a several ways to populate document with data sources:
     String doc = getMyDir() + "Report building.docx";

     MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.1.docx", sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.2.docx", new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.3.docx", sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.4.docx", SaveFormat.DOCX, sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.5.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.6.docx", SaveFormat.DOCX, sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.7.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"}, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.8.docx", new Object[]{sender}, new String[]{"s"}, options);

     options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(doc, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     ReportBuilder.create(reportBuilderContext)
             .from(doc)
             .to(getArtifactsDir() + "LowCode.BuildReportDataSource.9.docx")
             .execute();
 }

 public static class MessageTestClass {
     public String getName() {
         return mName;
     }

     public void setName(String value) {
         mName = value;
     }

     private String mName;

     public String getMessage() {
         return mMessage;
     }

     public void setMessage(String value) {
         mMessage = value;
     }

     private String mMessage;

     public MessageTestClass(String name, String message) {
         setName(name);
         setMessage(message);
     }
 }
 
```

Показывает, как заполнять документ источниками данных, используя документы из потока.

```

 // There is a several ways to populate document with data sources using documents from the stream:
 MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Report building.docx")) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.1.docx")) {
         ReportBuilder.buildReport(streamIn, streamOut, SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     }

     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.2.docx")) {
         ReportBuilder.buildReport(streamIn, streamOut1, SaveFormat.DOCX, sender, "s");
     }

     try (FileOutputStream streamOut2 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.3.docx")) {
         ReportBuilderOptions options = new ReportBuilderOptions();
         options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
         ReportBuilder.buildReport(streamIn, streamOut2, SaveFormat.DOCX, sender, "s", options);
     }

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     try (FileOutputStream streamOut3 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.4.docx")) {
         ReportBuilder.create(reportBuilderContext)
                 .from(streamIn)
                 .to(streamOut3, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Returns:**
[ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) - The corresponding [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Обратный вызов предупреждения, используемый процессором.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Настройки шрифтов, используемые процессором.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | Соответствующее значение [FontSettings](../../com.aspose.words/fontsettings/). |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Обратный вызов предупреждения, используемый процессором.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Соответствующее значение [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

