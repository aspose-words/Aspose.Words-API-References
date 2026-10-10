---
title: "NativeLibSettings"
linktitle: "NativeLibSettings"
second_title: "Aspose.Words pour Java"
description: "Cette classe aide à définir diverses options telles que le dossier temporaire pour les bibliothèques natives Aspose.Words et si les bibliothèques natives doivent être chargées et utilisées en Java."
type: docs
weight: 475
url: /fr/java/com.aspose.words/nativelibsettings/
---

**Inheritance:**
java.lang.Object
```
public class NativeLibSettings
```

Cette classe aide à définir diverses options telles que le dossier temporaire pour les bibliothèques natives d'Aspose.Words et si les bibliothèques natives doivent être chargées et utilisées.
## Méthodes

| Méthode | Description |
| --- | --- |
| [clearAsposeNativeTmpDirectory()](#clearAsposeNativeTmpDirectory) | Efface le répertoire où les bibliothèques temporaires Aspose sont stockées. |
| [getInterruptThreadIfImageExceptionThrown()](#getInterruptThreadIfImageExceptionThrown) | Renvoie la valeur actuelle de la propriété qui contrôle l’interruption du thread en cas d’exceptions d’image. |
| [getTmpDirectoryPath()](#getTmpDirectoryPath) | Renvoie le chemin du répertoire temporaire des bibliothèques natives. |
| [getUseJAIImageRendering()](#getUseJAIImageRendering) | Obtient une valeur qui détermine si JAI (Java Advanced Imaging) est utilisé lors du rendu des images du document. |
| [isHarfBuzzNativeLibLoaded()](#isHarfBuzzNativeLibLoaded) | Renvoie `true` si les bibliothèques HarfBuzz sont chargées. |
| [isWinNativeLibLoaded()](#isWinNativeLibLoaded) | Renvoie `true` si les bibliothèques WindowsNativeCall sont chargées. |
| [loadHarfBuzzNativeLib()](#loadHarfBuzzNativeLib) | Définit le chargement et l’utilisation des bibliothèques harfbuzz-shaping-engine-dll.dll. |
| [loadWinNativeLib()](#loadWinNativeLib) | Sets to load and use WindowsNativeCall\_x86 | \_x64.dll libraries. |
| [setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)](#setInterruptThreadIfImageExceptionThrown-boolean) | Définit la propriété qui définit le comportement lors du traitement des exceptions d’image. |
| [setTmpDirectoryPath(String path)](#setTmpDirectoryPath-java.lang.String) | Spécifie le chemin du répertoire temporaire des bibliothèques natives. |
| [setUseJAIImageRendering(boolean useJAIImageRendering)](#setUseJAIImageRendering-boolean) | Définit une valeur qui détermine si JAI (Java Advanced Imaging) est utilisé lors du rendu des images du document. |
| [skipHarfBuzzNativeLib()](#skipHarfBuzzNativeLib) | Ignorer le chargement et utiliser les bibliothèques harfbuzz-shaping-engine-dll.dll. |
| [skipWinNativeLib()](#skipWinNativeLib) | Skip loading and use WindowsNativeCall\_x86 | \_x64.dll libraries. |
### clearAsposeNativeTmpDirectory() {#clearAsposeNativeTmpDirectory}
```
public static void clearAsposeNativeTmpDirectory()
```


Efface le répertoire où les bibliothèques temporaires Aspose sont stockées.

### getInterruptThreadIfImageExceptionThrown() {#getInterruptThreadIfImageExceptionThrown}
```
public static boolean getInterruptThreadIfImageExceptionThrown()
```


Renvoie la valeur actuelle de la propriété qui contrôle l’interruption du thread en cas d’exceptions d’image.

**Remarks:**

La valeur par défaut est `false`.

**Returns:**
booléen - indique si le thread doit être interrompu en cas d’exceptions d’image.
### getTmpDirectoryPath() {#getTmpDirectoryPath}
```
public static String getTmpDirectoryPath()
```


Renvoie le chemin du répertoire temporaire des bibliothèques natives.

**Returns:**
java.lang.String
### getUseJAIImageRendering() {#getUseJAIImageRendering}
```
public static boolean getUseJAIImageRendering()
```


Obtient une valeur qui détermine si JAI (Java Advanced Imaging) est utilisé lors du rendu des images du document. Dans certains cas, cela peut améliorer les performances.

**Remarks:**

La valeur par défaut est `true`.

JAI ne sera utilisé que s’il est inclus comme dépendance comme décrit [here][]. Certaines images pourraient ne pas être rendues correctement si JAI est désactivé.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Returns:**
booléen - indique si JAI est utilisé.
### isHarfBuzzNativeLibLoaded() {#isHarfBuzzNativeLibLoaded}
```
public static boolean isHarfBuzzNativeLibLoaded()
```


Renvoie `true` si les bibliothèques HarfBuzz sont chargées. Par défaut, les bibliothèques natives sont chargées.

**Returns:**
boolean
### isWinNativeLibLoaded() {#isWinNativeLibLoaded}
```
public static boolean isWinNativeLibLoaded()
```


Renvoie `true` si les bibliothèques WindowsNativeCall sont chargées. Par défaut, les bibliothèques natives sont chargées.

**Returns:**
boolean
### loadHarfBuzzNativeLib() {#loadHarfBuzzNativeLib}
```
public static void loadHarfBuzzNativeLib()
```


Définit le chargement et l’utilisation des bibliothèques harfbuzz-shaping-engine-dll.dll. Par défaut, les bibliothèques natives sont chargées.

### loadWinNativeLib() {#loadWinNativeLib}
```
public static void loadWinNativeLib()
```


Définit le chargement et l'utilisation des bibliothèques WindowsNativeCall\_x86|\_x64.dll. Par défaut, les bibliothèques natives sont chargées.

### setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown) {#setInterruptThreadIfImageExceptionThrown-boolean}
```
public static void setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)
```


Définit la propriété qui définit le comportement lors du traitement des exceptions d'image. Si la propriété est définie sur true, le thread d'exécution sera interrompu lorsqu'une exception se produit pendant le traitement d'image.

**Remarks:**

La valeur par défaut est `false`.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| abortSavingIfImageExceptionThrown | boolean | true - interrompre le thread en cas d'exceptions d'image, false - ne pas interrompre |

### setTmpDirectoryPath(String path) {#setTmpDirectoryPath-java.lang.String}
```
public static void setTmpDirectoryPath(String path)
```


Spécifie le chemin du répertoire temporaire des bibliothèques natives.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| path | java.lang.String | le chemin du répertoire temporaire des bibliothèques natives. |

### setUseJAIImageRendering(boolean useJAIImageRendering) {#setUseJAIImageRendering-boolean}
```
public static void setUseJAIImageRendering(boolean useJAIImageRendering)
```


Définit une valeur qui détermine si JAI (Java Advanced Imaging) est utilisé lors du rendu des images de documents. Dans certains cas, cela peut améliorer les performances.

**Remarks:**

La valeur par défaut est `true`.

JAI ne sera utilisé que s’il est inclus comme dépendance comme décrit [here][]. Certaines images pourraient ne pas être rendues correctement si JAI est désactivé.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| useJAIImageRendering | boolean | est-il nécessaire d'utiliser JAI. |

### skipHarfBuzzNativeLib() {#skipHarfBuzzNativeLib}
```
public static void skipHarfBuzzNativeLib()
```


Ignorer le chargement et utiliser les bibliothèques harfbuzz-shaping-engine-dll.dll. Par défaut, les bibliothèques natives sont chargées.

### skipWinNativeLib() {#skipWinNativeLib}
```
public static void skipWinNativeLib()
```


Ignorer le chargement et utiliser les bibliothèques WindowsNativeCall\_x86|\_x64.dll. Par défaut, les bibliothèques natives sont chargées.

