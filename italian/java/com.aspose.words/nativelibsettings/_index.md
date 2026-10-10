---
title: "NativeLibSettings"
linktitle: "NativeLibSettings"
second_title: "Aspose.Words per Java"
description: "Questa classe aiuta a impostare varie opzioni come la cartella temporanea per le librerie native di Aspose.Words e se le librerie native devono essere caricate e utilizzate in Java."
type: docs
weight: 475
url: /it/java/com.aspose.words/nativelibsettings/
---

**Inheritance:**
java.lang.Object
```
public class NativeLibSettings
```

Questa classe aiuta a impostare varie opzioni come la cartella temporanea per le librerie native di Aspose.Words e se le librerie native devono essere caricate e utilizzate.
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [clearAsposeNativeTmpDirectory()](#clearAsposeNativeTmpDirectory) | Cancella la directory in cui sono archiviate le librerie temporanee di Aspose. |
| [getInterruptThreadIfImageExceptionThrown()](#getInterruptThreadIfImageExceptionThrown) | Restituisce il valore corrente della proprietà che controlla l'interruzione del thread in caso di eccezioni di immagine. |
| [getTmpDirectoryPath()](#getTmpDirectoryPath) | Restituisce il percorso della directory temporanea delle librerie native. |
| [getUseJAIImageRendering()](#getUseJAIImageRendering) | Ottiene un valore che determina se JAI (Java Advanced Imaging) è utilizzato durante il rendering delle immagini del documento. |
| [isHarfBuzzNativeLibLoaded()](#isHarfBuzzNativeLibLoaded) | Restituisce `true` se le librerie HarfBuzz sono caricate. |
| [isWinNativeLibLoaded()](#isWinNativeLibLoaded) | Restituisce `true` se le librerie WindowsNativeCall sono caricate. |
| [loadHarfBuzzNativeLib()](#loadHarfBuzzNativeLib) | Imposta il caricamento e l'uso delle librerie harfbuzz-shaping-engine-dll.dll. |
| [loadWinNativeLib()](#loadWinNativeLib) | Sets to load and use WindowsNativeCall\_x86 | Librerie \_x64.dll. |
| [setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)](#setInterruptThreadIfImageExceptionThrown-boolean) | Imposta la proprietà che definisce il comportamento nella gestione delle eccezioni di immagine. |
| [setTmpDirectoryPath(String path)](#setTmpDirectoryPath-java.lang.String) | Specifica il percorso della directory temporanea delle librerie native. |
| [setUseJAIImageRendering(boolean useJAIImageRendering)](#setUseJAIImageRendering-boolean) | Imposta un valore che determina se JAI (Java Advanced Imaging) è utilizzato durante il rendering delle immagini del documento. |
| [skipHarfBuzzNativeLib()](#skipHarfBuzzNativeLib) | Salta il caricamento e utilizza le librerie harfbuzz-shaping-engine-dll.dll. |
| [skipWinNativeLib()](#skipWinNativeLib) | Skip loading and use WindowsNativeCall\_x86 | Librerie \_x64.dll. |
### clearAsposeNativeTmpDirectory() {#clearAsposeNativeTmpDirectory}
```
public static void clearAsposeNativeTmpDirectory()
```


Cancella la directory in cui sono archiviate le librerie temporanee di Aspose.

### getInterruptThreadIfImageExceptionThrown() {#getInterruptThreadIfImageExceptionThrown}
```
public static boolean getInterruptThreadIfImageExceptionThrown()
```


Restituisce il valore corrente della proprietà che controlla l'interruzione del thread in caso di eccezioni di immagine.

**Remarks:**

Il valore predefinito è `false`.

**Returns:**
boolean - indica se il thread deve essere interrotto in caso di eccezioni di immagine.
### getTmpDirectoryPath() {#getTmpDirectoryPath}
```
public static String getTmpDirectoryPath()
```


Restituisce il percorso della directory temporanea delle librerie native.

**Returns:**
java.lang.String
### getUseJAIImageRendering() {#getUseJAIImageRendering}
```
public static boolean getUseJAIImageRendering()
```


Ottiene un valore che determina se JAI (Java Advanced Imaging) è utilizzato durante il rendering delle immagini del documento. In alcuni casi, ciò può migliorare le prestazioni.

**Remarks:**

Il valore predefinito è `true`.

JAI verrà utilizzato solo se è incluso come dipendenza come descritto [here][]. Alcune immagini potrebbero non essere renderizzate correttamente se JAI è disabilitato.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Returns:**
boolean - indica se JAI è utilizzato.
### isHarfBuzzNativeLibLoaded() {#isHarfBuzzNativeLibLoaded}
```
public static boolean isHarfBuzzNativeLibLoaded()
```


Restituisce `true` se le librerie HarfBuzz sono caricate. Per impostazione predefinita, le librerie native sono caricate.

**Returns:**
boolean
### isWinNativeLibLoaded() {#isWinNativeLibLoaded}
```
public static boolean isWinNativeLibLoaded()
```


Restituisce `true` se le librerie WindowsNativeCall sono caricate. Per impostazione predefinita, le librerie native sono caricate.

**Returns:**
boolean
### loadHarfBuzzNativeLib() {#loadHarfBuzzNativeLib}
```
public static void loadHarfBuzzNativeLib()
```


Imposta il caricamento e l'uso delle librerie harfbuzz-shaping-engine-dll.dll. Per impostazione predefinita, le librerie native sono caricate.

### loadWinNativeLib() {#loadWinNativeLib}
```
public static void loadWinNativeLib()
```


Imposta il caricamento e l'uso delle librerie WindowsNativeCall\\_x86|\\_x64.dll. Per impostazione predefinita, le librerie native vengono caricate.

### setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown) {#setInterruptThreadIfImageExceptionThrown-boolean}
```
public static void setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)
```


Imposta la proprietà che definisce il comportamento nella gestione delle eccezioni di immagine. Se la proprietà è impostata su true, il thread di esecuzione verrà interrotto quando si verifica un'eccezione durante l'elaborazione dell'immagine.

**Remarks:**

Il valore predefinito è `false`.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| abortSavingIfImageExceptionThrown | boolean | true - interrompe il thread in caso di eccezioni di immagine, false - non interrompe |

### setTmpDirectoryPath(String path) {#setTmpDirectoryPath-java.lang.String}
```
public static void setTmpDirectoryPath(String path)
```


Specifica il percorso della directory temporanea delle librerie native.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| percorso | java.lang.String | il percorso della directory temporanea delle librerie native. |

### setUseJAIImageRendering(boolean useJAIImageRendering) {#setUseJAIImageRendering-boolean}
```
public static void setUseJAIImageRendering(boolean useJAIImageRendering)
```


Imposta un valore che determina se JAI (Java Advanced Imaging) viene utilizzato durante il rendering delle immagini dei documenti. In alcuni casi, ciò può migliorare le prestazioni.

**Remarks:**

Il valore predefinito è `true`.

JAI verrà utilizzato solo se è incluso come dipendenza come descritto [here][]. Alcune immagini potrebbero non essere renderizzate correttamente se JAI è disabilitato.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| useJAIImageRendering | boolean | è necessario utilizzare JAI. |

### skipHarfBuzzNativeLib() {#skipHarfBuzzNativeLib}
```
public static void skipHarfBuzzNativeLib()
```


Salta il caricamento e utilizza le librerie harfbuzz-shaping-engine-dll.dll. Per impostazione predefinita, le librerie native vengono caricate.

### skipWinNativeLib() {#skipWinNativeLib}
```
public static void skipWinNativeLib()
```


Salta il caricamento e utilizza le librerie WindowsNativeCall\\_x86|\\_x64.dll. Per impostazione predefinita, le librerie native vengono caricate.

