---
title: PageBorderAppliesTo
linktitle: PageBorderAppliesTo
second_title: Aspose.Words for Java
description: Specifies which pages the page border is printed on in Java.
type: docs
weight: 486
url: /java/com.aspose.words/pageborderappliesto/
---

**Inheritance:**
java.lang.Object
```
public class PageBorderAppliesTo
```

Specifies which pages the page border is printed on.

 **Examples:** 

Shows how to create a wide blue band border at the top of the first page.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [ALL_PAGES](#ALL-PAGES) | Page border is shown on all pages of the section. |
| [FIRST_PAGE](#FIRST-PAGE) | Page border is shown on the first page of the section only. |
| [OTHER_PAGES](#OTHER-PAGES) | Page border is shown on all pages except the first page of the section. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String pageBorderAppliesToName)](#fromName-java.lang.String) |  |
| [getName(int pageBorderAppliesTo)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageBorderAppliesTo)](#toString-int) |  |
### ALL_PAGES {#ALL-PAGES}
```
public static int ALL_PAGES
```


Page border is shown on all pages of the section.

### FIRST_PAGE {#FIRST-PAGE}
```
public static int FIRST_PAGE
```


Page border is shown on the first page of the section only.

### OTHER_PAGES {#OTHER-PAGES}
```
public static int OTHER_PAGES
```


Page border is shown on all pages except the first page of the section.

### length {#length}
```
public static int length
```


### fromName(String pageBorderAppliesToName) {#fromName-java.lang.String}
```
public static int fromName(String pageBorderAppliesToName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageBorderAppliesToName | java.lang.String |  |

**Returns:**
int
### getName(int pageBorderAppliesTo) {#getName-int}
```
public static String getName(int pageBorderAppliesTo)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageBorderAppliesTo | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pageBorderAppliesTo) {#toString-int}
```
public static String toString(int pageBorderAppliesTo)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageBorderAppliesTo | int |  |

**Returns:**
java.lang.String
