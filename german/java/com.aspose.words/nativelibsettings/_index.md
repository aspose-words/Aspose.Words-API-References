---
title: "NativeLibSettings"
linktitle: "NativeLibSettings"
second_title: "Aspose.Words für Java"
description: "Diese Klasse hilft, verschiedene Optionen festzulegen, wie z.B. den temporären Ordner für native Bibliotheken von Aspose.Words und ob native Bibliotheken in Java geladen und verwendet werden sollen."
type: docs
weight: 475
url: /de/java/com.aspose.words/nativelibsettings/
---

**Inheritance:**
java.lang.Object
```
public class NativeLibSettings
```

Diese Klasse hilft beim Festlegen verschiedener Optionen, wie z. B. des temporären Ordners für native Bibliotheken von Aspose.Words und ob native Bibliotheken geladen und verwendet werden sollen.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [clearAsposeNativeTmpDirectory()](#clearAsposeNativeTmpDirectory) | Löscht das Verzeichnis, in dem temporäre Aspose-Bibliotheken gespeichert werden. |
| [getInterruptThreadIfImageExceptionThrown()](#getInterruptThreadIfImageExceptionThrown) | Gibt den aktuellen Wert der Eigenschaft zurück, die die Thread-Unterbrechung bei Bildausnahmen steuert. |
| [getTmpDirectoryPath()](#getTmpDirectoryPath) | Gibt den Pfad zum temporären Verzeichnis der nativen Bibliotheken zurück. |
| [getUseJAIImageRendering()](#getUseJAIImageRendering) | Liest einen Wert, der bestimmt, ob JAI (Java Advanced Imaging) bei der Darstellung von Dokumentenbildern verwendet wird. |
| [isHarfBuzzNativeLibLoaded()](#isHarfBuzzNativeLibLoaded) | Gibt `true` zurück, wenn HarfBuzz-Bibliotheken geladen sind. |
| [isWinNativeLibLoaded()](#isWinNativeLibLoaded) | Gibt `true` zurück, wenn WindowsNativeCall-Bibliotheken geladen sind. |
| [loadHarfBuzzNativeLib()](#loadHarfBuzzNativeLib) | Setzt das Laden und die Verwendung von harfbuzz-shaping-engine-dll.dll-Bibliotheken. |
| [loadWinNativeLib()](#loadWinNativeLib) | Sets to load and use WindowsNativeCall\_x86 | \_x64.dll Bibliotheken. |
| [setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)](#setInterruptThreadIfImageExceptionThrown-boolean) | Setzt die Eigenschaft, die das Verhalten beim Umgang mit Bildausnahmen definiert. |
| [setTmpDirectoryPath(String path)](#setTmpDirectoryPath-java.lang.String) | Gibt den Pfad zum temporären Verzeichnis der nativen Bibliotheken an. |
| [setUseJAIImageRendering(boolean useJAIImageRendering)](#setUseJAIImageRendering-boolean) | Legt einen Wert fest, der bestimmt, ob JAI (Java Advanced Imaging) beim Rendern von Dokumentenbildern verwendet wird. |
| [skipHarfBuzzNativeLib()](#skipHarfBuzzNativeLib) | Überspringe das Laden und verwende die Bibliotheken harfbuzz-shaping-engine-dll.dll. |
| [skipWinNativeLib()](#skipWinNativeLib) | Skip loading and use WindowsNativeCall\_x86 | \_x64.dll Bibliotheken. |
### clearAsposeNativeTmpDirectory() {#clearAsposeNativeTmpDirectory}
```
public static void clearAsposeNativeTmpDirectory()
```


Löscht das Verzeichnis, in dem temporäre Aspose-Bibliotheken gespeichert werden.

### getInterruptThreadIfImageExceptionThrown() {#getInterruptThreadIfImageExceptionThrown}
```
public static boolean getInterruptThreadIfImageExceptionThrown()
```


Gibt den aktuellen Wert der Eigenschaft zurück, die die Thread-Unterbrechung bei Bildausnahmen steuert.

**Remarks:**

Der Standardwert ist `false`.

**Returns:**
boolean – gibt an, ob der Thread bei Bildausnahmen unterbrochen werden soll.
### getTmpDirectoryPath() {#getTmpDirectoryPath}
```
public static String getTmpDirectoryPath()
```


Gibt den Pfad zum temporären Verzeichnis der nativen Bibliotheken zurück.

**Returns:**
java.lang.String
### getUseJAIImageRendering() {#getUseJAIImageRendering}
```
public static boolean getUseJAIImageRendering()
```


Liest einen Wert, der bestimmt, ob JAI (Java Advanced Imaging) beim Rendern von Dokumentenbildern verwendet wird. In einigen Fällen kann dies die Leistung verbessern.

**Remarks:**

Der Standardwert ist `true`.

JAI wird nur verwendet, wenn es als Abhängigkeit eingebunden ist, wie [here][]. Bestimmte Bilder werden möglicherweise nicht korrekt gerendert, wenn JAI deaktiviert ist.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Returns:**
boolean – gibt an, ob JAI verwendet wird.
### isHarfBuzzNativeLibLoaded() {#isHarfBuzzNativeLibLoaded}
```
public static boolean isHarfBuzzNativeLibLoaded()
```


Gibt `true` zurück, wenn die HarfBuzz-Bibliotheken geladen sind. Standardmäßig werden native Bibliotheken geladen.

**Returns:**
boolean
### isWinNativeLibLoaded() {#isWinNativeLibLoaded}
```
public static boolean isWinNativeLibLoaded()
```


Gibt `true` zurück, wenn die WindowsNativeCall-Bibliotheken geladen sind. Standardmäßig werden native Bibliotheken geladen.

**Returns:**
boolean
### loadHarfBuzzNativeLib() {#loadHarfBuzzNativeLib}
```
public static void loadHarfBuzzNativeLib()
```


Legt fest, die Bibliotheken harfbuzz-shaping-engine-dll.dll zu laden und zu verwenden. Standardmäßig werden native Bibliotheken geladen.

### loadWinNativeLib() {#loadWinNativeLib}
```
public static void loadWinNativeLib()
```


Legt fest, die Bibliotheken WindowsNativeCall\_x86|\_x64.dll zu laden und zu verwenden. Standardmäßig werden native Bibliotheken geladen.

### setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown) {#setInterruptThreadIfImageExceptionThrown-boolean}
```
public static void setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)
```


Legt die Eigenschaft fest, die das Verhalten bei Bildausnahmen definiert. Ist die Eigenschaft auf true gesetzt, wird der Ausführungs‑Thread unterbrochen, wenn während der Bildverarbeitung eine Ausnahme auftritt.

**Remarks:**

Der Standardwert ist `false`.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| abortSavingIfImageExceptionThrown | boolean | true – Thread bei Bildausnahmen unterbrechen, false – nicht unterbrechen |

### setTmpDirectoryPath(String path) {#setTmpDirectoryPath-java.lang.String}
```
public static void setTmpDirectoryPath(String path)
```


Gibt den Pfad zum temporären Verzeichnis der nativen Bibliotheken an.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Pfad | java.lang.String | Der Pfad zum temporären Verzeichnis der nativen Bibliotheken. |

### setUseJAIImageRendering(boolean useJAIImageRendering) {#setUseJAIImageRendering-boolean}
```
public static void setUseJAIImageRendering(boolean useJAIImageRendering)
```


Legt einen Wert fest, der bestimmt, ob JAI (Java Advanced Imaging) beim Rendern von Dokumentenbildern verwendet wird. In einigen Fällen kann dies die Leistung verbessern.

**Remarks:**

Der Standardwert ist `true`.

JAI wird nur verwendet, wenn es als Abhängigkeit eingebunden ist, wie [here][]. Bestimmte Bilder werden möglicherweise nicht korrekt gerendert, wenn JAI deaktiviert ist.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| useJAIImageRendering | boolean | Ist es notwendig, JAI zu verwenden. |

### skipHarfBuzzNativeLib() {#skipHarfBuzzNativeLib}
```
public static void skipHarfBuzzNativeLib()
```


Überspringe das Laden und verwende die Bibliotheken harfbuzz-shaping-engine-dll.dll. Standardmäßig werden native Bibliotheken geladen.

### skipWinNativeLib() {#skipWinNativeLib}
```
public static void skipWinNativeLib()
```


Überspringe das Laden und verwende die Bibliotheken WindowsNativeCall\_x86|\_x64.dll. Standardmäßig werden native Bibliotheken geladen.

