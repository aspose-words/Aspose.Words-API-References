---
title: "TabStop"
linktitle: "TabStop"
second_title: "Aspose.Words Java için"
description: "Java'da tek bir özel sekme durağını temsil eder."
type: docs
weight: 654
url: /tr/java/com.aspose.words/tabstop/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TabStop implements Cloneable
```

Tek bir özel sekme durağını temsil eder. [TabStop](../../com.aspose.words/tabstop/) nesnesi, [TabStopCollection](../../com.aspose.words/tabstopcollection/) koleksiyonunun bir üyesidir.

Daha fazla bilgi edinmek için, [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Normalde, bir sekme durağı, bir sekme durağının bulunduğu konumu belirtir. Ancak sekme durakları üst stillerden devralınabildiği için, alt nesnenin belirli bir konumda sekme durağı olmadığını açıkça tanımlaması gerekebilir. Belirli bir konumdaki devralınan sekme durağını temizlemek için bir [TabStop](../../com.aspose.words/tabstop/) nesnesi oluşturun ve [getAlignment()](../../com.aspose.words/tabstop/\#getAlignment) / [setAlignment(int)](../../com.aspose.words/tabstop/\#setAlignment-int) değerini [TabAlignment.CLEAR](../../com.aspose.words/tabalignment/\#CLEAR) olarak ayarlayın.

Daha fazla bilgi için [TabStopCollection](../../com.aspose.words/tabstopcollection/) adresine bakın.

 **Examples:** 

TOC ile ilgili paragraflarda sağ sekme durağının konumunu nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [TabStop(double position)](#TabStop-double) | Bu sınıfın yeni bir örneğini başlatır. |
| [TabStop(double position, int alignment, int leader)](#TabStop-double-int-int) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [equals(TabStop rhs)](#equals-com.aspose.words.TabStop) | Belirtilen [TabStop](../../com.aspose.words/tabstop/) ile karşılaştırır. |
| [getAlignment()](#getAlignment) | Bu sekme durağındaki metnin hizalamasını alır. |
| [getLeader()](#getLeader) | Sekme karakterinin altında gösterilen lider çizgi tipini alır. |
| [getPosition()](#getPosition) | Sekme durağının konumunu puan cinsinden alır. |
| [hashCode()](#hashCode) |  |
| [isClear()](#isClear) | Bu sekme durağı, bu konumdaki mevcut sekme duraklarını temizliyorsa  true  döndürür. |
| [setAlignment(int value)](#setAlignment-int) | Bu sekme durağındaki metnin hizalamasını ayarlar. |
| [setLeader(int value)](#setLeader-int) | Sekme karakterinin altında gösterilen lider çizgi tipini ayarlar. |
### TabStop(double position) {#TabStop-double}
```
public TabStop(double position)
```


Bu sınıfın yeni bir örneğini başlatır.

 **Examples:** 

Bir belgenin sekme durakları koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TabStopCollection tabStops = builder.getParagraphFormat().getTabStops();

 // 72 points is one "inch" on the Microsoft Word tab stop ruler.
 tabStops.add(new TabStop(72.0));
 tabStops.add(new TabStop(432, TabAlignment.RIGHT, TabLeader.DASHES));

 Assert.assertEquals(2, tabStops.getCount());
 Assert.assertFalse(tabStops.get(0).isClear());
 Assert.assertFalse(tabStops.get(0).equals(tabStops.get(1)));

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 builder.writeln("Start\tTab 1\tTab 2");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(2, paragraphs.getCount());

 // Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
 Assert.assertEquals(paragraphs.get(0).getParagraphFormat().getTabStops(), paragraphs.get(1).getParagraphFormat().getTabStops());

 // A tab stop collection can point us to TabStops before and after certain positions.
 Assert.assertEquals(72.0, tabStops.before(100.0).getPosition());
 Assert.assertEquals(432.0, tabStops.after(100.0).getPosition());

 // We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
 paragraphs.get(1).getParagraphFormat().getTabStops().clear();

 Assert.assertEquals(0, paragraphs.get(1).getParagraphFormat().getTabStops().getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.TabStopCollection.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| konum | double |  |

### TabStop(double position, int alignment, int leader) {#TabStop-double-int-int}
```
public TabStop(double position, int alignment, int leader)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| konum | double |  |
| hizalama | int |  |
| lider | int |  |

### equals(TabStop rhs) {#equals-com.aspose.words.TabStop}
```
public boolean equals(TabStop rhs)
```


Belirtilen [TabStop](../../com.aspose.words/tabstop/) ile karşılaştırır.

 **Examples:** 

Bir belgenin sekme durakları koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TabStopCollection tabStops = builder.getParagraphFormat().getTabStops();

 // 72 points is one "inch" on the Microsoft Word tab stop ruler.
 tabStops.add(new TabStop(72.0));
 tabStops.add(new TabStop(432, TabAlignment.RIGHT, TabLeader.DASHES));

 Assert.assertEquals(2, tabStops.getCount());
 Assert.assertFalse(tabStops.get(0).isClear());
 Assert.assertFalse(tabStops.get(0).equals(tabStops.get(1)));

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 builder.writeln("Start\tTab 1\tTab 2");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(2, paragraphs.getCount());

 // Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
 Assert.assertEquals(paragraphs.get(0).getParagraphFormat().getTabStops(), paragraphs.get(1).getParagraphFormat().getTabStops());

 // A tab stop collection can point us to TabStops before and after certain positions.
 Assert.assertEquals(72.0, tabStops.before(100.0).getPosition());
 Assert.assertEquals(432.0, tabStops.after(100.0).getPosition());

 // We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
 paragraphs.get(1).getParagraphFormat().getTabStops().clear();

 Assert.assertEquals(0, paragraphs.get(1).getParagraphFormat().getTabStops().getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.TabStopCollection.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| rhs | [TabStop](../../com.aspose.words/tabstop/) |  |

**Returns:**
boolean
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Bu sekme durağındaki metnin hizalamasını alır.

 **Examples:** 

TOC ile ilgili paragraflarda sağ sekme durağının konumunu nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Returns:**
int - Bu sekme durağındaki metnin hizalaması. Döndürülen değer, [TabAlignment](../../com.aspose.words/tabalignment/) sabitlerinden biridir.
### getLeader() {#getLeader}
```
public int getLeader()
```


Sekme karakterinin altında gösterilen lider çizgi tipini alır.

 **Examples:** 

TOC ile ilgili paragraflarda sağ sekme durağının konumunu nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Returns:**
int - Sekme karakterinin altında gösterilen lider çizgi türü. Döndürülen değer, [TabLeader](../../com.aspose.words/tableader/) sabitlerinden biridir.
### getPosition() {#getPosition}
```
public double getPosition()
```


Sekme durağının konumunu puan cinsinden alır.

 **Examples:** 

TOC ile ilgili paragraflarda sağ sekme durağının konumunu nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Returns:**
double - Sekme durağının nokta cinsinden konumu.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isClear() {#isClear}
```
public boolean isClear()
```


Bu sekme durağı, bu konumdaki mevcut sekme duraklarını temizliyorsa  true  döndürür.

 **Examples:** 

Bir belgenin sekme durakları koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TabStopCollection tabStops = builder.getParagraphFormat().getTabStops();

 // 72 points is one "inch" on the Microsoft Word tab stop ruler.
 tabStops.add(new TabStop(72.0));
 tabStops.add(new TabStop(432, TabAlignment.RIGHT, TabLeader.DASHES));

 Assert.assertEquals(2, tabStops.getCount());
 Assert.assertFalse(tabStops.get(0).isClear());
 Assert.assertFalse(tabStops.get(0).equals(tabStops.get(1)));

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 builder.writeln("Start\tTab 1\tTab 2");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(2, paragraphs.getCount());

 // Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
 Assert.assertEquals(paragraphs.get(0).getParagraphFormat().getTabStops(), paragraphs.get(1).getParagraphFormat().getTabStops());

 // A tab stop collection can point us to TabStops before and after certain positions.
 Assert.assertEquals(72.0, tabStops.before(100.0).getPosition());
 Assert.assertEquals(432.0, tabStops.after(100.0).getPosition());

 // We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
 paragraphs.get(1).getParagraphFormat().getTabStops().clear();

 Assert.assertEquals(0, paragraphs.get(1).getParagraphFormat().getTabStops().getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.TabStopCollection.docx");
 
```

**Returns:**
boolean -  true  eğer bu sekme durağı bu konumdaki mevcut sekme duraklarını temizlerse.
### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Bu sekme durağındaki metnin hizalamasını ayarlar.

 **Examples:** 

TOC ile ilgili paragraflarda sağ sekme durağının konumunu nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bu sekme durağındaki metnin hizalaması. Değer, [TabAlignment](../../com.aspose.words/tabalignment/) sabitlerinden biri olmalıdır. |

### setLeader(int value) {#setLeader-int}
```
public void setLeader(int value)
```


Sekme karakterinin altında gösterilen lider çizgi tipini ayarlar.

 **Examples:** 

TOC ile ilgili paragraflarda sağ sekme durağının konumunu nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Sekme karakterinin altında gösterilen lider çizgi türü. Değer, [TabLeader](../../com.aspose.words/tableader/) sabitlerinden biri olmalıdır. |

