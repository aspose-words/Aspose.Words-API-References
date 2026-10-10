---
title: "ContinuousSectionRestart"
linktitle: "ContinuousSectionRestart"
second_title: "Aspose.Words для Java"
description: "Представляет различные поведения при вычислении номеров страниц в непрерывном разделе, который перезапускает нумерацию страниц в Java."
type: docs
weight: 127
url: /ru/java/com.aspose.words/continuoussectionrestart/
---

**Inheritance:**
java.lang.Object
```
public class ContinuousSectionRestart
```

Представляет различные поведения при вычислении номеров страниц в непрерывном разделе, который перезапускает нумерацию страниц.

 **Examples:** 

Показывает, как управлять нумерацией страниц в непрерывном разделе.

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
## Поля

| Поле | Описание |
| --- | --- |
| [ALWAYS](#ALWAYS) | Нумерация страниц всегда перезапускается независимо от потока содержимого. |
| [FROM_NEW_PAGE_ONLY](#FROM-NEW-PAGE-ONLY) | Нумерация страниц перезапускается только если перед разделом на странице, где начинается раздел, нет другого содержимого. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String continuousSectionRestartName)](#fromName-java.lang.String) |  |
| [getName(int continuousSectionRestart)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int continuousSectionRestart)](#toString-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


Нумерация страниц всегда перезапускается независимо от потока содержимого.

 **Remarks:** 

Это поведение демонстрируется во всех версиях MS Word, кроме Word 2016.

### FROM_NEW_PAGE_ONLY {#FROM-NEW-PAGE-ONLY}
```
public static int FROM_NEW_PAGE_ONLY
```


Нумерация страниц перезапускается только если перед разделом на странице, где начинается раздел, нет другого содержимого.

 **Remarks:** 

Это поведение демонстрируется в MS Word 2016.

### length {#length}
```
public static int length
```


### fromName(String continuousSectionRestartName) {#fromName-java.lang.String}
```
public static int fromName(String continuousSectionRestartName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| continuousSectionRestartName | java.lang.String |  |

**Returns:**
int
### getName(int continuousSectionRestart) {#getName-int}
```
public static String getName(int continuousSectionRestart)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| continuousSectionRestart | int |  |

**Returns:**
java.lang.String
