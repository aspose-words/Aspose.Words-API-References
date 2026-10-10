---
title: "ContinuousSectionRestart"
linktitle: "ContinuousSectionRestart"
second_title: "Aspose.Words لـ Java"
description: "يمثل سلوكيات مختلفة عند حساب أرقام الصفحات في قسم مستمر يعيد بدء ترقيم الصفحات في Java."
type: docs
weight: 127
url: /ar/java/com.aspose.words/continuoussectionrestart/
---

**Inheritance:**
java.lang.Object
```
public class ContinuousSectionRestart
```

يمثل سلوكيات مختلفة عند حساب أرقام الصفحات في قسم مستمر يعيد بدء ترقيم الصفحات.

 **Examples:** 

يوضح كيفية التحكم في ترقيم الصفحات في قسم مستمر.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [ALWAYS](#ALWAYS) | ترقيم الصفحات يعيد البدء دائمًا بغض النظر عن تدفق المحتوى. |
| [FROM_NEW_PAGE_ONLY](#FROM-NEW-PAGE-ONLY) | ترقيم الصفحات يعيد البدء فقط إذا لم يكن هناك محتوى آخر قبل القسم على الصفحة التي يبدأ فيها القسم. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String continuousSectionRestartName)](#fromName-java.lang.String) |  |
| [getName(int continuousSectionRestart)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int continuousSectionRestart)](#toString-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


ترقيم الصفحات يعيد البدء دائمًا بغض النظر عن تدفق المحتوى.

 **Remarks:** 

هذا السلوك يتم توضيحه في جميع إصدارات MS Word، باستثناء Word 2016.

### FROM_NEW_PAGE_ONLY {#FROM-NEW-PAGE-ONLY}
```
public static int FROM_NEW_PAGE_ONLY
```


ترقيم الصفحات يعيد البدء فقط إذا لم يكن هناك محتوى آخر قبل القسم على الصفحة التي يبدأ فيها القسم.

 **Remarks:** 

السلوك يتم توضيحه في MS Word 2016.

### length {#length}
```
public static int length
```


### fromName(String continuousSectionRestartName) {#fromName-java.lang.String}
```
public static int fromName(String continuousSectionRestartName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| continuousSectionRestartName | java.lang.String |  |

**Returns:**
int
### getName(int continuousSectionRestart) {#getName-int}
```
public static String getName(int continuousSectionRestart)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| continuousSectionRestart | int |  |

**Returns:**
java.lang.String
