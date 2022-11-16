---
title: FontSavingArgs
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет данные для события.
type: docs
weight: 285
url: /ru/java/com.aspose.words/fontsavingargs/
---

**Наследование:**
java.lang.Object
```
public class FontSavingArgs
```

 Предоставляет данные для[IFontSavingCallback.fontSaving(com.aspose.words.FontSavingArgs)](../../com.aspose.words/ifontsavingcallback\#fontSaving-com.aspose.words.FontSavingArgs-) мероприятие.

 Чтобы узнать больше, посетите**Save a Document** документальная статья.

 Когда Aspose.Words сохраняет документ в HTML или родственных форматах и[HtmlSaveOptions.getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [HtmlSaveOptions.setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) установлен на**true**, он сохраняет каждую тему шрифта для экспорта в отдельный файл.

[FontSavingArgs](../../com.aspose.words/fontsavingargs) определяет, следует ли экспортировать конкретный ресурс шрифта и каким образом.

[FontSavingArgs](../../com.aspose.words/fontsavingargs) также позволяет переопределить, как генерируются имена файлов шрифтов, или полностью обойти сохранение шрифтов в файлы, предоставив свои собственные потоковые объекты.

 Чтобы решить, сохранять ли конкретный ресурс шрифта, используйте[isExportNeeded()](../../com.aspose.words/fontsavingargs\#isExportNeeded--) / [isExportNeeded(boolean)](../../com.aspose.words/fontsavingargs\#isExportNeeded-boolean-) имущество.

 Чтобы сохранить шрифты в потоки, а не в файлы, используйте**P:Aspose.Words.Saving.FontSavingArgs.FontStream** имущество.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBold()](#getBold--) | Указывает, является ли текущий шрифт полужирным. |
| [getClass()](#getClass--) |  |
| [getDocument()](#getDocument--) | Получает сохраняемый объект документа. |
| [getFontFamilyName()](#getFontFamilyName--) | Указывает текущее имя семейства шрифтов. |
| [getFontFileName()](#getFontFileName--) | Получает имя файла (без пути), в котором будет сохранен шрифт. |
| [getFontStream()](#getFontStream--) |  |
| [getItalic()](#getItalic--) | Указывает, является ли текущий шрифт курсивом. |
| [getKeepFontStreamOpen()](#getKeepFontStreamOpen--) | Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения шрифта. |
| [getOriginalFileName()](#getOriginalFileName--) | Получает исходное имя файла шрифта с расширением. |
| [getOriginalFileSize()](#getOriginalFileSize--) | Получает исходный размер файла шрифта. |
| [hashCode()](#hashCode--) |  |
| [isExportNeeded()](#isExportNeeded--) | Позволяет указать, будет ли текущий шрифт экспортироваться как ресурс шрифта. |
| [isExportNeeded(boolean value)](#isExportNeeded-boolean-) | Позволяет указать, будет ли текущий шрифт экспортироваться как ресурс шрифта. |
| [isSubsettingNeeded()](#isSubsettingNeeded--) | Позволяет указать, будет ли текущий шрифт подмножаться перед экспортом в качестве ресурса шрифта. |
| [isSubsettingNeeded(boolean value)](#isSubsettingNeeded-boolean-) | Позволяет указать, будет ли текущий шрифт подмножаться перед экспортом в качестве ресурса шрифта. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setFontFileName(String value)](#setFontFileName-java.lang.String-) | Устанавливает имя файла (без пути), в котором будет сохранен шрифт. |
| [setFontStream(OutputStream value)](#setFontStream-java.io.OutputStream-) |  |
| [setKeepFontStreamOpen(boolean value)](#setKeepFontStreamOpen-boolean-) | Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения шрифта. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### getBold() {#getBold--}
```
public boolean getBold()
```


Указывает, является ли текущий шрифт полужирным.

**Возвращает:**
boolean - соответствующее логическое значение.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDocument() {#getDocument--}
```
public Document getDocument()
```


Получает сохраняемый объект документа.

**Возвращает:**
[Document](../../com.aspose.words/document) - Сохраняемый объект документа.
### getFontFamilyName() {#getFontFamilyName--}
```
public String getFontFamilyName()
```


Указывает текущее имя семейства шрифтов.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getFontFileName() {#getFontFileName--}
```
public String getFontFileName()
```


Получает имя файла (без пути), в котором будет сохранен шрифт.

Это свойство позволяет переопределить способ генерации имен файлов шрифтов при экспорте в HTML.

Когда событие запускается, это свойство содержит имя файла, созданное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить шрифт в другой файл. Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого встроенного шрифта при экспорте в формат HTML. Способ генерации имени файла шрифта зависит от того, сохраняете ли вы документ в файл или в поток.

При сохранении документа в файл сгенерированное имя файла шрифта выглядит так:*..*.

 При сохранении документа в поток сгенерированное имя файла шрифта выглядит так:*Aspose.Words...*.

[getFontFileName()](../../com.aspose.words/fontsavingargs\#getFontFileName--) / [setFontFileName(java.lang.String)](../../com.aspose.words/fontsavingargs\#setFontFileName-java.lang.String-) должен содержать только имя файла без пути. Aspose.Words определяет путь для сохранения по имени файла документа,[HtmlSaveOptions.getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [HtmlSaveOptions.setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) а также[HtmlSaveOptions.getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [HtmlSaveOptions.setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) характеристики.

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Возвращает:**
java.lang.String — имя файла (без пути), в котором будет сохранен шрифт.
### getFontStream() {#getFontStream--}
```
public OutputStream getFontStream()
```




**Возвращает:**
java.io.OutputStream
### getItalic() {#getItalic--}
```
public boolean getItalic()
```


Указывает, является ли текущий шрифт курсивом.

**Возвращает:**
boolean - соответствующее логическое значение.
### getKeepFontStreamOpen() {#getKeepFontStreamOpen--}
```
public boolean getKeepFontStreamOpen()
```


Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения шрифта.

 По умолчанию установлено значение false, и Aspose.Words закроет поток, указанный вами в**P:Aspose.Words.Saving.FontSavingArgs.FontStream** свойство после записи в него шрифта. Укажите значение true, чтобы поток оставался открытым.

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Возвращает:**
boolean - соответствующее логическое значение.
### getOriginalFileName() {#getOriginalFileName--}
```
public String getOriginalFileName()
```


Получает исходное имя файла шрифта с расширением.

Это свойство содержит исходное имя файла текущего шрифта, если оно известно. В противном случае это может быть пустая строка.

**Возвращает:**
java.lang.String — исходное имя файла шрифта с расширением.
### getOriginalFileSize() {#getOriginalFileSize--}
```
public int getOriginalFileSize()
```


Получает исходный размер файла шрифта.

Это свойство содержит исходный размер файла текущего шрифта, если он известен. В противном случае он может быть равен нулю.

**Возвращает:**
int - Исходный размер файла шрифта.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isExportNeeded() {#isExportNeeded--}
```
public boolean isExportNeeded()
```


Позволяет указать, будет ли текущий шрифт экспортироваться как ресурс шрифта. По умолчанию верно.

**Возвращает:**
boolean - соответствующее логическое значение.
### isExportNeeded(boolean value) {#isExportNeeded-boolean-}
```
public void isExportNeeded(boolean value)
```


Позволяет указать, будет ли текущий шрифт экспортироваться как ресурс шрифта. По умолчанию верно.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### isSubsettingNeeded() {#isSubsettingNeeded--}
```
public boolean isSubsettingNeeded()
```


Позволяет указать, будет ли текущий шрифт подмножаться перед экспортом в качестве ресурса шрифта.

Шрифты можно экспортировать как полные исходные файлы шрифтов или подмножества, чтобы включить только символы, которые используются в документе. Подмножество позволяет уменьшить результирующий размер ресурса шрифта.

 По умолчанию Aspose.Words решает, выполнять ли подмножество или нет, сравнивая исходный размер файла шрифта с размером, указанным в[HtmlSaveOptions.getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions\#getFontResourcesSubsettingSizeThreshold--) / [HtmlSaveOptions.setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions\#setFontResourcesSubsettingSizeThreshold-int-) . Вы можете переопределить это поведение для отдельных шрифтов, установив[isSubsettingNeeded()](../../com.aspose.words/fontsavingargs\#isSubsettingNeeded--) / [isSubsettingNeeded(boolean)](../../com.aspose.words/fontsavingargs\#isSubsettingNeeded-boolean-) имущество.

**Возвращает:**
boolean - соответствующее логическое значение.
### isSubsettingNeeded(boolean value) {#isSubsettingNeeded-boolean-}
```
public void isSubsettingNeeded(boolean value)
```


Позволяет указать, будет ли текущий шрифт подмножаться перед экспортом в качестве ресурса шрифта.

Шрифты можно экспортировать как полные исходные файлы шрифтов или подмножества, чтобы включить только символы, которые используются в документе. Подмножество позволяет уменьшить результирующий размер ресурса шрифта.

 По умолчанию Aspose.Words решает, выполнять ли подмножество или нет, сравнивая исходный размер файла шрифта с размером, указанным в[HtmlSaveOptions.getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions\#getFontResourcesSubsettingSizeThreshold--) / [HtmlSaveOptions.setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions\#setFontResourcesSubsettingSizeThreshold-int-) . Вы можете переопределить это поведение для отдельных шрифтов, установив[isSubsettingNeeded()](../../com.aspose.words/fontsavingargs\#isSubsettingNeeded--) / [isSubsettingNeeded(boolean)](../../com.aspose.words/fontsavingargs\#isSubsettingNeeded-boolean-) имущество.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setFontFileName(String value) {#setFontFileName-java.lang.String-}
```
public void setFontFileName(String value)
```


Устанавливает имя файла (без пути), в котором будет сохранен шрифт.

Это свойство позволяет переопределить способ генерации имен файлов шрифтов при экспорте в HTML.

Когда событие запускается, это свойство содержит имя файла, созданное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить шрифт в другой файл. Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого встроенного шрифта при экспорте в формат HTML. Способ генерации имени файла шрифта зависит от того, сохраняете ли вы документ в файл или в поток.

При сохранении документа в файл сгенерированное имя файла шрифта выглядит так:*..*.

 При сохранении документа в поток сгенерированное имя файла шрифта выглядит так:*Aspose.Words...*.

[getFontFileName()](../../com.aspose.words/fontsavingargs\#getFontFileName--) / [setFontFileName(java.lang.String)](../../com.aspose.words/fontsavingargs\#setFontFileName-java.lang.String-) должен содержать только имя файла без пути. Aspose.Words определяет путь для сохранения по имени файла документа,[HtmlSaveOptions.getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [HtmlSaveOptions.setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) а также[HtmlSaveOptions.getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [HtmlSaveOptions.setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) характеристики.

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя файла (без пути), в котором будет сохранен шрифт. |

### setFontStream(OutputStream value) {#setFontStream-java.io.OutputStream-}
```
public void setFontStream(OutputStream value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.io.OutputStream |  |

### setKeepFontStreamOpen(boolean value) {#setKeepFontStreamOpen-boolean-}
```
public void setKeepFontStreamOpen(boolean value)
```


Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения шрифта.

 По умолчанию установлено значение false, и Aspose.Words закроет поток, указанный вами в**P:Aspose.Words.Saving.FontSavingArgs.FontStream** свойство после записи в него шрифта. Укажите значение true, чтобы поток оставался открытым.

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
