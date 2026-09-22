---
title: "SectionLayoutMode"
linktitle: "SectionLayoutMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد وضع التخطيط لقسم يسمح بتعريف سلوك شبكة المستند في Java."
type: docs
weight: 607
url: /ar/java/com.aspose.words/sectionlayoutmode/
---

**Inheritance:**
java.lang.Object
```
public class SectionLayoutMode
```

يحدد وضع التخطيط لقسم يسمح بتعريف سلوك شبكة المستند.

 **Examples:** 

يوضح كيفية تحديد حد لعدد الأحرف التي قد يحتويها كل سطر.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

يظهر كيفية تحديد حد لعدد الأسطر التي قد يحتويها كل صفحة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [DEFAULT](#DEFAULT) | يحدد أنه لا ينبغي تطبيق أي شبكة مستند على محتويات القسم المقابل في المستند. |
| [GRID](#GRID) | يحدد أن القسم المقابل يجب أن يحتوي على كل من ارتفاع السطر الإضافي وارتفاع الحرف المضاف إلى كل سطر وحرف داخله بهدف الحفاظ على عدد محدد من الأسطر لكل صفحة والحروف لكل سطر. |
| [LINE_GRID](#LINE-GRID) | يحدد أن القسم المقابل يجب أن يحتوي على ارتفاع سطر إضافي يُضاف إلى كل سطر داخله بهدف الحفاظ على العدد المحدد من الأسطر لكل صفحة. |
| [SNAP_TO_CHARS](#SNAP-TO-CHARS) | يحدد أن القسم المقابل يجب أن يحتوي على كل من ارتفاع السطر الإضافي وارتفاع الحرف المضاف إلى كل سطر وحرف داخله بهدف الحفاظ على عدد محدد من الأسطر لكل صفحة والحروف لكل سطر. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String sectionLayoutModeName)](#fromName-java.lang.String) |  |
| [getName(int sectionLayoutMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sectionLayoutMode)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


يحدد أنه لا ينبغي تطبيق أي شبكة مستند على محتويات القسم المقابل في المستند.

### GRID {#GRID}
```
public static int GRID
```


يحدد أن القسم المقابل يجب أن يحتوي على كل من ارتفاع السطر الإضافي وارتفاع الحرف المضاف إلى كل سطر وحرف داخله بهدف الحفاظ على عدد محدد من الأسطر لكل صفحة والحروف لكل سطر. لن يتم محاذاة الأحرف تلقائيًا مع خطوط الشبكة أثناء الكتابة.

### LINE_GRID {#LINE-GRID}
```
public static int LINE_GRID
```


يحدد أن القسم المقابل يجب أن يحتوي على ارتفاع سطر إضافي يُضاف إلى كل سطر داخله بهدف الحفاظ على العدد المحدد من الأسطر لكل صفحة.

### SNAP_TO_CHARS {#SNAP-TO-CHARS}
```
public static int SNAP_TO_CHARS
```


يحدد أن القسم المقابل يجب أن يحتوي على كل من ارتفاع السطر الإضافي وارتفاع الحرف المضاف إلى كل سطر وحرف داخله بهدف الحفاظ على عدد محدد من الأسطر لكل صفحة والحروف لكل سطر. سيتم محاذاة الأحرف تلقائيًا مع خطوط الشبكة أثناء الكتابة.

### length {#length}
```
public static int length
```


### fromName(String sectionLayoutModeName) {#fromName-java.lang.String}
```
public static int fromName(String sectionLayoutModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sectionLayoutModeName | java.lang.String |  |

**Returns:**
int
### getName(int sectionLayoutMode) {#getName-int}
```
public static String getName(int sectionLayoutMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sectionLayoutMode) {#toString-int}
```
public static String toString(int sectionLayoutMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
