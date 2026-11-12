---
title: "ComparerContext"
linktitle: "ComparerContext"
second_title: "Aspose.Words для Java"
description: "Контекст сравнения документов в Java."
type: docs
weight: 115
url: /ru/java/com.aspose.words/comparercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ComparerContext extends ProcessorContext
```

Контекст сравнения документов

 **Examples:** 

Показывает, как просто сравнивать документы, используя контекст.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 ComparerContext comparerContext = new ComparerContext();
 comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
 comparerContext.setAuthor("Author");
 comparerContext.setDateTime(new Date());

 Comparer.create(comparerContext)
         .from(firstDoc)
         .from(secondDoc)
         .to(getArtifactsDir() + "LowCode.CompareContextDocuments.docx")
         .execute();
 
```

Показывает, как сравнивать документы из потока, используя контекст.

```

 // There is a several ways to compare documents from the stream:
 try (FileInputStream firstStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.docx")) {
     try (FileInputStream secondStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.doc")) {
         ComparerContext comparerContext = new ComparerContext();
         comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
         comparerContext.setAuthor("Author");
         comparerContext.setDateTime(new Date());

         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.CompareContextStreamDocuments.docx")) {
             Comparer.create(comparerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [ComparerContext()](#ComparerContext) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [getAcceptRevisions()](#getAcceptRevisions) | Указывает, принимать ли исправления в документах перед их сравнением. |
| [getAuthor()](#getAuthor) | Автор, который будет назначен исправлениям, созданным во время сравнения документов. |
| [getCompareOptions()](#getCompareOptions) | Параметры, используемые при сравнении документов. |
| [getDateTime()](#getDateTime) | Дата и время, назначенные исправлениям, созданным во время сравнения документов. |
| [getFontSettings()](#getFontSettings) | Настройки шрифтов, используемые процессором. |
| [getLayoutOptions()](#getLayoutOptions) | Параметры макета документа, используемые процессором. |
| [getWarningCallback()](#getWarningCallback) | Обратный вызов предупреждения, используемый процессором. |
| [setAcceptRevisions(boolean value)](#setAcceptRevisions-boolean) | Указывает, принимать ли исправления в документах перед их сравнением. |
| [setAuthor(String value)](#setAuthor-java.lang.String) | Автор, который будет назначен исправлениям, созданным во время сравнения документов. |
| [setDateTime(Date value)](#setDateTime-java.util.Date) | Дата и время, назначенные исправлениям, созданным во время сравнения документов. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Настройки шрифтов, используемые процессором. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Обратный вызов предупреждения, используемый процессором. |
### ComparerContext() {#ComparerContext}
```
public ComparerContext()
```


Инициализирует новый экземпляр этого класса.

### getAcceptRevisions() {#getAcceptRevisions}
```
public boolean getAcceptRevisions()
```


Указывает, принимать ли исправления в документах перед их сравнением. Если сравниваемые документы содержат исправления и этот флаг установлен в false, процессор отклонит исправления. По умолчанию — true.

**Returns:**
boolean - Соответствующее  boolean  значение.
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Автор, который будет назначен исправлениям, созданным во время сравнения документов.

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getCompareOptions() {#getCompareOptions}
```
public CompareOptions getCompareOptions()
```


Параметры, используемые при сравнении документов.

 **Examples:** 

Показывает, как просто сравнивать документы, используя контекст.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 ComparerContext comparerContext = new ComparerContext();
 comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
 comparerContext.setAuthor("Author");
 comparerContext.setDateTime(new Date());

 Comparer.create(comparerContext)
         .from(firstDoc)
         .from(secondDoc)
         .to(getArtifactsDir() + "LowCode.CompareContextDocuments.docx")
         .execute();
 
```

Показывает, как сравнивать документы из потока, используя контекст.

```

 // There is a several ways to compare documents from the stream:
 try (FileInputStream firstStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.docx")) {
     try (FileInputStream secondStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.doc")) {
         ComparerContext comparerContext = new ComparerContext();
         comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
         comparerContext.setAuthor("Author");
         comparerContext.setDateTime(new Date());

         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.CompareContextStreamDocuments.docx")) {
             Comparer.create(comparerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

**Returns:**
[CompareOptions](../../com.aspose.words/compareoptions/) - The corresponding [CompareOptions](../../com.aspose.words/compareoptions/) value.
### getDateTime() {#getDateTime}
```
public Date getDateTime()
```


Дата и время, назначенные исправлениям, созданным во время сравнения документов.

**Returns:**
java.util.Date — соответствующее значение java.util.Date.
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
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Обратный вызов предупреждения, используемый процессором.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setAcceptRevisions(boolean value) {#setAcceptRevisions-boolean}
```
public void setAcceptRevisions(boolean value)
```


Указывает, принимать ли исправления в документах перед их сравнением. Если сравниваемые документы содержат исправления и этот флаг установлен в false, процессор отклонит исправления. По умолчанию — true.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setAuthor(String value) {#setAuthor-java.lang.String}
```
public void setAuthor(String value)
```


Автор, который будет назначен исправлениям, созданным во время сравнения документов.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setDateTime(Date value) {#setDateTime-java.util.Date}
```
public void setDateTime(Date value)
```


Дата и время, назначенные исправлениям, созданным во время сравнения документов.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.util.Date | Соответствующее значение java.util.Date. |

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

