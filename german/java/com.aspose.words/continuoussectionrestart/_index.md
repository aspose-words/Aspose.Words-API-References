---
title: "ContinuousSectionRestart"
linktitle: "ContinuousSectionRestart"
second_title: "Aspose.Words für Java"
description: "Stellt unterschiedliche Verhaltensweisen beim Berechnen von Seitenzahlen in einem kontinuierlichen Abschnitt dar, der die Seitennummerierung in Java neu startet."
type: docs
weight: 127
url: /de/java/com.aspose.words/continuoussectionrestart/
---

**Inheritance:**
java.lang.Object
```
public class ContinuousSectionRestart
```

Stellt unterschiedliche Verhaltensweisen bei der Berechnung von Seitenzahlen in einem fortlaufenden Abschnitt dar, der die Seitennummerierung neu startet.

 **Examples:** 

Zeigt, wie die Seitennummerierung in einem kontinuierlichen Abschnitt gesteuert wird.

```

 Document doc = new Document(getMyDir() + "Continuous section page numbering.docx");

 // By default Aspose.Words behavior matches the Microsoft Word 2019.
 // If you need old Aspose.Words behavior, repetitive Microsoft Word 2016, use 'ContinuousSectionRestart.FromNewPageOnly'.
 // Page numbering restarts only if there is no other content before the section on the page where the section starts,
 // because of that the numbering will reset to 2 from the second page.
 doc.getLayoutOptions().setContinuousSectionPageNumberingRestart(ContinuousSectionRestart.FROM_NEW_PAGE_ONLY);
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Layout.RestartPageNumberingInContinuousSection.pdf");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ALWAYS](#ALWAYS) | Die Seitennummerierung wird immer neu gestartet, unabhängig vom Inhaltsfluss. |
| [FROM_NEW_PAGE_ONLY](#FROM-NEW-PAGE-ONLY) | Die Seitennummerierung wird nur neu gestartet, wenn vor dem Abschnitt auf der Seite, auf der der Abschnitt beginnt, kein anderer Inhalt vorhanden ist. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String continuousSectionRestartName)](#fromName-java.lang.String) |  |
| [getName(int continuousSectionRestart)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int continuousSectionRestart)](#toString-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


Die Seitennummerierung wird immer neu gestartet, unabhängig vom Inhaltsfluss.

 **Remarks:** 

Dieses Verhalten wird von allen MS‑Word‑Versionen gezeigt, außer Word 2016.

### FROM_NEW_PAGE_ONLY {#FROM-NEW-PAGE-ONLY}
```
public static int FROM_NEW_PAGE_ONLY
```


Die Seitennummerierung wird nur neu gestartet, wenn vor dem Abschnitt auf der Seite, auf der der Abschnitt beginnt, kein anderer Inhalt vorhanden ist.

 **Remarks:** 

Das Verhalten wird von MS Word 2016 gezeigt.

### length {#length}
```
public static int length
```


### fromName(String continuousSectionRestartName) {#fromName-java.lang.String}
```
public static int fromName(String continuousSectionRestartName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| continuousSectionRestartName | java.lang.String |  |

**Returns:**
int
### getName(int continuousSectionRestart) {#getName-int}
```
public static String getName(int continuousSectionRestart)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| continuousSectionRestart | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int continuousSectionRestart) {#toString-int}
```
public static String toString(int continuousSectionRestart)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| continuousSectionRestart | int |  |

**Returns:**
java.lang.String
