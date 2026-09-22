---
title: "FontEmbeddingUsagePermissions"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "Aspose.Words لـ Java"
description: "يمثل أذونات استخدام تضمين الخط في Java."
type: docs
weight: 322
url: /ar/java/com.aspose.words/fontembeddingusagepermissions/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingUsagePermissions
```

يمثل أذونات استخدام تضمين الخط.

 **Examples:** 

يوضح كيفية الحصول على معلومات حقوق الترخيص للخطوط المضمنة (FontInfo).

```

 Document doc = new Document(getMyDir() + "Embedded font rights.docx");

 // Get the list of document fonts.
 FontInfoCollection fontInfos = doc.getFontInfos();
 for (FontInfo fontInfo : fontInfos)
 {
     if (fontInfo.getEmbeddingLicensingRights() != null)
     {
         System.out.println(fontInfo.getEmbeddingLicensingRights().getEmbeddingUsagePermissions());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getBitmapEmbeddingOnly());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getNoSubsetting());
     }
 }
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [EDITABLE](#EDITABLE) | يمكن تضمين الخط، وقد يتم تحميله مؤقتًا على أنظمة أخرى. |
| [INSTALLABLE](#INSTALLABLE) | يمكن تضمين الخط، وقد يتم تثبيته بشكل دائم للاستخدام على أنظمة بعيدة، أو للاستخدام من قبل مستخدمين آخرين. |
| [PRINT_AND_PREVIEW](#PRINT-AND-PREVIEW) | يمكن تضمين الخط، وقد يتم تحميله مؤقتًا على أنظمة أخرى لأغراض عرض أو طباعة المستند. |
| [RESTRICTED_LICENSE](#RESTRICTED-LICENSE) | يجب عدم تعديل الخط أو تضمينه أو تبادله بأي طريقة دون الحصول أولاً على إذن صريح من المالك القانوني. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String fontEmbeddingUsagePermissionsName)](#fromName-java.lang.String) |  |
| [getName(int fontEmbeddingUsagePermissions)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontEmbeddingUsagePermissions)](#toString-int) |  |
### EDITABLE {#EDITABLE}
```
public static int EDITABLE
```


يمكن تضمين الخط، وقد يتم تحميله مؤقتًا على أنظمة أخرى.

 **Remarks:** 

كما هو الحال مع تضمين المعاينة والطباعة، يمكن فتح المستندات التي تحتوي على خطوط قابلة للتحرير للقراءة. بالإضافة إلى ذلك، يُسمح بالتحرير، بما في ذلك القدرة على تنسيق نص جديد باستخدام الخط المضمّن، ويمكن حفظ التغييرات.

### INSTALLABLE {#INSTALLABLE}
```
public static int INSTALLABLE
```


يمكن تضمين الخط، وقد يتم تثبيته بشكل دائم للاستخدام على أنظمة بعيدة، أو للاستخدام من قبل مستخدمين آخرين.

### PRINT_AND_PREVIEW {#PRINT-AND-PREVIEW}
```
public static int PRINT_AND_PREVIEW
```


يمكن تضمين الخط، وقد يتم تحميله مؤقتًا على أنظمة أخرى لأغراض عرض أو طباعة المستند.

 **Remarks:** 

يجب فتح المستندات التي تحتوي على خطوط المعاينة والطباعة كـ \u201cread-only\u201d؛ لا يجوز إجراء أي تعديلات على المستند.

### RESTRICTED_LICENSE {#RESTRICTED-LICENSE}
```
public static int RESTRICTED_LICENSE
```


يجب عدم تعديل الخط أو تضمينه أو تبادله بأي طريقة دون الحصول أولاً على إذن صريح من المالك القانوني.

### length {#length}
```
public static int length
```


### fromName(String fontEmbeddingUsagePermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String fontEmbeddingUsagePermissionsName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontEmbeddingUsagePermissionsName | java.lang.String |  |

**Returns:**
int
### getName(int fontEmbeddingUsagePermissions) {#getName-int}
```
public static String getName(int fontEmbeddingUsagePermissions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontEmbeddingUsagePermissions | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontEmbeddingUsagePermissions) {#toString-int}
```
public static String toString(int fontEmbeddingUsagePermissions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontEmbeddingUsagePermissions | int |  |

**Returns:**
java.lang.String
