---
title: DocSaveOptions
second_title: Справочник по API Aspose.Words для Java
description: Может использоваться для указания дополнительных параметров при сохранении документа в формате или.
type: docs
weight: 119
url: /ru/java/com.aspose.words/docsaveoptions/
---

**Наследование:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions)
```
public class DocSaveOptions extends SaveOptions
```

 Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.DOC](../../com.aspose.words/saveformat\#DOC) или же[SaveFormat.DOT](../../com.aspose.words/saveformat\#DOT) формат.

 Чтобы узнать больше, посетите**Specify Save Options** документальная статья.

 На данный момент предоставляет только[getSaveFormat()](../../com.aspose.words/docsaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/docsaveoptions\#setSaveFormat-int-) свойство, но в будущем будут добавлены другие параметры, такие как пароль шифрования или настройки цифровой подписи.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DocSaveOptions()](#DocSaveOptions--) |  Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в[SaveFormat.DOC](../../com.aspose.words/saveformat\#DOC) формат. |
| [DocSaveOptions(int saveFormat)](#DocSaveOptions-int-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int-) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String-) | Создает объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts--) | Получает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. |
| [getAlwaysCompressMetafiles()](#getAlwaysCompressMetafiles--) | При значении false небольшие метафайлы не сжимаются из соображений производительности. |
| [getClass()](#getClass--) |  |
| [getDefaultTemplate()](#getDefaultTemplate--) | Получает путь к шаблону по умолчанию (включая имя файла). |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode--) | Получает значение, определяющее способ визуализации 3D-эффектов. |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode--) | Получает значение, определяющее способ визуализации эффектов DrawingML. |
| [getDmlRenderingMode()](#getDmlRenderingMode--) | Получает значение, определяющее способ отображения фигур DrawingML. |
| [getExportGeneratorName()](#getExportGeneratorName--) | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. |
| [getImlRenderingMode()](#getImlRenderingMode--) | Получает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [getMemoryOptimization()](#getMemoryOptimization--) | Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. |
| [getPassword()](#getPassword--) | Получает/устанавливает пароль для шифрования документа с использованием метода шифрования RC4. |
| [getPrettyFormat()](#getPrettyFormat--) | Когда true , красивые форматы выводятся там, где это применимо. |
| [getProgressCallback()](#getProgressCallback--) | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| [getSaveFormat()](#getSaveFormat--) | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. |
| [getSavePictureBullet()](#getSavePictureBullet--) | При значении false данные PictureBullet не сохраняются в выходной документ. |
| [getSaveRoutingSlip()](#getSaveRoutingSlip--) | При значении false данные RoutingSlip не сохраняются в выходной документ. |
| [getTempFolder()](#getTempFolder--) | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty--) |  Получает значение, определяющее, является ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [getUpdateFields()](#getUpdateFields--) | Получает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty--) |  Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением. |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty--) |  Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [getUpdateSdtContent()](#getUpdateSdtContent--) |  Получает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. |
| [getUseAntiAliasing()](#getUseAntiAliasing--) | Получает значение, определяющее, следует ли использовать сглаживание для рендеринга. |
| [getUseHighQualityRendering()](#getUseHighQualityRendering--) | Получает значение, определяющее, следует ли использовать высокое качество (т. е. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean-) | Задает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. |
| [setAlwaysCompressMetafiles(boolean value)](#setAlwaysCompressMetafiles-boolean-) | При значении false небольшие метафайлы не сжимаются из соображений производительности. |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String-) | Устанавливает путь к шаблону по умолчанию (включая имя файла). |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int-) | Задает значение, определяющее способ визуализации 3D-эффектов. |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int-) | Задает значение, определяющее, как визуализируются эффекты DrawingML. |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int-) | Задает значение, определяющее, как отображаются фигуры DrawingML. |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean-) | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int-) | Задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean-) | Задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. |
| [setPassword(String value)](#setPassword-java.lang.String-) | Получает/устанавливает пароль для шифрования документа с использованием метода шифрования RC4. |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean-) | Когда true , красивые форматы выводятся там, где это применимо. |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback-) | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. |
| [setSavePictureBullet(boolean value)](#setSavePictureBullet-boolean-) | При значении false данные PictureBullet не сохраняются в выходной документ. |
| [setSaveRoutingSlip(boolean value)](#setSaveRoutingSlip-boolean-) | При значении false данные RoutingSlip не сохраняются в выходной документ. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String-) | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean-) |  Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean-) | Задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean-) |  Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением. |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean-) |  Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [setUpdateSdtContent(boolean value)](#setUpdateSdtContent-boolean-) |  Устанавливает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean-) | Задает значение, определяющее, следует ли использовать сглаживание для рендеринга. |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean-) | Устанавливает значение, определяющее, использовать ли высокое качество (т.е. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DocSaveOptions() {#DocSaveOptions--}
```
public DocSaveOptions()
```


 Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в[SaveFormat.DOC](../../com.aspose.words/saveformat\#DOC) формат.

### DocSaveOptions(int saveFormat) {#DocSaveOptions-int-}
```
public DocSaveOptions(int saveFormat)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | int |  |

### createSaveOptions(int saveFormat) {#createSaveOptions-int-}
```
public static SaveOptions createSaveOptions(int saveFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | int |  |

**Возвращает:**
[SaveOptions](../../com.aspose.words/saveoptions)
### createSaveOptions(String fileName) {#createSaveOptions-java.lang.String-}
```
public static SaveOptions createSaveOptions(String fileName)
```


Создает объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Расширение этого имени файла определяет класс создаваемого объекта параметров сохранения. |

**Возвращает:**
[SaveOptions](../../com.aspose.words/saveoptions) - Объект класса, производного от[SaveOptions](../../com.aspose.words/saveoptions).
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
### getAllowEmbeddingPostScriptFonts() {#getAllowEmbeddingPostScriptFonts--}
```
public boolean getAllowEmbeddingPostScriptFonts()
```


Получает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию**false**.

Обратите внимание: Word не встраивает шрифты PostScript, но может открывать документы со встроенными шрифтами этого типа.

 Этот вариант работает только тогда, когда[FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) принадлежащий[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--) свойство имеет значение true .

**Возвращает:**
boolean — логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения.
### getAlwaysCompressMetafiles() {#getAlwaysCompressMetafiles--}
```
public boolean getAlwaysCompressMetafiles()
```


 При значении false небольшие метафайлы не сжимаются из соображений производительности. Значение по умолчанию**true**, все метафайлы сжимаются независимо от их размера.

**Возвращает:**
boolean - соответствующее логическое значение.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDefaultTemplate() {#getDefaultTemplate--}
```
public String getDefaultTemplate()
```


 Получает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства**empty string** . Если указано, этот путь используется для загрузки шаблона, когда[Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-) правда, но[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) пустой.

**Возвращает:**
java.lang.String — путь к шаблону по умолчанию (включая имя файла).
### getDml3DEffectsRenderingMode() {#getDml3DEffectsRenderingMode--}
```
public int getDml3DEffectsRenderingMode()
```


Получает значение, определяющее способ визуализации 3D-эффектов. Значение по умолчанию[Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC).

**Возвращает:**
 int — значение, определяющее, как визуализируются 3D-эффекты. Возвращаемое значение является одним из[Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode) константы.
### getDmlEffectsRenderingMode() {#getDmlEffectsRenderingMode--}
```
public int getDmlEffectsRenderingMode()
```


 Получает значение, определяющее способ визуализации эффектов DrawingML. Значение по умолчанию[DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Возвращает:**
 int — значение, определяющее, как визуализируются эффекты DrawingML. Возвращаемое значение является одним из[DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode) константы.
### getDmlRenderingMode() {#getDmlRenderingMode--}
```
public int getDmlRenderingMode()
```


 Получает значение, определяющее способ отображения фигур DrawingML. Значение по умолчанию[DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode\#FALLBACK).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Возвращает:**
 int — значение, определяющее способ отображения фигур DrawingML. Возвращаемое значение является одним из[DmlRenderingMode](../../com.aspose.words/dmlrenderingmode) константы.
### getExportGeneratorName() {#getExportGeneratorName--}
```
public boolean getExportGeneratorName()
```


 При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию**true**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getImlRenderingMode() {#getImlRenderingMode--}
```
public int getImlRenderingMode()
```


 Получает значение, определяющее способ визуализации объектов рукописного ввода (InkML). Значение по умолчанию[ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Возвращает:**
 int — значение, определяющее способ отображения объектов рукописного ввода (InkML). Возвращаемое значение является одним из[ImlRenderingMode](../../com.aspose.words/imlrenderingmode) константы.
### getMemoryOptimization() {#getMemoryOptimization--}
```
public boolean getMemoryOptimization()
```


Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства**false**. Установка для этого параметра значения true может значительно снизить потребление памяти при сохранении больших документов за счет замедления времени сохранения.

**Возвращает:**
boolean — значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа.
### getPassword() {#getPassword--}
```
public String getPassword()
```


Получает/устанавливает пароль для шифрования документа с использованием метода шифрования RC4.

Чтобы сохранить документ без шифрования, это свойство должно иметь значение null или пустую строку.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getPrettyFormat() {#getPrettyFormat--}
```
public boolean getPrettyFormat()
```


 Когда true , красивые форматы выводятся там, где это применимо. Значение по умолчанию**false**.

 Установлен в**true** чтобы сделать вывод HTML, MHTML, EPUB, WordML, RTF, DOCX и ODT удобочитаемым для человека. Полезно для тестирования или отладки.

**Возвращает:**
boolean - соответствующее логическое значение.
### getProgressCallback() {#getProgressCallback--}
```
public IDocumentSavingCallback getProgressCallback()
```


Вызывается при сохранении документа и принимает данные о ходе сохранения.

 Прогресс сообщается при сохранении в[SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW) , или же[SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat\#XAML-FLOW-PACK).

**Возвращает:**
[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) - соответствующий[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) ценность.
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


 Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть[SaveFormat.DOC](../../com.aspose.words/saveformat\#DOC) или же[SaveFormat.DOT](../../com.aspose.words/saveformat\#DOT).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[SaveFormat](../../com.aspose.words/saveformat) константы.
### getSavePictureBullet() {#getSavePictureBullet--}
```
public boolean getSavePictureBullet()
```


 При значении false данные PictureBullet не сохраняются в выходной документ. Значение по умолчанию**true**.

Этот параметр предусмотрен для Word 97, который не может корректно работать с данными PictureBullet. Чтобы удалить данные PictureBullet, установите для параметра значение «false».

**Возвращает:**
boolean - соответствующее логическое значение.
### getSaveRoutingSlip() {#getSaveRoutingSlip--}
```
public boolean getSaveRoutingSlip()
```


 При значении false данные RoutingSlip не сохраняются в выходной документ. Значение по умолчанию**true**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getTempFolder() {#getTempFolder--}
```
public String getTempFolder()
```


Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство имеет значение null, и временные файлы не используются.

Когда Aspose.Words сохраняет документ, ему необходимо создать временные внутренние структуры. По умолчанию эти внутренние структуры создаются в памяти, и использование памяти резко возрастает в течение короткого периода времени, пока документ сохраняется. Когда сохранение завершено, память освобождается и утилизируется сборщиком мусора.

 Если вы сохраняете очень большой документ (тысячи страниц) и/или обрабатываете много документов одновременно, скачок памяти во время сохранения может быть достаточно значительным, чтобы система выдала исключение java.lang.IndexOutOfBoundsException. Указание временной папки с помощью[getTempFolder()](../../com.aspose.words/saveoptions\#getTempFolder--) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions\#setTempFolder-java.lang.String-)приведет к тому, что Aspose.Words будет хранить внутренние структуры во временных файлах, а не в памяти. Это уменьшает использование памяти во время сохранения, но снижает производительность сохранения.

Папка должна существовать и быть доступной для записи, иначе будет выдано исключение.

Aspose.Words автоматически удаляет все временные файлы после завершения сохранения.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getUpdateCreatedTimeProperty() {#getUpdateCreatedTimeProperty--}
```
public boolean getUpdateCreatedTimeProperty()
```


 Получает значение, определяющее, является ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. Значение по умолчанию — ложь;

**Возвращает:**
 boolean - Значение, определяющее, является ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением.
### getUpdateFields() {#getUpdateFields--}
```
public boolean getUpdateFields()
```


 Получает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства**true**. Позволяет указать, следует ли имитировать поведение MS Word.

**Возвращает:**
boolean — значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы.
### getUpdateLastPrintedProperty() {#getUpdateLastPrintedProperty--}
```
public boolean getUpdateLastPrintedProperty()
```


 Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением.

**Возвращает:**
 boolean - Значение, определяющее, является ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением.
### getUpdateLastSavedTimeProperty() {#getUpdateLastSavedTimeProperty--}
```
public boolean getUpdateLastSavedTimeProperty()
```


 Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением.

**Возвращает:**
 boolean - Значение, определяющее, является ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением.
### getUpdateSdtContent() {#getUpdateSdtContent--}
```
public boolean getUpdateSdtContent()
```


 Получает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. Значение по умолчанию неверно .

**Возвращает:**
 boolean — значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением.
### getUseAntiAliasing() {#getUseAntiAliasing--}
```
public boolean getUseAntiAliasing()
```


Получает значение, определяющее, следует ли использовать сглаживание для рендеринга.

Значение по умолчанию неверно . Когда для этого значения установлено значение true, для рендеринга используется сглаживание.

Это свойство используется, когда документ экспортируется в следующие форматы:[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF) . Когда документ экспортируется в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) а также[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) форматы эта опция используется для растровых изображений.

**Возвращает:**
логическое значение — значение, определяющее, следует ли использовать сглаживание для рендеринга.
### getUseHighQualityRendering() {#getUseHighQualityRendering--}
```
public boolean getUseHighQualityRendering()
```


Получает значение, определяющее, следует ли использовать высококачественные (то есть медленные) алгоритмы рендеринга. Значение по умолчанию неверно .

 Это свойство используется, когда документ экспортируется в форматы изображений:[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**Возвращает:**
логическое значение — значение, определяющее, следует ли использовать высокое качество (т.е.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAllowEmbeddingPostScriptFonts(boolean value) {#setAllowEmbeddingPostScriptFonts-boolean-}
```
public void setAllowEmbeddingPostScriptFonts(boolean value)
```


 Задает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию**false**.

Обратите внимание: Word не встраивает шрифты PostScript, но может открывать документы со встроенными шрифтами этого типа.

 Этот вариант работает только тогда, когда[FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) принадлежащий[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--) свойство имеет значение true .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. |

### setAlwaysCompressMetafiles(boolean value) {#setAlwaysCompressMetafiles-boolean-}
```
public void setAlwaysCompressMetafiles(boolean value)
```


 При значении false небольшие метафайлы не сжимаются из соображений производительности. Значение по умолчанию**true**, все метафайлы сжимаются независимо от их размера.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDefaultTemplate(String value) {#setDefaultTemplate-java.lang.String-}
```
public void setDefaultTemplate(String value)
```


 Устанавливает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства**empty string** . Если указано, этот путь используется для загрузки шаблона, когда[Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-) правда, но[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) пустой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Путь к шаблону по умолчанию (включая имя файла). |

### setDml3DEffectsRenderingMode(int value) {#setDml3DEffectsRenderingMode-int-}
```
public void setDml3DEffectsRenderingMode(int value)
```


 Задает значение, определяющее способ визуализации 3D-эффектов. Значение по умолчанию[Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее способ визуализации 3D-эффектов. Значение должно быть одним из[Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode) константы. |

### setDmlEffectsRenderingMode(int value) {#setDmlEffectsRenderingMode-int-}
```
public void setDmlEffectsRenderingMode(int value)
```


 Задает значение, определяющее, как визуализируются эффекты DrawingML. Значение по умолчанию[DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее, как визуализируются эффекты DrawingML. Значение должно быть одним из[DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode) константы. |

### setDmlRenderingMode(int value) {#setDmlRenderingMode-int-}
```
public void setDmlRenderingMode(int value)
```


 Задает значение, определяющее, как отображаются фигуры DrawingML. Значение по умолчанию[DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode\#FALLBACK).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее, как отображаются фигуры DrawingML. Значение должно быть одним из[DmlRenderingMode](../../com.aspose.words/dmlrenderingmode) константы. |

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean-}
```
public void setExportGeneratorName(boolean value)
```


 При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setImlRenderingMode(int value) {#setImlRenderingMode-int-}
```
public void setImlRenderingMode(int value)
```


 Задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). Значение по умолчанию[ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее способ визуализации объектов рукописного ввода (InkML). Значение должно быть одним из[ImlRenderingMode](../../com.aspose.words/imlrenderingmode) константы. |

### setMemoryOptimization(boolean value) {#setMemoryOptimization-boolean-}
```
public void setMemoryOptimization(boolean value)
```


 Задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства**false**. Установка для этого параметра значения true может значительно снизить потребление памяти при сохранении больших документов за счет замедления времени сохранения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. |

### setPassword(String value) {#setPassword-java.lang.String-}
```
public void setPassword(String value)
```


Получает/устанавливает пароль для шифрования документа с использованием метода шифрования RC4.

Чтобы сохранить документ без шифрования, это свойство должно иметь значение null или пустую строку.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setPrettyFormat(boolean value) {#setPrettyFormat-boolean-}
```
public void setPrettyFormat(boolean value)
```


 Когда true , красивые форматы выводятся там, где это применимо. Значение по умолчанию**false**.

 Установлен в**true** чтобы сделать вывод HTML, MHTML, EPUB, WordML, RTF, DOCX и ODT удобочитаемым для человека. Полезно для тестирования или отладки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setProgressCallback(IDocumentSavingCallback value) {#setProgressCallback-com.aspose.words.IDocumentSavingCallback-}
```
public void setProgressCallback(IDocumentSavingCallback value)
```


Вызывается при сохранении документа и принимает данные о ходе сохранения.

 Прогресс сообщается при сохранении в[SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW) , или же[SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat\#XAML-FLOW-PACK).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) |  Соответствующий[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) ценность. |

### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


 Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть[SaveFormat.DOC](../../com.aspose.words/saveformat\#DOC) или же[SaveFormat.DOT](../../com.aspose.words/saveformat\#DOT).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[SaveFormat](../../com.aspose.words/saveformat) константы. |

### setSavePictureBullet(boolean value) {#setSavePictureBullet-boolean-}
```
public void setSavePictureBullet(boolean value)
```


 При значении false данные PictureBullet не сохраняются в выходной документ. Значение по умолчанию**true**.

Этот параметр предусмотрен для Word 97, который не может корректно работать с данными PictureBullet. Чтобы удалить данные PictureBullet, установите для параметра значение «false».

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSaveRoutingSlip(boolean value) {#setSaveRoutingSlip-boolean-}
```
public void setSaveRoutingSlip(boolean value)
```


 При значении false данные RoutingSlip не сохраняются в выходной документ. Значение по умолчанию**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setTempFolder(String value) {#setTempFolder-java.lang.String-}
```
public void setTempFolder(String value)
```


Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство имеет значение null, и временные файлы не используются.

Когда Aspose.Words сохраняет документ, ему необходимо создать временные внутренние структуры. По умолчанию эти внутренние структуры создаются в памяти, и использование памяти резко возрастает в течение короткого периода времени, пока документ сохраняется. Когда сохранение завершено, память освобождается и утилизируется сборщиком мусора.

 Если вы сохраняете очень большой документ (тысячи страниц) и/или обрабатываете много документов одновременно, скачок памяти во время сохранения может быть достаточно значительным, чтобы система выдала исключение java.lang.IndexOutOfBoundsException. Указание временной папки с помощью[getTempFolder()](../../com.aspose.words/saveoptions\#getTempFolder--) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions\#setTempFolder-java.lang.String-)приведет к тому, что Aspose.Words будет хранить внутренние структуры во временных файлах, а не в памяти. Это уменьшает использование памяти во время сохранения, но снижает производительность сохранения.

Папка должна существовать и быть доступной для записи, иначе будет выдано исключение.

Aspose.Words автоматически удаляет все временные файлы после завершения сохранения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setUpdateCreatedTimeProperty(boolean value) {#setUpdateCreatedTimeProperty-boolean-}
```
public void setUpdateCreatedTimeProperty(boolean value)
```


 Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. Значение по умолчанию — ложь;

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Значение, определяющее, является ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. |

### setUpdateFields(boolean value) {#setUpdateFields-boolean-}
```
public void setUpdateFields(boolean value)
```


Задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства**true**. Позволяет указать, следует ли имитировать поведение MS Word.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. |

### setUpdateLastPrintedProperty(boolean value) {#setUpdateLastPrintedProperty-boolean-}
```
public void setUpdateLastPrintedProperty(boolean value)
```


 Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Значение, определяющее, является ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением. |

### setUpdateLastSavedTimeProperty(boolean value) {#setUpdateLastSavedTimeProperty-boolean-}
```
public void setUpdateLastSavedTimeProperty(boolean value)
```


 Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Значение, определяющее, является ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением. |

### setUpdateSdtContent(boolean value) {#setUpdateSdtContent-boolean-}
```
public void setUpdateSdtContent(boolean value)
```


 Устанавливает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Значение, определяющее, является ли содержание[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. |

### setUseAntiAliasing(boolean value) {#setUseAntiAliasing-boolean-}
```
public void setUseAntiAliasing(boolean value)
```


Задает значение, определяющее, следует ли использовать сглаживание для рендеринга.

Значение по умолчанию неверно . Когда для этого значения установлено значение true, для рендеринга используется сглаживание.

Это свойство используется, когда документ экспортируется в следующие форматы:[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF) . Когда документ экспортируется в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) а также[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) форматы эта опция используется для растровых изображений.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли использовать сглаживание для рендеринга. |

### setUseHighQualityRendering(boolean value) {#setUseHighQualityRendering-boolean-}
```
public void setUseHighQualityRendering(boolean value)
```


Устанавливает значение, определяющее, следует ли использовать высококачественные (т.е. медленные) алгоритмы рендеринга. Значение по умолчанию неверно .

 Это свойство используется, когда документ экспортируется в форматы изображений:[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли использовать высокое качество (т.е. |

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
