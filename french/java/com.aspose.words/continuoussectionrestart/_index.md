---
title: "ContinuousSectionRestart"
linktitle: "ContinuousSectionRestart"
second_title: "Aspose.Words pour Java"
description: "Représente différents comportements lors du calcul des numéros de page dans une section continue qui redémarre la numérotation des pages en Java."
type: docs
weight: 127
url: /fr/java/com.aspose.words/continuoussectionrestart/
---

**Inheritance:**
java.lang.Object
```
public class ContinuousSectionRestart
```

Représente les différents comportements lors du calcul des numéros de page dans une section continue qui redémarre la numérotation des pages.

 **Examples:** 

Montre comment contrôler la numérotation des pages dans une section continue.

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
## Champs

| Champ | Description |
| --- | --- |
| [ALWAYS](#ALWAYS) | La numérotation des pages redémarre toujours, quel que soit le flux de contenu. |
| [FROM_NEW_PAGE_ONLY](#FROM-NEW-PAGE-ONLY) | La numérotation des pages redémarre uniquement s'il n'y a aucun autre contenu avant la section sur la page où la section commence. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String continuousSectionRestartName)](#fromName-java.lang.String) |  |
| [getName(int continuousSectionRestart)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int continuousSectionRestart)](#toString-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


La numérotation des pages redémarre toujours, quel que soit le flux de contenu.

 **Remarks:** 

Ce comportement est démontré par toutes les versions de MS Word, sauf Word 2016.

### FROM_NEW_PAGE_ONLY {#FROM-NEW-PAGE-ONLY}
```
public static int FROM_NEW_PAGE_ONLY
```


La numérotation des pages redémarre uniquement s'il n'y a aucun autre contenu avant la section sur la page où la section commence.

 **Remarks:** 

Le comportement est démontré par MS Word 2016.

### length {#length}
```
public static int length
```


### fromName(String continuousSectionRestartName) {#fromName-java.lang.String}
```
public static int fromName(String continuousSectionRestartName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| continuousSectionRestartName | java.lang.String |  |

**Returns:**
int
### getName(int continuousSectionRestart) {#getName-int}
```
public static String getName(int continuousSectionRestart)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| continuousSectionRestart | int |  |

**Returns:**
java.lang.String
