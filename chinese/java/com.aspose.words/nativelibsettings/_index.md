---
title: "NativeLibSettings"
linktitle: "NativeLibSettings"
second_title: "Aspose.Words for Java"
description: "此类用于设置各种选项，例如 Aspose.Words 本机库的临时文件夹以及是否在 Java 中加载和使用本机库。"
type: docs
weight: 475
url: /zh/java/com.aspose.words/nativelibsettings/
---

**Inheritance:**
java.lang.Object
```
public class NativeLibSettings
```

此类用于设置各种选项，例如 Aspose.Words 本机库的临时文件夹以及是否加载和使用本机库。
## 方法

| 方法 | 描述 |
| --- | --- |
| [clearAsposeNativeTmpDirectory()](#clearAsposeNativeTmpDirectory) | 清除存放 Aspose 临时库的目录。 |
| [getInterruptThreadIfImageExceptionThrown()](#getInterruptThreadIfImageExceptionThrown) | 返回控制图像异常时线程中断的属性的当前值。 |
| [getTmpDirectoryPath()](#getTmpDirectoryPath) | 返回本机库临时目录的路径。 |
| [getUseJAIImageRendering()](#getUseJAIImageRendering) | 获取一个值，用于确定在渲染文档图像时是否使用 JAI（Java Advanced Imaging）。 |
| [isHarfBuzzNativeLibLoaded()](#isHarfBuzzNativeLibLoaded) | 如果已加载 HarfBuzz 库，则返回 `true`。 |
| [isWinNativeLibLoaded()](#isWinNativeLibLoaded) | 如果已加载 WindowsNativeCall 库，则返回 `true`。 |
| [loadHarfBuzzNativeLib()](#loadHarfBuzzNativeLib) | 设置加载并使用 harfbuzz-shaping-engine-dll.dll 库。 |
| [loadWinNativeLib()](#loadWinNativeLib) | Sets to load and use WindowsNativeCall\_x86 | \_x64.dll 库。 |
| [setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)](#setInterruptThreadIfImageExceptionThrown-boolean) | 设置定义处理图像异常时行为的属性。 |
| [setTmpDirectoryPath(String path)](#setTmpDirectoryPath-java.lang.String) | 指定本机库临时目录的路径。 |
| [setUseJAIImageRendering(boolean useJAIImageRendering)](#setUseJAIImageRendering-boolean) | 设置一个值，以确定在渲染文档图像时是否使用 JAI（Java Advanced Imaging）。 |
| [skipHarfBuzzNativeLib()](#skipHarfBuzzNativeLib) | 跳过加载并使用 harfbuzz-shaping-engine-dll.dll 库。 |
| [skipWinNativeLib()](#skipWinNativeLib) | Skip loading and use WindowsNativeCall\_x86 | \_x64.dll 库。 |
### clearAsposeNativeTmpDirectory() {#clearAsposeNativeTmpDirectory}
```
public static void clearAsposeNativeTmpDirectory()
```


清除存放 Aspose 临时库的目录。

### getInterruptThreadIfImageExceptionThrown() {#getInterruptThreadIfImageExceptionThrown}
```
public static boolean getInterruptThreadIfImageExceptionThrown()
```


返回控制图像异常时线程中断的属性的当前值。

**Remarks:**

默认值为 `false`。

**Returns:**
boolean - 线程在图像异常时是否应被中断。
### getTmpDirectoryPath() {#getTmpDirectoryPath}
```
public static String getTmpDirectoryPath()
```


返回本机库临时目录的路径。

**Returns:**
java.lang.String
### getUseJAIImageRendering() {#getUseJAIImageRendering}
```
public static boolean getUseJAIImageRendering()
```


获取一个值，以确定在渲染文档图像时是否使用 JAI（Java Advanced Imaging）。在某些情况下，这可能提升性能。

**Remarks:**

默认值为 `true`。

只有在如 [here][] 所述将 JAI 包含为依赖时才会使用 JAI。如果禁用 JAI，某些图像可能无法正确渲染。


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Returns:**
boolean - 是否使用 JAI。
### isHarfBuzzNativeLibLoaded() {#isHarfBuzzNativeLibLoaded}
```
public static boolean isHarfBuzzNativeLibLoaded()
```


如果已加载 HarfBuzz 库，则返回 `true`。默认情况下，会加载本机库。

**Returns:**
boolean
### isWinNativeLibLoaded() {#isWinNativeLibLoaded}
```
public static boolean isWinNativeLibLoaded()
```


如果已加载 WindowsNativeCall 库，则返回 `true`。默认情况下，会加载本机库。

**Returns:**
boolean
### loadHarfBuzzNativeLib() {#loadHarfBuzzNativeLib}
```
public static void loadHarfBuzzNativeLib()
```


设置加载并使用 harfbuzz-shaping-engine-dll.dll 库。默认情况下，会加载本机库。

### loadWinNativeLib() {#loadWinNativeLib}
```
public static void loadWinNativeLib()
```


设置加载并使用 WindowsNativeCall\_x86|\_x64.dll 库。默认情况下，会加载本机库。

### setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown) {#setInterruptThreadIfImageExceptionThrown-boolean}
```
public static void setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)
```


设置定义处理图像异常时行为的属性。如果该属性设置为 true，则在图像处理期间发生异常时，执行线程将被中断。

**Remarks:**

默认值为 `false`。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| abortSavingIfImageExceptionThrown | boolean | true - 在图像异常时中断线程，false - 不中断 |

### setTmpDirectoryPath(String path) {#setTmpDirectoryPath-java.lang.String}
```
public static void setTmpDirectoryPath(String path)
```


指定本机库临时目录的路径。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 路径 | java.lang.String | 本机库临时目录的路径。 |

### setUseJAIImageRendering(boolean useJAIImageRendering) {#setUseJAIImageRendering-boolean}
```
public static void setUseJAIImageRendering(boolean useJAIImageRendering)
```


设置一个值，以确定在渲染文档图像时是否使用 JAI（Java Advanced Imaging）。在某些情况下，这可能提升性能。

**Remarks:**

默认值为 `true`。

只有在如 [here][] 所述将 JAI 包含为依赖时才会使用 JAI。如果禁用 JAI，某些图像可能无法正确渲染。


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| useJAIImageRendering | boolean | 是否有必要使用 JAI。 |

### skipHarfBuzzNativeLib() {#skipHarfBuzzNativeLib}
```
public static void skipHarfBuzzNativeLib()
```


跳过加载并使用 harfbuzz-shaping-engine-dll.dll 库。默认情况下，会加载本机库。

### skipWinNativeLib() {#skipWinNativeLib}
```
public static void skipWinNativeLib()
```


跳过加载并使用 WindowsNativeCall\_x86|\_x64.dll 库。默认情况下，会加载本机库。

