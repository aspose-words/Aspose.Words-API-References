---
title: "PdfPermissions"
linktitle: "PdfPermissions"
second_title: "Aspose.Words для Java"
description: "Указывает операции, разрешённые пользователю над зашифрованным PDF‑документом в Java."
type: docs
weight: 541
url: /ru/java/com.aspose.words/pdfpermissions/
---

**Inheritance:**
java.lang.Object
```
public class PdfPermissions
```

Указывает операции, разрешённые пользователю в зашифрованном PDF‑документе.

 **Examples:** 

Показывает, как установить разрешения для сохранённого PDF‑документа.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [ALLOW_ALL](#ALLOW-ALL) | Разрешает все операции над PDF‑документом. |
| [CONTENT_COPY](#CONTENT-COPY) | Копировать или иным способом извлекать текст и графику из документа операциями, отличными от контролируемых [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY). |
| [CONTENT_COPY_FOR_ACCESSIBILITY](#CONTENT-COPY-FOR-ACCESSIBILITY) | Извлекать текст и графику (в целях обеспечения доступности для пользователей с ограниченными возможностями или для других целей). |
| [DISALLOW_ALL](#DISALLOW-ALL) | Запрещает все операции над PDF‑документом. |
| [DOCUMENT_ASSEMBLY](#DOCUMENT-ASSEMBLY) | Собирать документ (вставлять, вращать или удалять страницы и создавать элементы структуры документа или миниатюры), даже если [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) не установлен. |
| [FILL_IN](#FILL-IN) | Заполнять существующие интерактивные поля формы (включая поля подписи), даже если [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) не установлен. |
| [HIGH_RESOLUTION_PRINTING](#HIGH-RESOLUTION-PRINTING) | Печатать документ в представление, из которого может быть создана точная цифровая копия содержимого PDF, на основе зависящего от реализации алгоритма. |
| [MODIFY_ANNOTATIONS](#MODIFY-ANNOTATIONS) | Добавлять или изменять текстовые аннотации, заполнять интерактивные поля формы и, если [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) также установлен, создавать или изменять интерактивные поля формы (включая поля подписи). |
| [MODIFY_CONTENTS](#MODIFY-CONTENTS) | Изменять содержимое документа операциями, отличными от контролируемых [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions/\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions/\#FILL-IN), и [DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions/\#DOCUMENT-ASSEMBLY). |
| [PRINTING](#PRINTING) | Печатать документ (возможно не в наивысшем качестве, в зависимости от того, установлен ли также [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions/\#HIGH-RESOLUTION-PRINTING)). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String pdfPermissionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set pdfPermissionsNames)](#fromNames-java.util.Set) |  |
| [getName(int pdfPermissions)](#getName-int) |  |
| [getNames(int pdfPermissions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPermissions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### ALLOW_ALL {#ALLOW-ALL}
```
public static int ALLOW_ALL
```


Разрешает все операции над PDF‑документом.

### CONTENT_COPY {#CONTENT-COPY}
```
public static int CONTENT_COPY
```


Копировать или иным способом извлекать текст и графику из документа операциями, отличными от контролируемых [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY).

### CONTENT_COPY_FOR_ACCESSIBILITY {#CONTENT-COPY-FOR-ACCESSIBILITY}
```
public static int CONTENT_COPY_FOR_ACCESSIBILITY
```


Извлекать текст и графику (в целях обеспечения доступности для пользователей с ограниченными возможностями или для других целей).

### DISALLOW_ALL {#DISALLOW-ALL}
```
public static int DISALLOW_ALL
```


Запрещает все операции над PDF‑документом. Это значение по умолчанию.

### DOCUMENT_ASSEMBLY {#DOCUMENT-ASSEMBLY}
```
public static int DOCUMENT_ASSEMBLY
```


Собирать документ (вставлять, вращать или удалять страницы и создавать элементы структуры документа или миниатюры), даже если [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) не установлен.

### FILL_IN {#FILL-IN}
```
public static int FILL_IN
```


Заполнять существующие интерактивные поля формы (включая поля подписи), даже если [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) не установлен.

### HIGH_RESOLUTION_PRINTING {#HIGH-RESOLUTION-PRINTING}
```
public static int HIGH_RESOLUTION_PRINTING
```


Печатать документ в представление, из которого может быть создана точная цифровая копия содержимого PDF, на основе зависящего от реализации алгоритма. Когда этот флаг не установлен (и [PRINTING](../../com.aspose.words/pdfpermissions/\#PRINTING) установлен), печать должна быть ограничена низкоуровневым представлением внешнего вида, возможно с пониженным качеством.

### MODIFY_ANNOTATIONS {#MODIFY-ANNOTATIONS}
```
public static int MODIFY_ANNOTATIONS
```


Добавлять или изменять текстовые аннотации, заполнять интерактивные поля формы и, если [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) также установлен, создавать или изменять интерактивные поля формы (включая поля подписи).

### MODIFY_CONTENTS {#MODIFY-CONTENTS}
```
public static int MODIFY_CONTENTS
```


Изменять содержимое документа операциями, отличными от контролируемых [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions/\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions/\#FILL-IN), и [DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions/\#DOCUMENT-ASSEMBLY).

### PRINTING {#PRINTING}
```
public static int PRINTING
```


Печатать документ (возможно не в наивысшем качестве, в зависимости от того, установлен ли также [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions/\#HIGH-RESOLUTION-PRINTING)).

### length {#length}
```
public static int length
```


### fromName(String pdfPermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPermissionsName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPermissionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set pdfPermissionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set pdfPermissionsNames)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPermissionsNames | java.util.Set |  |

**Returns:**
int
### getName(int pdfPermissions) {#getName-int}
```
public static String getName(int pdfPermissions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.lang.String
### getNames(int pdfPermissions) {#getNames-int}
```
public static Set getNames(int pdfPermissions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfPermissions) {#toString-int}
```
public static String toString(int pdfPermissions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
