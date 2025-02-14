---
title: ReportBuilder
linktitle: ReportBuilder
second_title: Aspose.Words for Java
description: Provides methods intended to fill template with data using LINQ Reporting Engine in Java.
type: docs
weight: 552
url: /java/com.aspose.words/reportbuilder/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuilder
```

Provides methods intended to fill template with data using LINQ Reporting Engine.
## Methods

| Method | Description |
| --- | --- |
| [buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions) | Populates the template document with data from the specified source, generating a completed report with specified output format and additional options. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) | Populates the template document with data from the specified source, generating a completed report with specified output format, a named data source reference, and additional options. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | Populates the template document with data from multiple sources, generating a completed report with a specified output format and additional options. |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, Object data)](#buildReport-java.lang.String-java.lang.String-java.lang.Object) | Populates the template document with data from the specified source, generating a completed report. |
| [buildReport(String inputFileName, String outputFileName, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-java.lang.Object-com.aspose.words.ReportBuilderOptions) | Populates the template document with data from the specified source, generating a completed report with additional options. |
| [buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName)](#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String) | Populates the template document with data from the specified source, generating a completed report with a named data source reference. |
| [buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) | Populates the template document with data from the specified source, generating a completed report with a named data source reference and additional options. |
| [buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames)](#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String) | Populates the template document with data from multiple sources, generating a completed report from the specified input and output file names. |
| [buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | Populates the template document with data from multiple sources, generating a completed report with additional options. |
### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| data | java.lang.Object |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| data | java.lang.Object |  |
| dataSourceName | java.lang.String |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| data | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| data | java.lang.Object |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| data | java.lang.Object |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| data | java.lang.Object |  |
| dataSourceName | java.lang.String |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| data | java.lang.Object |  |
| dataSourceName | java.lang.String |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| data | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| data | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)
```


Populates the template document with data from the specified source, generating a completed report with specified output format and additional options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The output's save options. |
| data | java.lang.Object | A data source object. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Additional report build options. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```


Populates the template document with data from the specified source, generating a completed report with specified output format, a named data source reference, and additional options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The output's save options. |
| data | java.lang.Object | A data source object. |
| dataSourceName | java.lang.String | A name to reference the data source object in the template. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Additional report build options. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


Populates the template document with data from multiple sources, generating a completed report with a specified output format and additional options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The output's save options. |
| data | java.lang.Object[] | An array of data source objects. |
| dataSourceNames | java.lang.String[] | An array of names to reference the data source objects within the template. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Additional report build options. |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| data | java.lang.Object |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| data | java.lang.Object |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| data | java.lang.Object |  |
| dataSourceName | java.lang.String |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| data | java.lang.Object |  |
| dataSourceName | java.lang.String |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| data | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| data | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, Object data) {#buildReport-java.lang.String-java.lang.String-java.lang.Object}
```
public static void buildReport(String inputFileName, String outputFileName, Object data)
```


Populates the template document with data from the specified source, generating a completed report.

 **Examples:** 

Shows how to populate document with data.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| data | java.lang.Object | A data source object. |

### buildReport(String inputFileName, String outputFileName, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, Object data, ReportBuilderOptions reportBuilderOptions)
```


Populates the template document with data from the specified source, generating a completed report with additional options.

 **Examples:** 

Shows how to populate document with data.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| data | java.lang.Object | A data source object. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Additional report build options. |

### buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName) {#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName)
```


Populates the template document with data from the specified source, generating a completed report with a named data source reference.

 **Examples:** 

Shows how to populate document with data sources.

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
 }

 public static class MessageTestClass {
     public String getName() {
         return mName;
     }

     ;

     public void setName(String value) {
         mName = value;
     }

     ;

     private String mName;

     public String getMessage() {
         return mMessage;
     }

     ;

     public void setMessage(String value) {
         mMessage = value;
     }

     ;

     private String mMessage;

     public MessageTestClass(String name, String message) {
         setName(name);
         setMessage(message);
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| data | java.lang.Object | A data source object. |
| dataSourceName | java.lang.String | A name to reference the data source object in the template. |

### buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```


Populates the template document with data from the specified source, generating a completed report with a named data source reference and additional options.

 **Examples:** 

Shows how to populate document with data sources.

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
 }

 public static class MessageTestClass {
     public String getName() {
         return mName;
     }

     ;

     public void setName(String value) {
         mName = value;
     }

     ;

     private String mName;

     public String getMessage() {
         return mMessage;
     }

     ;

     public void setMessage(String value) {
         mMessage = value;
     }

     ;

     private String mMessage;

     public MessageTestClass(String name, String message) {
         setName(name);
         setMessage(message);
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| data | java.lang.Object | A data source object. |
| dataSourceName | java.lang.String | A name to reference the data source object in the template. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Additional report build options. |

### buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames) {#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames)
```


Populates the template document with data from multiple sources, generating a completed report from the specified input and output file names. This overload automatically determines the save format based on the output file extension.

 **Examples:** 

Shows how to populate document with data sources.

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
 }

 public static class MessageTestClass {
     public String getName() {
         return mName;
     }

     ;

     public void setName(String value) {
         mName = value;
     }

     ;

     private String mName;

     public String getMessage() {
         return mMessage;
     }

     ;

     public void setMessage(String value) {
         mMessage = value;
     }

     ;

     private String mMessage;

     public MessageTestClass(String name, String message) {
         setName(name);
         setMessage(message);
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| data | java.lang.Object[] | An array of data source objects. |
| dataSourceNames | java.lang.String[] | An array of names to reference the data source objects within the template. |

### buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


Populates the template document with data from multiple sources, generating a completed report with additional options. This overload automatically determines the save format based on the output file extension.

 **Examples:** 

Shows how to populate document with data sources.

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
 }

 public static class MessageTestClass {
     public String getName() {
         return mName;
     }

     ;

     public void setName(String value) {
         mName = value;
     }

     ;

     private String mName;

     public String getMessage() {
         return mMessage;
     }

     ;

     public void setMessage(String value) {
         mMessage = value;
     }

     ;

     private String mMessage;

     public MessageTestClass(String name, String message) {
         setName(name);
         setMessage(message);
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| data | java.lang.Object[] | An array of data source objects. |
| dataSourceNames | java.lang.String[] | An array of names to reference the data source objects within the template. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Additional report build options. |

