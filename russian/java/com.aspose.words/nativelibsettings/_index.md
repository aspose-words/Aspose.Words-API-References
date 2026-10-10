---
title: "NativeLibSettings"
linktitle: "NativeLibSettings"
second_title: "Aspose.Words для Java"
description: "Этот класс помогает задавать различные параметры, такие как временная папка для нативных библиотек Aspose.Words и то, должны ли нативные библиотеки загружаться и использоваться в Java."
type: docs
weight: 475
url: /ru/java/com.aspose.words/nativelibsettings/
---

**Inheritance:**
java.lang.Object
```
public class NativeLibSettings
```

Этот класс помогает установить различные параметры, такие как временная папка для нативных библиотек Aspose.Words и то, должны ли нативные библиотеки загружаться и использоваться.
## Методы

| Метод | Описание |
| --- | --- |
| [clearAsposeNativeTmpDirectory()](#clearAsposeNativeTmpDirectory) | Очищает каталог, в котором хранятся временные библиотеки Aspose. |
| [getInterruptThreadIfImageExceptionThrown()](#getInterruptThreadIfImageExceptionThrown) | Возвращает текущее значение свойства, контролирующего прерывание потока при исключениях изображений. |
| [getTmpDirectoryPath()](#getTmpDirectoryPath) | Возвращает путь к временной папке нативных библиотек. |
| [getUseJAIImageRendering()](#getUseJAIImageRendering) | Получает значение, определяющее, используется ли JAI (Java Advanced Imaging) при рендеринге изображений документа. |
| [isHarfBuzzNativeLibLoaded()](#isHarfBuzzNativeLibLoaded) | Возвращает `true`, если библиотеки HarfBuzz загружены. |
| [isWinNativeLibLoaded()](#isWinNativeLibLoaded) | Возвращает `true`, если библиотеки WindowsNativeCall загружены. |
| [loadHarfBuzzNativeLib()](#loadHarfBuzzNativeLib) | Устанавливает загрузку и использование библиотек harfbuzz-shaping-engine-dll.dll. |
| [loadWinNativeLib()](#loadWinNativeLib) | Sets to load and use WindowsNativeCall\_x86 | \_x64.dll библиотеки. |
| [setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)](#setInterruptThreadIfImageExceptionThrown-boolean) | Устанавливает свойство, определяющее поведение при обработке исключений изображений. |
| [setTmpDirectoryPath(String path)](#setTmpDirectoryPath-java.lang.String) | Указывает путь к временной папке нативных библиотек. |
| [setUseJAIImageRendering(boolean useJAIImageRendering)](#setUseJAIImageRendering-boolean) | Устанавливает значение, определяющее, используется ли JAI (Java Advanced Imaging) при рендеринге изображений документа. |
| [skipHarfBuzzNativeLib()](#skipHarfBuzzNativeLib) | Пропустить загрузку и использовать библиотеки harfbuzz-shaping-engine-dll.dll. |
| [skipWinNativeLib()](#skipWinNativeLib) | Skip loading and use WindowsNativeCall\_x86 | \_x64.dll библиотеки. |
### clearAsposeNativeTmpDirectory() {#clearAsposeNativeTmpDirectory}
```
public static void clearAsposeNativeTmpDirectory()
```


Очищает каталог, в котором хранятся временные библиотеки Aspose.

### getInterruptThreadIfImageExceptionThrown() {#getInterruptThreadIfImageExceptionThrown}
```
public static boolean getInterruptThreadIfImageExceptionThrown()
```


Возвращает текущее значение свойства, контролирующего прерывание потока при исключениях изображений.

**Remarks:**

Значение по умолчанию — `false`.

**Returns:**
boolean — должно ли поток прерываться при исключениях изображений.
### getTmpDirectoryPath() {#getTmpDirectoryPath}
```
public static String getTmpDirectoryPath()
```


Возвращает путь к временной папке нативных библиотек.

**Returns:**
java.lang.String
### getUseJAIImageRendering() {#getUseJAIImageRendering}
```
public static boolean getUseJAIImageRendering()
```


Получает значение, определяющее, используется ли JAI (Java Advanced Imaging) при рендеринге изображений документа. В некоторых случаях это может улучшить производительность.

**Remarks:**

Значение по умолчанию — `true`.

JAI будет использоваться только в случае включения его в зависимости, как описано [здесь][]. Некоторые изображения могут отображаться некорректно, если JAI отключён.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Returns:**
boolean — используется ли JAI.
### isHarfBuzzNativeLibLoaded() {#isHarfBuzzNativeLibLoaded}
```
public static boolean isHarfBuzzNativeLibLoaded()
```


Возвращает `true`, если библиотеки HarfBuzz загружены. По умолчанию нативные библиотеки загружаются.

**Returns:**
boolean
### isWinNativeLibLoaded() {#isWinNativeLibLoaded}
```
public static boolean isWinNativeLibLoaded()
```


Возвращает `true`, если библиотеки WindowsNativeCall загружены. По умолчанию нативные библиотеки загружаются.

**Returns:**
boolean
### loadHarfBuzzNativeLib() {#loadHarfBuzzNativeLib}
```
public static void loadHarfBuzzNativeLib()
```


Устанавливает загрузку и использование библиотек harfbuzz-shaping-engine-dll.dll. По умолчанию нативные библиотеки загружаются.

### loadWinNativeLib() {#loadWinNativeLib}
```
public static void loadWinNativeLib()
```


Устанавливает загрузку и использование библиотек WindowsNativeCall\_x86|\_x64.dll. По умолчанию нативные библиотеки загружаются.

### setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown) {#setInterruptThreadIfImageExceptionThrown-boolean}
```
public static void setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)
```


Устанавливает свойство, определяющее поведение при обработке исключений изображений. Если свойство установлено в true, поток выполнения будет прерван при возникновении исключения во время обработки изображения.

**Remarks:**

Значение по умолчанию — `false`.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| abortSavingIfImageExceptionThrown | boolean | true - прервать поток при исключениях изображений, false - не прерывать |

### setTmpDirectoryPath(String path) {#setTmpDirectoryPath-java.lang.String}
```
public static void setTmpDirectoryPath(String path)
```


Указывает путь к временной папке нативных библиотек.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| path | java.lang.String | путь к временной директории нативных библиотек. |

### setUseJAIImageRendering(boolean useJAIImageRendering) {#setUseJAIImageRendering-boolean}
```
public static void setUseJAIImageRendering(boolean useJAIImageRendering)
```


Устанавливает значение, определяющее, используется ли JAI (Java Advanced Imaging) при рендеринге изображений документов. В некоторых случаях это может улучшить производительность.

**Remarks:**

Значение по умолчанию — `true`.

JAI будет использоваться только в случае включения его в зависимости, как описано [здесь][]. Некоторые изображения могут отображаться некорректно, если JAI отключён.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| useJAIImageRendering | boolean | необходимо ли использовать JAI. |

### skipHarfBuzzNativeLib() {#skipHarfBuzzNativeLib}
```
public static void skipHarfBuzzNativeLib()
```


Пропустить загрузку и использовать библиотеки harfbuzz-shaping-engine-dll.dll. По умолчанию нативные библиотеки загружаются.

### skipWinNativeLib() {#skipWinNativeLib}
```
public static void skipWinNativeLib()
```


Пропустить загрузку и использовать библиотеки WindowsNativeCall\_x86|\_x64.dll. По умолчанию нативные библиотеки загружаются.

