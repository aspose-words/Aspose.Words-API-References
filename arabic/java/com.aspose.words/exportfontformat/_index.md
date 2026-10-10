---
title: "ExportFontFormat"
linktitle: "ExportFontFormat"
second_title: "Aspose.Words لـ Java"
description: "يشير إلى التنسيق المستخدم لتصدير الخطوط أثناء التحويل إلى تنسيق HTML ثابت في Java."
type: docs
weight: 191
url: /ar/java/com.aspose.words/exportfontformat/
---

**Inheritance:**
java.lang.Object
```
public class ExportFontFormat
```

يشير إلى التنسيق المستخدم لتصدير الخطوط أثناء التحويل إلى تنسيق HTML ثابت.

 **Examples:** 

يعرض كيفية استخدام الخطوط فقط من الجهاز الهدف عند حفظ مستند إلى HTML.

```

 Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

 HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
 {
     saveOptions.setExportEmbeddedCss(true);
     saveOptions.setUseTargetMachineFonts(useTargetMachineFonts);
     saveOptions.setFontFormat(ExportFontFormat.TTF);
     saveOptions.setExportEmbeddedFonts(false);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html"), StandardCharsets.UTF_8);

 if (useTargetMachineFonts)
     Assert.assertFalse(Pattern.compile("@font-face").matcher(outDocContents).find());
 else
     Assert.assertTrue(Pattern.compile(
         "@font-face [{] font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'\u263a'[)], " +
         "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; [}]").matcher(outDocContents).find());
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [TTF](#TTF) | TTF (تنسيق الخط TrueType). |
| [WOFF](#WOFF) | WOFF (تنسيق الخط Web Open Font). |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String exportFontFormatName)](#fromName-java.lang.String) |  |
| [getName(int exportFontFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int exportFontFormat)](#toString-int) |  |
### TTF {#TTF}
```
public static int TTF
```


TTF (تنسيق الخط TrueType).

### WOFF {#WOFF}
```
public static int WOFF
```


WOFF (تنسيق الخط Web Open Font).

### length {#length}
```
public static int length
```


### fromName(String exportFontFormatName) {#fromName-java.lang.String}
```
public static int fromName(String exportFontFormatName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| exportFontFormatName | java.lang.String |  |

**Returns:**
int
### getName(int exportFontFormat) {#getName-int}
```
public static String getName(int exportFontFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| exportFontFormat | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int exportFontFormat) {#toString-int}
```
public static String toString(int exportFontFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| exportFontFormat | int |  |

**Returns:**
java.lang.String
