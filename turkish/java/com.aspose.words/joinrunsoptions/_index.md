---
title: "JoinRunsOptions"
linktitle: "JoinRunsOptions"
second_title: "Aspose.Words Java için"
description: "Java'da birleştirme çalıştırma işlemi için yapılandırma bayrakları sağlar."
type: docs
weight: 406
url: /tr/java/com.aspose.words/joinrunsoptions/
---

**Inheritance:**
java.lang.Object
```
public class JoinRunsOptions
```

Koşulları birleştirme işlemi için yapılandırma bayrakları sağlar.

 **Examples:** 

Gereksiz ve önemsiz öznitelikler göz ardı edilerek aynı biçimlendirmeye sahip çalıştırmaların nasıl birleştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create runs with identical visible formatting but some internal differences.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(12.0);
 builder.write("Hello ");
 builder.write("world");

 // Verify runs before join.
 Assert.assertEquals(2, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello ", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());
 Assert.assertEquals("world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(1).getText());

 // Configure options to ignore redundant and insignificant attributes during join.
 JoinRunsOptions options = new JoinRunsOptions();
 options.setIgnoreRedundant(true); // Ignore redundant run properties that don't affect appearance.
 options.setIgnoreInsignificant(true); // Ignore insignificant differences like whitespace-only runs.

 // Join runs that have the same visible formatting using the extended options.
 doc.getFirstSection().getBody().getFirstParagraph().joinRunsWithSameFormatting(options);

 // Verify that runs were successfully joined.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());

 doc.save(getArtifactsDir() + "Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
 
```
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getIgnoreInsignificant()](#getIgnoreInsignificant) | True, aynı biçimlendirme sahip çalıştırmalar birleştirildiğinde tüm çalıştırmaların önemsiz özniteliklerinin göz ardı edileceğini gösterir. |
| [getIgnoreRedundant()](#getIgnoreRedundant) | True, aynı biçimlendirme sahip çalıştırmalar birleştirildiğinde tüm çalıştırmaların gereksiz özniteliklerinin göz ardı edileceğini gösterir. |
| [getIgnoreSpacing()](#getIgnoreSpacing) | True, aynı biçimlendirme sahip çalıştırmalar birleştirildiğinde tüm çalıştırmaların boşluk özniteliklerinin göz ardı edileceğini gösterir. |
| [setIgnoreInsignificant(boolean value)](#setIgnoreInsignificant-boolean) | True, aynı biçimlendirme sahip çalıştırmalar birleştirildiğinde tüm çalıştırmaların önemsiz özniteliklerinin göz ardı edileceğini gösterir. |
| [setIgnoreRedundant(boolean value)](#setIgnoreRedundant-boolean) | True, aynı biçimlendirme sahip çalıştırmalar birleştirildiğinde tüm çalıştırmaların gereksiz özniteliklerinin göz ardı edileceğini gösterir. |
| [setIgnoreSpacing(boolean value)](#setIgnoreSpacing-boolean) | True, aynı biçimlendirme sahip çalıştırmalar birleştirildiğinde tüm çalıştırmaların boşluk özniteliklerinin göz ardı edileceğini gösterir. |
### getIgnoreInsignificant() {#getIgnoreInsignificant}
```
public boolean getIgnoreInsignificant()
```


True, aynı biçimlendirme sahip çalıştırmalar birleştirildiğinde tüm çalıştırmaların önemsiz özniteliklerinin göz ardı edileceğini gösterir.

 **Remarks:** 

Önemli olmayan öznitelikler, verilen metin içeriğine sahip bir çalıştırmanın biçimlendirmesi üzerinde belirgin bir etkisi olmayan özniteliklerdir. Varsayılan değer False'tur.

**Returns:**
boolean - İlgili  boolean  değeri.
### getIgnoreRedundant() {#getIgnoreRedundant}
```
public boolean getIgnoreRedundant()
```


True, aynı biçimlendirme sahip çalıştırmalar birleştirildiğinde tüm çalıştırmaların gereksiz özniteliklerinin göz ardı edileceğini gösterir.

 **Remarks:** 

Gereksiz öznitelikler, verilen metin içeriğine sahip çalıştırmayı etkilemeyen özniteliklerdir. Varsayılan değer False'tur.

**Returns:**
boolean - İlgili  boolean  değeri.
### getIgnoreSpacing() {#getIgnoreSpacing}
```
public boolean getIgnoreSpacing()
```


True, aynı biçimlendirme sahip çalıştırmalar birleştirildiğinde tüm çalıştırmaların boşluk özniteliklerinin göz ardı edileceğini gösterir.

 **Remarks:** 

Varsayılan değer False'tur.

**Returns:**
boolean - İlgili  boolean  değeri.
### setIgnoreInsignificant(boolean value) {#setIgnoreInsignificant-boolean}
```
public void setIgnoreInsignificant(boolean value)
```


True, aynı biçimlendirme sahip çalıştırmalar birleştirildiğinde tüm çalıştırmaların önemsiz özniteliklerinin göz ardı edileceğini gösterir.

 **Remarks:** 

Önemli olmayan öznitelikler, verilen metin içeriğine sahip bir çalıştırmanın biçimlendirmesi üzerinde belirgin bir etkisi olmayan özniteliklerdir. Varsayılan değer False'tur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setIgnoreRedundant(boolean value) {#setIgnoreRedundant-boolean}
```
public void setIgnoreRedundant(boolean value)
```


True, aynı biçimlendirme sahip çalıştırmalar birleştirildiğinde tüm çalıştırmaların gereksiz özniteliklerinin göz ardı edileceğini gösterir.

 **Remarks:** 

Gereksiz öznitelikler, verilen metin içeriğine sahip çalıştırmayı etkilemeyen özniteliklerdir. Varsayılan değer False'tur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setIgnoreSpacing(boolean value) {#setIgnoreSpacing-boolean}
```
public void setIgnoreSpacing(boolean value)
```


True, aynı biçimlendirme sahip çalıştırmalar birleştirildiğinde tüm çalıştırmaların boşluk özniteliklerinin göz ardı edileceğini gösterir.

 **Remarks:** 

Varsayılan değer False'tur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

