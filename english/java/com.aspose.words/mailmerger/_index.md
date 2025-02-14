---
title: MailMerger
linktitle: MailMerger
second_title: Aspose.Words for Java
description: Provides methods intended to fill template with data using simple mail merge and mail merge with regions operations in Java.
type: docs
weight: 437
url: /java/com.aspose.words/mailmerger/
---

**Inheritance:**
java.lang.Object
```
public class MailMerger
```

Provides methods intended to fill template with data using simple mail merge and mail merge with regions operations.
## Methods

| Method | Description |
| --- | --- |
| [execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataRow dataRow)](#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataRow) |  |
| [execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)](#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, String[] fieldNames, Object[] fieldValues)](#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-java.lang.String---java.lang.Object) |  |
| [execute(InputStream inputStream, OutputStream outputStream, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataRow dataRow)](#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataRow) |  |
| [execute(InputStream inputStream, OutputStream outputStream, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)](#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(InputStream inputStream, OutputStream outputStream, int saveFormat, MailMergeOptions mailMergeOptions, String[] fieldNames, Object[] fieldValues)](#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.MailMergeOptions-java.lang.String---java.lang.Object) |  |
| [execute(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataRow dataRow)](#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataRow) |  |
| [execute(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable)](#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(InputStream inputStream, OutputStream outputStream, int saveFormat, String[] fieldNames, Object[] fieldValues)](#execute-java.io.InputStream-java.io.OutputStream-int-java.lang.String---java.lang.Object) |  |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataRow dataRow)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataRow) | Performs mail merge from a DataRow into the document. |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable) | Performs mail merge from a DataRow into the document. |
| [execute(String inputFileName, String outputFileName, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-java.lang.String---java.lang.Object) | Performs a mail merge operation for a single record. |
| [execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow)](#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataRow) | Performs mail merge from a DataRow into the document. |
| [execute(String inputFileName, String outputFileName, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Performs mail merge from a DataTable into the document. |
| [execute(String inputFileName, String outputFileName, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataRow dataRow)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataRow) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, MailMergeOptions mailMergeOptions, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.MailMergeOptions-java.lang.String---java.lang.Object) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataRow dataRow)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataRow) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable)](#execute-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable) |  |
| [execute(String inputFileName, String outputFileName, int saveFormat, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-int-java.lang.String---java.lang.Object) |  |
| [execute(String inputFileName, String outputFileName, String[] fieldNames, Object[] fieldValues)](#execute-java.lang.String-java.lang.String-java.lang.String---java.lang.Object) | Performs a mail merge operation for a single record. |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataSet dataSet)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataSet dataSet)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataSet dataSet)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, System.Data.DataTable dataTable)](#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataSet) | Performs mail merge from a DataTable into the document with mail merge regions. |
| [executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable) | Performs mail merge from a DataTable into the document with mail merge regions. |
| [executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataSet) | Performs mail merge from a DataSet into a document with mail merge regions. |
| [executeWithRegions(String inputFileName, String outputFileName, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Performs mail merge from a DataTable into the document with mail merge regions. |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataSet dataSet)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataSet) |  |
| [executeWithRegions(String inputFileName, String outputFileName, int saveFormat, System.Data.DataTable dataTable)](#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.net.System.Data.DataTable) |  |
### execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataRow dataRow) {#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable) {#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, String[] fieldNames, Object[] fieldValues) {#execute-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-java.lang.String---java.lang.Object}
```
public static void execute(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, String[] fieldNames, Object[] fieldValues)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |
| fieldNames | java.lang.String[] |  |
| fieldValues | java.lang.Object[] |  |

### execute(InputStream inputStream, OutputStream outputStream, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataRow dataRow) {#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(InputStream inputStream, OutputStream outputStream, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### execute(InputStream inputStream, OutputStream outputStream, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable) {#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(InputStream inputStream, OutputStream outputStream, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### execute(InputStream inputStream, OutputStream outputStream, int saveFormat, MailMergeOptions mailMergeOptions, String[] fieldNames, Object[] fieldValues) {#execute-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.MailMergeOptions-java.lang.String---java.lang.Object}
```
public static void execute(InputStream inputStream, OutputStream outputStream, int saveFormat, MailMergeOptions mailMergeOptions, String[] fieldNames, Object[] fieldValues)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |
| fieldNames | java.lang.String[] |  |
| fieldValues | java.lang.Object[] |  |

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

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataRow dataRow) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataRow dataRow)
```


Performs mail merge from a DataRow into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The output's save options. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Row that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)
```


Performs mail merge from a DataRow into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The output's save options. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

### execute(String inputFileName, String outputFileName, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, String[] fieldNames, Object[] fieldValues) {#execute-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-java.lang.String---java.lang.Object}
```
public static void execute(String inputFileName, String outputFileName, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, String[] fieldNames, Object[] fieldValues)
```


Performs a mail merge operation for a single record.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The output's save options. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |
| fieldNames | java.lang.String[] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| fieldValues | java.lang.Object[] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |

### execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow) {#execute-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(String inputFileName, String outputFileName, System.Data.DataRow dataRow)
```


Performs mail merge from a DataRow into the document.

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
 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMergeDataRow.3.docx", SaveFormat.DOCX, options, dataRow);
 
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
 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMergeDataTable.3.docx", SaveFormat.DOCX, options, dataTable);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

### execute(String inputFileName, String outputFileName, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataRow dataRow) {#execute-java.lang.String-java.lang.String-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataRow}
```
public static void execute(String inputFileName, String outputFileName, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataRow dataRow)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### execute(String inputFileName, String outputFileName, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable) {#execute-java.lang.String-java.lang.String-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void execute(String inputFileName, String outputFileName, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### execute(String inputFileName, String outputFileName, int saveFormat, MailMergeOptions mailMergeOptions, String[] fieldNames, Object[] fieldValues) {#execute-java.lang.String-java.lang.String-int-com.aspose.words.MailMergeOptions-java.lang.String---java.lang.Object}
```
public static void execute(String inputFileName, String outputFileName, int saveFormat, MailMergeOptions mailMergeOptions, String[] fieldNames, Object[] fieldValues)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |
| fieldNames | java.lang.String[] |  |
| fieldValues | java.lang.Object[] |  |

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

### execute(String inputFileName, String outputFileName, String[] fieldNames, Object[] fieldValues) {#execute-java.lang.String-java.lang.String-java.lang.String---java.lang.Object}
```
public static void execute(String inputFileName, String outputFileName, String[] fieldNames, Object[] fieldValues)
```


Performs a mail merge operation for a single record.

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
 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMerge.3.docx", SaveFormat.DOCX, options, fieldNames, fieldValues);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| fieldNames | java.lang.String[] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| fieldValues | java.lang.Object[] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |

### executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataSet dataSet) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataSet dataSet)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |

### executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataSet dataSet) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataSet dataSet)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |

### executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable) {#executeWithRegions-java.io.InputStream-java.io.OutputStream-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(InputStream inputStream, OutputStream outputStream, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

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

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataSet dataSet) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataSet dataSet)
```


Performs mail merge from a DataTable into the document with mail merge regions.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The output's save options. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) | DataSet that contains data to be inserted into mail merge fields. |

### executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(String inputFileName, String outputFileName, SaveOptions saveOptions, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)
```


Performs mail merge from a DataTable into the document with mail merge regions.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The output's save options. |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) | Mail merge options. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

### executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet) {#executeWithRegions-java.lang.String-java.lang.String-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(String inputFileName, String outputFileName, System.Data.DataSet dataSet)
```


Performs mail merge from a DataSet into a document with mail merge regions.

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
 MailMerger.executeWithRegions(doc, getArtifactsDir() + "LowCode.MailMergeWithRegionsDataSet.3.docx", SaveFormat.DOCX, options, dataSet);
 
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
 MailMerger.executeWithRegions(doc, getArtifactsDir() + "LowCode.MailMergeWithRegionsDataTable.3.docx", SaveFormat.DOCX, options, dataTable);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Data source for the mail merge operation. The table must have its TableName property set. |

### executeWithRegions(String inputFileName, String outputFileName, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataSet dataSet) {#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataSet}
```
public static void executeWithRegions(String inputFileName, String outputFileName, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataSet dataSet)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |

### executeWithRegions(String inputFileName, String outputFileName, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable) {#executeWithRegions-java.lang.String-java.lang.String-int-com.aspose.words.MailMergeOptions-com.aspose.words.net.System.Data.DataTable}
```
public static void executeWithRegions(String inputFileName, String outputFileName, int saveFormat, MailMergeOptions mailMergeOptions, System.Data.DataTable dataTable)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| mailMergeOptions | [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) |  |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

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

