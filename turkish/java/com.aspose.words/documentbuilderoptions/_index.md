---
title: "DocumentBuilderOptions"
linktitle: "DocumentBuilderOptions"
second_title: "Aspose.Words Java için"
description: "Java'da belge oluşturma süreci için ek seçenekler belirtmeye izin verir."
type: docs
weight: 164
url: /tr/java/com.aspose.words/documentbuilderoptions/
---

**Inheritance:**
java.lang.Object
```
public class DocumentBuilderOptions
```

Belge oluşturma süreci için ek seçenekleri belirtmeye izin verir.

 **Examples:** 

Tablo biçimlendirmesini sonrasındaki içerik için nasıl yok sayacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
 builderOptions.setContextTableFormatting(true);
 DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

 // Adds content before the table.
 // Default font size is 12.
 builder.writeln("Font size 12 here.");
 builder.startTable();
 builder.insertCell();
 // Changes the font size inside the table.
 builder.getFont().setSize(5.0);
 builder.write("Font size 5 here");
 builder.insertCell();
 builder.write("Font size 5 here");
 builder.endRow();
 builder.endTable();

 // If ContextTableFormatting is true, then table formatting isn't applied to the content after.
 // If ContextTableFormatting is false, then table formatting is applied to the content after.
 builder.writeln("Font size 12 here.");

 doc.save(getArtifactsDir() + "Table.ContextTableFormatting.docx");
 
```
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getContextTableFormatting()](#getContextTableFormatting) | Tablo içeriğine uygulanan biçimlendirme, ardından gelen içeriğin biçimlendirmesini etkilemiyorsa true. |
| [getDesignMode()](#getDesignMode) | Microsoft Word'deki Tasarım Modu'na karşılık gelir. |
| [setContextTableFormatting(boolean value)](#setContextTableFormatting-boolean) | Tablo içeriğine uygulanan biçimlendirme, ardından gelen içeriğin biçimlendirmesini etkilemiyorsa true. |
| [setDesignMode(boolean value)](#setDesignMode-boolean) | Microsoft Word'deki Tasarım Modu'na karşılık gelir. |
### getContextTableFormatting() {#getContextTableFormatting}
```
public boolean getContextTableFormatting()
```


Tablo içeriğine uygulanan biçimlendirme, ardından gelen içeriğin biçimlendirmesini etkilemiyorsa true. Varsayılan değer  true .

 **Examples:** 

Tablo biçimlendirmesini sonrasındaki içerik için nasıl yok sayacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
 builderOptions.setContextTableFormatting(true);
 DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

 // Adds content before the table.
 // Default font size is 12.
 builder.writeln("Font size 12 here.");
 builder.startTable();
 builder.insertCell();
 // Changes the font size inside the table.
 builder.getFont().setSize(5.0);
 builder.write("Font size 5 here");
 builder.insertCell();
 builder.write("Font size 5 here");
 builder.endRow();
 builder.endTable();

 // If ContextTableFormatting is true, then table formatting isn't applied to the content after.
 // If ContextTableFormatting is false, then table formatting is applied to the content after.
 builder.writeln("Font size 12 here.");

 doc.save(getArtifactsDir() + "Table.ContextTableFormatting.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getDesignMode() {#getDesignMode}
```
public boolean getDesignMode()
```


Microsoft Word'deki Tasarım Modu'na karşılık gelir.

**Returns:**
boolean - İlgili  boolean  değeri.
### setContextTableFormatting(boolean value) {#setContextTableFormatting-boolean}
```
public void setContextTableFormatting(boolean value)
```


Tablo içeriğine uygulanan biçimlendirme, ardından gelen içeriğin biçimlendirmesini etkilemiyorsa true. Varsayılan değer  true .

 **Examples:** 

Tablo biçimlendirmesini sonrasındaki içerik için nasıl yok sayacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
 builderOptions.setContextTableFormatting(true);
 DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

 // Adds content before the table.
 // Default font size is 12.
 builder.writeln("Font size 12 here.");
 builder.startTable();
 builder.insertCell();
 // Changes the font size inside the table.
 builder.getFont().setSize(5.0);
 builder.write("Font size 5 here");
 builder.insertCell();
 builder.write("Font size 5 here");
 builder.endRow();
 builder.endTable();

 // If ContextTableFormatting is true, then table formatting isn't applied to the content after.
 // If ContextTableFormatting is false, then table formatting is applied to the content after.
 builder.writeln("Font size 12 here.");

 doc.save(getArtifactsDir() + "Table.ContextTableFormatting.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setDesignMode(boolean value) {#setDesignMode-boolean}
```
public void setDesignMode(boolean value)
```


Microsoft Word'deki Tasarım Modu'na karşılık gelir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

