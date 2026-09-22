---
title: "NativeLibSettings"
linktitle: "NativeLibSettings"
second_title: "Aspose.Words لـ Java"
description: "هذه الفئة تساعد على ضبط خيارات مختلفة مثل المجلد المؤقت لمكتبات Aspose.Words الأصلية وما إذا كان يجب تحميل المكتبات الأصلية واستخدامها في Java."
type: docs
weight: 475
url: /ar/java/com.aspose.words/nativelibsettings/
---

**Inheritance:**
java.lang.Object
```
public class NativeLibSettings
```

تساعد هذه الفئة في تعيين خيارات مختلفة مثل المجلد المؤقت لمكتبات Aspose.Words الأصلية وما إذا كان يجب تحميل المكتبات الأصلية واستخدامها.
## الطرق

| طريقة | الوصف |
| --- | --- |
| [clearAsposeNativeTmpDirectory()](#clearAsposeNativeTmpDirectory) | يمسح الدليل الذي تُخزن فيه مكتبات Aspose المؤقتة. |
| [getInterruptThreadIfImageExceptionThrown()](#getInterruptThreadIfImageExceptionThrown) | يعيد القيمة الحالية للخاصية التي تتحكم في مقاطعة الخيط عند استثناءات الصورة. |
| [getTmpDirectoryPath()](#getTmpDirectoryPath) | إرجاع المسار إلى الدليل المؤقت للمكتبات الأصلية. |
| [getUseJAIImageRendering()](#getUseJAIImageRendering) | يحصل على قيمة تحدد ما إذا كان يتم استخدام JAI (Java Advanced Imaging) أثناء عرض صور المستند. |
| [isHarfBuzzNativeLibLoaded()](#isHarfBuzzNativeLibLoaded) | يعيد `true` إذا تم تحميل مكتبات HarfBuzz. |
| [isWinNativeLibLoaded()](#isWinNativeLibLoaded) | يعيد `true` إذا تم تحميل مكتبات WindowsNativeCall. |
| [loadHarfBuzzNativeLib()](#loadHarfBuzzNativeLib) | يضبط لتحميل واستخدام مكتبات harfbuzz-shaping-engine-dll.dll. |
| [loadWinNativeLib()](#loadWinNativeLib) | Sets to load and use WindowsNativeCall\_x86 | \_x64.dll libraries. |
| [setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)](#setInterruptThreadIfImageExceptionThrown-boolean) | يضبط الخاصية التي تحدد السلوك عند معالجة استثناءات الصورة. |
| [setTmpDirectoryPath(String path)](#setTmpDirectoryPath-java.lang.String) | يحدد المسار إلى الدليل المؤقت للمكتبات الأصلية. |
| [setUseJAIImageRendering(boolean useJAIImageRendering)](#setUseJAIImageRendering-boolean) | يضبط قيمة تحدد ما إذا كان يتم استخدام JAI (Java Advanced Imaging) أثناء عرض صور المستند. |
| [skipHarfBuzzNativeLib()](#skipHarfBuzzNativeLib) | تخطي التحميل واستخدام مكتبات harfbuzz-shaping-engine-dll.dll. |
| [skipWinNativeLib()](#skipWinNativeLib) | Skip loading and use WindowsNativeCall\_x86 | \_x64.dll libraries. |
### clearAsposeNativeTmpDirectory() {#clearAsposeNativeTmpDirectory}
```
public static void clearAsposeNativeTmpDirectory()
```


يمسح الدليل الذي تُخزن فيه مكتبات Aspose المؤقتة.

### getInterruptThreadIfImageExceptionThrown() {#getInterruptThreadIfImageExceptionThrown}
```
public static boolean getInterruptThreadIfImageExceptionThrown()
```


يعيد القيمة الحالية للخاصية التي تتحكم في مقاطعة الخيط عند استثناءات الصورة.

**Remarks:**

القيمة الافتراضية هي `false`.

**Returns:**
boolean - هل يجب مقاطعة الخيط عند استثناءات الصورة.
### getTmpDirectoryPath() {#getTmpDirectoryPath}
```
public static String getTmpDirectoryPath()
```


إرجاع المسار إلى الدليل المؤقت للمكتبات الأصلية.

**Returns:**
java.lang.String
### getUseJAIImageRendering() {#getUseJAIImageRendering}
```
public static boolean getUseJAIImageRendering()
```


يحصل على قيمة تحدد ما إذا كان يتم استخدام JAI (Java Advanced Imaging) أثناء عرض صور المستند. في بعض الحالات، قد يحسن ذلك الأداء.

**Remarks:**

القيمة الافتراضية هي `true`.

سيتم استخدام JAI فقط إذا تم تضمينه كاعتماد كما هو موضح [here][]. قد لا يتم عرض بعض الصور بشكل صحيح إذا تم تعطيل JAI.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Returns:**
boolean - هل يُستخدم JAI.
### isHarfBuzzNativeLibLoaded() {#isHarfBuzzNativeLibLoaded}
```
public static boolean isHarfBuzzNativeLibLoaded()
```


يعيد `true` إذا تم تحميل مكتبات HarfBuzz. بشكل افتراضي، يتم تحميل المكتبات الأصلية.

**Returns:**
boolean
### isWinNativeLibLoaded() {#isWinNativeLibLoaded}
```
public static boolean isWinNativeLibLoaded()
```


يعيد `true` إذا تم تحميل مكتبات WindowsNativeCall. بشكل افتراضي، يتم تحميل المكتبات الأصلية.

**Returns:**
boolean
### loadHarfBuzzNativeLib() {#loadHarfBuzzNativeLib}
```
public static void loadHarfBuzzNativeLib()
```


يضبط لتحميل واستخدام مكتبات harfbuzz-shaping-engine-dll.dll. بشكل افتراضي، يتم تحميل المكتبات الأصلية.

### loadWinNativeLib() {#loadWinNativeLib}
```
public static void loadWinNativeLib()
```


يحدد تحميل واستخدام مكتبات WindowsNativeCall\_x86|\_x64.dll. بشكل افتراضي، يتم تحميل المكتبات الأصلية.

### setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown) {#setInterruptThreadIfImageExceptionThrown-boolean}
```
public static void setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)
```


يحدد الخاصية التي تحدد السلوك عند معالجة استثناءات الصورة. إذا تم تعيين الخاصية إلى true، سيتم مقاطعة خيط التنفيذ عندما يحدث استثناء أثناء معالجة الصورة.

**Remarks:**

القيمة الافتراضية هي `false`.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| abortSavingIfImageExceptionThrown | boolean | true - مقاطعة الخيط عند استثناءات الصورة، false - عدم المقاطعة |

### setTmpDirectoryPath(String path) {#setTmpDirectoryPath-java.lang.String}
```
public static void setTmpDirectoryPath(String path)
```


يحدد المسار إلى الدليل المؤقت للمكتبات الأصلية.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| المسار | java.lang.String | المسار إلى الدليل المؤقت للمكتبات الأصلية. |

### setUseJAIImageRendering(boolean useJAIImageRendering) {#setUseJAIImageRendering-boolean}
```
public static void setUseJAIImageRendering(boolean useJAIImageRendering)
```


يحدد قيمة تحدد ما إذا كان يتم استخدام JAI (Java Advanced Imaging) أثناء عرض صور المستندات. في بعض الحالات، قد يحسن ذلك الأداء.

**Remarks:**

القيمة الافتراضية هي `true`.

سيتم استخدام JAI فقط إذا تم تضمينه كاعتماد كما هو موضح [here][]. قد لا يتم عرض بعض الصور بشكل صحيح إذا تم تعطيل JAI.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| useJAIImageRendering | boolean | هل من الضروري استخدام JAI. |

### skipHarfBuzzNativeLib() {#skipHarfBuzzNativeLib}
```
public static void skipHarfBuzzNativeLib()
```


تجاوز تحميل واستخدام مكتبات harfbuzz-shaping-engine-dll.dll. بشكل افتراضي، يتم تحميل المكتبات الأصلية.

### skipWinNativeLib() {#skipWinNativeLib}
```
public static void skipWinNativeLib()
```


تجاوز تحميل واستخدام مكتبات WindowsNativeCall\_x86|\_x64.dll. بشكل افتراضي، يتم تحميل المكتبات الأصلية.

