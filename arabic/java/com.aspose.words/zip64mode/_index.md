---
title: "Zip64Mode"
linktitle: "Zip64Mode"
second_title: "Aspose.Words لـ Java"
description: "يحدد متى يتم استخدام امتدادات تنسيق ZIP64 لملفات OOXML في Java."
type: docs
weight: 750
url: /ar/java/com.aspose.words/zip64mode/
---

**Inheritance:**
java.lang.Object
```
public class Zip64Mode
```

يحدد متى يتم استخدام امتدادات تنسيق ZIP64 لملفات OOXML.

 **Remarks:** 

ملف OOXML هو أرشيف ZIP له حد 4 جيجابايت (2^32 بايت) على الحجم غير المضغوط للملف، الحجم المضغوط للملف، وإجمالي حجم الأرشيف، بالإضافة إلى حد 65,535 (2^16-1) ملفًا في الأرشيف. تزيد امتدادات تنسيق ZIP64 من الحدود إلى 2^64.

 **Examples:** 

يظهر كيفية استخدام امتدادات تنسيق ZIP64.

```

 Random random = new Random();
 DocumentBuilder builder = new DocumentBuilder();

 for (int i = 0; i < 10000; i++)
 {
     BufferedImage bmp = new BufferedImage(5, 5, BufferedImage.TYPE_INT_ARGB);
     Graphics2D g = bmp.createGraphics();
     g.setColor(new Color(random.nextInt(254), random.nextInt(254), random.nextInt(254)));
     g.drawImage(bmp, 0, 0, null);
     g.dispose();
     builder.insertImage(bmp);
 }

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setZip64Mode(Zip64Mode.ALWAYS);

 builder.getDocument().save(getArtifactsDir() + "OoxmlSaveOptions.Zip64ModeOption.docx", saveOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [ALWAYS](#ALWAYS) | استخدم دائمًا امتدادات تنسيق ZIP64. |
| [IF_NECESSARY](#IF-NECESSARY) | إذا لزم الأمر، استخدم امتدادات تنسيق ZIP64. |
| [NEVER](#NEVER) | لا تستخدم امتدادات تنسيق ZIP64. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String zip64ModeName)](#fromName-java.lang.String) |  |
| [getName(int zip64Mode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zip64Mode)](#toString-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


استخدم دائمًا امتدادات تنسيق ZIP64.

### IF_NECESSARY {#IF-NECESSARY}
```
public static int IF_NECESSARY
```


إذا لزم الأمر، استخدم امتدادات تنسيق ZIP64.

### NEVER {#NEVER}
```
public static int NEVER
```


لا تستخدم امتدادات تنسيق ZIP64.

### length {#length}
```
public static int length
```


### fromName(String zip64ModeName) {#fromName-java.lang.String}
```
public static int fromName(String zip64ModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| zip64ModeName | java.lang.String |  |

**Returns:**
int
### getName(int zip64Mode) {#getName-int}
```
public static String getName(int zip64Mode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| zip64Mode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int zip64Mode) {#toString-int}
```
public static String toString(int zip64Mode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| zip64Mode | int |  |

**Returns:**
java.lang.String
