---
title: "CompressionLevel"
linktitle: "CompressionLevel"
second_title: "Aspose.Words لـ Java"
description: "مستوى الضغط لملفات OOXML و XPS في Java."
type: docs
weight: 122
url: /ar/java/com.aspose.words/compressionlevel/
---

**Inheritance:**
java.lang.Object
```
public class CompressionLevel
```

مستوى الضغط لملفات OOXML و XPS.

(DOCX، DOTX وملفات XPS هي داخليًا أرشيف ZIP، هذه الخاصية تتحكم في مستوى ضغط الأرشيف.

ملاحظة، أن ملف FlatOpc ليس أرشيف ZIP، لذلك، هذه الخاصية لا تؤثر على ملفات FlatOpc.)

 **Examples:** 

يظهر كيفية تحديد مستوى الضغط لاستخدامه أثناء حفظ مستند OOXML.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
 // and then pass it to the document's saving method to modify how we save the document.
 // Set the "CompressionLevel" property to "CompressionLevel.Maximum" to apply the strongest and slowest compression.
 // Set the "CompressionLevel" property to "CompressionLevel.Normal" to apply
 // the default compression that Aspose.Words uses while saving OOXML documents.
 // Set the "CompressionLevel" property to "CompressionLevel.Fast" to apply a faster and weaker compression.
 // Set the "CompressionLevel" property to "CompressionLevel.SuperFast" to apply
 // the default compression that Microsoft Word uses.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.DOCX);
 saveOptions.setCompressionLevel(compressionLevel);

 StopWatch st = new StopWatch();
 st.start();
 doc.save(getArtifactsDir() + "OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
 st.stop();

 File fileInfo = new File(getArtifactsDir() + "OoxmlSaveOptions.DocumentCompression.docx");

 System.out.println(MessageFormat.format("Saving operation done using the \"{0}\" compression level:", compressionLevel));
 System.out.println(MessageFormat.format("\tDuration:\t{0}", st.getTime()));
 System.out.println(MessageFormat.format("\tFile Size:\t{0} bytes", fileInfo.length()));
 
```

يظهر كيفية التحكم في مستوى الضغط عند حفظ مستند بتنسيق XPS.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Sample document for XPS compression test.");

 // Create an XpsSaveOptions object and set the compression level.
 XpsSaveOptions options = new XpsSaveOptions();
 options.setCompressionLevel(CompressionLevel.MAXIMUM);

 doc.save(getArtifactsDir() + "XpsSaveOptions.CompressionLevelXps.xps", options);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [FAST](#FAST) | مستوى ضغط سريع. |
| [MAXIMUM](#MAXIMUM) | أقصى مستوى ضغط. |
| [NORMAL](#NORMAL) | مستوى ضغط عادي. |
| [SUPER_FAST](#SUPER-FAST) | مستوى ضغط فائق السرعة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String compressionLevelName)](#fromName-java.lang.String) |  |
| [getName(int compressionLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int compressionLevel)](#toString-int) |  |
### FAST {#FAST}
```
public static int FAST
```


مستوى ضغط سريع.

### MAXIMUM {#MAXIMUM}
```
public static int MAXIMUM
```


أقصى مستوى ضغط.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


مستوى ضغط عادي. مستوى الضغط الافتراضي المستخدم من قبل Aspose.Words.

### SUPER_FAST {#SUPER-FAST}
```
public static int SUPER_FAST
```


مستوى ضغط فائق السرعة. يستخدم Microsoft Word هذا المستوى من الضغط.

### length {#length}
```
public static int length
```


### fromName(String compressionLevelName) {#fromName-java.lang.String}
```
public static int fromName(String compressionLevelName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| compressionLevelName | java.lang.String |  |

**Returns:**
int
### getName(int compressionLevel) {#getName-int}
```
public static String getName(int compressionLevel)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| compressionLevel | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int compressionLevel) {#toString-int}
```
public static String toString(int compressionLevel)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| compressionLevel | int |  |

**Returns:**
java.lang.String
