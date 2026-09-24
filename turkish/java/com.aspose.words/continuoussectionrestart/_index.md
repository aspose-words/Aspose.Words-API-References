---
title: "ContinuousSectionRestart"
linktitle: "ContinuousSectionRestart"
second_title: "Aspose.Words Java için"
description: "Java'da sayfa numaralandırmasını yeniden başlatan sürekli bir bölümde sayfa numaraları hesaplanırken farklı davranışları temsil eder."
type: docs
weight: 127
url: /tr/java/com.aspose.words/continuoussectionrestart/
---

**Inheritance:**
java.lang.Object
```
public class ContinuousSectionRestart
```

Sayfa numaralandırmasını yeniden başlatan sürekli bir bölümde sayfa numaraları hesaplanırken farklı davranışları temsil eder.

 **Examples:** 

Sürekli bir bölümde sayfa numaralandırmasını nasıl kontrol edeceğinizi gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ALWAYS](#ALWAYS) | Sayfa numaralandırması, içerik akışına bakılmaksızın her zaman yeniden başlar. |
| [FROM_NEW_PAGE_ONLY](#FROM-NEW-PAGE-ONLY) | Sayfa numaralandırması, bölümün başladığı sayfada bölümden önce başka içerik olmadığında yalnızca yeniden başlar. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String continuousSectionRestartName)](#fromName-java.lang.String) |  |
| [getName(int continuousSectionRestart)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int continuousSectionRestart)](#toString-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


Sayfa numaralandırması, içerik akışına bakılmaksızın her zaman yeniden başlar.

 **Remarks:** 

Bu davranış, Word 2016 dışındaki tüm MS Word sürümlerinde gösterilir.

### FROM_NEW_PAGE_ONLY {#FROM-NEW-PAGE-ONLY}
```
public static int FROM_NEW_PAGE_ONLY
```


Sayfa numaralandırması, bölümün başladığı sayfada bölümden önce başka içerik olmadığında yalnızca yeniden başlar.

 **Remarks:** 

Bu davranış, MS Word 2016'da gösterilir.

### length {#length}
```
public static int length
```


### fromName(String continuousSectionRestartName) {#fromName-java.lang.String}
```
public static int fromName(String continuousSectionRestartName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| continuousSectionRestartName | java.lang.String |  |

**Returns:**
int
### getName(int continuousSectionRestart) {#getName-int}
```
public static String getName(int continuousSectionRestart)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| continuousSectionRestart | int |  |

**Returns:**
java.lang.String
