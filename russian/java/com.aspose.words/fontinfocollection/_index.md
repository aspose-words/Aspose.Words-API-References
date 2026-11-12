---
title: "FontInfoCollection"
linktitle: "FontInfoCollection"
second_title: "Aspose.Words для Java"
description: "Представляет собой коллекцию шрифтов, используемых в документе на Java."
type: docs
weight: 327
url: /ru/java/com.aspose.words/fontinfocollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class FontInfoCollection implements Iterable
```

Представляет коллекцию шрифтов, используемых в документе.

Чтобы узнать больше, посетите статью документации [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

Элементы являются объектами [FontInfo](../../com.aspose.words/fontinfo/).

Вы не создаёте экземпляры этого класса напрямую. Используйте свойство [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) для доступа к коллекции шрифтов, определённых в документе.

 **Examples:** 

Показывает, как вывести детали о шрифтах, присутствующих в документе.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfoCollection allFonts = doc.getFontInfos();
 // Print all the used and unused fonts in the document.
 for (int i = 0; i < allFonts.getCount(); i++) {
     System.out.println("Font index #{i}");
     System.out.println("\tName: {allFonts[i].Name}");
 }
 
```

Показывает, как сохранить документ со встроенными TrueType‑шрифтами.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Методы

| Метод | Описание |
| --- | --- |
| [contains(String name)](#contains-java.lang.String) | Определяет, содержит ли коллекция шрифт с указанным именем. |
| [get(int index)](#get-int) | Получает шрифт по указанному индексу. |
| [get(String name)](#get-java.lang.String) | Обеспечивает доступ к элементам коллекции. |
| [getCount()](#getCount) | Получает количество элементов, содержащихся в коллекции. |
| [getEmbedSystemFonts()](#getEmbedSystemFonts) | Указывает, следует ли встраивать системные шрифты в документ. |
| [getEmbedTrueTypeFonts()](#getEmbedTrueTypeFonts) | Указывает, следует ли встраивать TrueType‑шрифты в документ при его сохранении. |
| [getSaveSubsetFonts()](#getSaveSubsetFonts) | Указывает, следует ли сохранять подмножество встроенных TrueType‑шрифтов вместе с документом. |
| [iterator()](#iterator) | Возвращает объект-итератор, который можно использовать для перебора всех элементов в коллекции. |
| [setEmbedSystemFonts(boolean value)](#setEmbedSystemFonts-boolean) | Указывает, следует ли встраивать системные шрифты в документ. |
| [setEmbedTrueTypeFonts(boolean value)](#setEmbedTrueTypeFonts-boolean) | Указывает, следует ли встраивать TrueType‑шрифты в документ при его сохранении. |
| [setSaveSubsetFonts(boolean value)](#setSaveSubsetFonts-boolean) | Указывает, следует ли сохранять подмножество встроенных TrueType‑шрифтов вместе с документом. |
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Определяет, содержит ли коллекция шрифт с указанным именем.

 **Examples:** 

Показывает информацию о шрифтах, присутствующих в пустом документе.

```

 Document doc = new Document();

 // A blank document contains 3 default fonts. Each font in the document
 // will have a corresponding FontInfo object which contains details about that font.
 Assert.assertEquals(3, doc.getFontInfos().getCount());

 Assert.assertTrue(doc.getFontInfos().contains("Times New Roman"));
 Assert.assertEquals(204, doc.getFontInfos().get("Times New Roman").getCharset());

 Assert.assertTrue(doc.getFontInfos().contains("Symbol"));
 Assert.assertTrue(doc.getFontInfos().contains("Arial"));
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Регистронезависимое имя шрифта для поиска. |

**Returns:**
boolean -  true  если элемент найден в коллекции; иначе,  false .
### get(int index) {#get-int}
```
public FontInfo get(int index)
```


Получает шрифт по указанному индексу.

 **Examples:** 

Показывает, как извлечь встроенный шрифт из документа и сохранить его в локальную файловую систему.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Нулевой индекс шрифта. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - A font at the specified index.
### get(String name) {#get-java.lang.String}
```
public FontInfo get(String name)
```


Обеспечивает доступ к элементам коллекции.  Получает шрифт с указанным именем.

 **Examples:** 

Показывает, как извлечь встроенный шрифт из документа и сохранить его в локальную файловую систему.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Регистронезависимое имя шрифта для поиска. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - The corresponding [FontInfo](../../com.aspose.words/fontinfo/) value.
### getCount() {#getCount}
```
public int getCount()
```


Получает количество элементов, содержащихся в коллекции.

 **Examples:** 

Показывает информацию о шрифтах, присутствующих в пустом документе.

```

 Document doc = new Document();

 // A blank document contains 3 default fonts. Each font in the document
 // will have a corresponding FontInfo object which contains details about that font.
 Assert.assertEquals(3, doc.getFontInfos().getCount());

 Assert.assertTrue(doc.getFontInfos().contains("Times New Roman"));
 Assert.assertEquals(204, doc.getFontInfos().get("Times New Roman").getCharset());

 Assert.assertTrue(doc.getFontInfos().contains("Symbol"));
 Assert.assertTrue(doc.getFontInfos().contains("Arial"));
 
```

**Returns:**
int — количество элементов, содержащихся в коллекции.
### getEmbedSystemFonts() {#getEmbedSystemFonts}
```
public boolean getEmbedSystemFonts()
```


Указывает, следует ли встраивать системные шрифты в документ. Значение свойства по умолчанию — false.

Эта опция работает только когда параметр [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) установлен в true.

 **Remarks:** 

Установка этого свойства в true полезна, если пользователь работает на системе Восточной Азии и хочет создать документ, читаемый другими, у кого на системе нет шрифтов для этого языка. Например, пользователь японской системы может выбрать встраивание шрифтов в документ, чтобы японский документ был читаем на всех системах.

Эта опция работает только с форматами DOC, DOCX и RTF.

 **Examples:** 

Показывает, как сохранить документ со встроенными TrueType‑шрифтами.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getEmbedTrueTypeFonts() {#getEmbedTrueTypeFonts}
```
public boolean getEmbedTrueTypeFonts()
```


Указывает, следует ли встраивать TrueType‑шрифты в документ при его сохранении. Значение свойства по умолчанию — false.

 **Remarks:** 

Встраивание TrueType‑шрифтов позволяет другим просматривать документ теми же шрифтами, которые использовались при его создании, но может существенно увеличить размер документа.

Эта опция работает только с форматами DOC, DOCX и RTF.

 **Examples:** 

Показывает, как сохранить документ со встроенными TrueType‑шрифтами.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getSaveSubsetFonts() {#getSaveSubsetFonts}
```
public boolean getSaveSubsetFonts()
```


Указывает, следует ли сохранять подмножество встроенных TrueType‑шрифтов вместе с документом. Значение свойства по умолчанию — false.

Эта опция работает только когда свойство [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) установлено в true.

 **Remarks:** 

Эта опция работает только с форматами DOC, DOCX и RTF.

 **Examples:** 

Показывает, как сохранить документ со встроенными TrueType‑шрифтами.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### iterator() {#iterator}
```
public Iterator iterator()
```


Возвращает объект-итератор, который можно использовать для перебора всех элементов в коллекции.

 **Examples:** 

Показывает, как получить доступ и вывести детали каждого шрифта в документе.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Iterator fontCollectionEnumerator = doc.getFontInfos().iterator();
 while (fontCollectionEnumerator.hasNext()) {
     FontInfo fontInfo = fontCollectionEnumerator.next();
     if (fontInfo != null) {
         System.out.println("Font name: " + fontInfo.getName());

         // Alt names are usually blank.
         System.out.println("Alt name: " + fontInfo.getAltName());
         System.out.println("\t- Family: " + fontInfo.getFamily());
         System.out.println("\t- " + (fontInfo.isTrueType() ? "Is TrueType" : "Is not TrueType"));
         System.out.println("\t- Pitch: " + fontInfo.getPitch());
         System.out.println("\t- Charset: " + fontInfo.getCharset());
         System.out.println("\t- Panose:");
         System.out.println("\t\tFamily Kind: " + (fontInfo.getPanose()[0] & 0xFF));
         System.out.println("\t\tSerif Style: " + (fontInfo.getPanose()[1] & 0xFF));
         System.out.println("\t\tWeight: " + (fontInfo.getPanose()[2] & 0xFF));
         System.out.println("\t\tProportion: " + (fontInfo.getPanose()[3] & 0xFF));
         System.out.println("\t\tContrast: " + (fontInfo.getPanose()[4] & 0xFF));
         System.out.println("\t\tStroke Variation: " + (fontInfo.getPanose()[5] & 0xFF));
         System.out.println("\t\tArm Style: " + (fontInfo.getPanose()[6] & 0xFF));
         System.out.println("\t\tLetterform: " + (fontInfo.getPanose()[7] & 0xFF));
         System.out.println("\t\tMidline: " + (fontInfo.getPanose()[8] & 0xFF));
         System.out.println("\t\tX-Height: " + (fontInfo.getPanose()[9] & 0xFF));
     }
 }
 
```

**Returns:**
java.util.Iterator
### setEmbedSystemFonts(boolean value) {#setEmbedSystemFonts-boolean}
```
public void setEmbedSystemFonts(boolean value)
```


Указывает, следует ли встраивать системные шрифты в документ. Значение свойства по умолчанию — false.

Эта опция работает только когда параметр [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) установлен в true.

 **Remarks:** 

Установка этого свойства в true полезна, если пользователь работает на системе Восточной Азии и хочет создать документ, читаемый другими, у кого на системе нет шрифтов для этого языка. Например, пользователь японской системы может выбрать встраивание шрифтов в документ, чтобы японский документ был читаем на всех системах.

Эта опция работает только с форматами DOC, DOCX и RTF.

 **Examples:** 

Показывает, как сохранить документ со встроенными TrueType‑шрифтами.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setEmbedTrueTypeFonts(boolean value) {#setEmbedTrueTypeFonts-boolean}
```
public void setEmbedTrueTypeFonts(boolean value)
```


Указывает, следует ли встраивать TrueType‑шрифты в документ при его сохранении. Значение свойства по умолчанию — false.

 **Remarks:** 

Встраивание TrueType‑шрифтов позволяет другим просматривать документ теми же шрифтами, которые использовались при его создании, но может существенно увеличить размер документа.

Эта опция работает только с форматами DOC, DOCX и RTF.

 **Examples:** 

Показывает, как сохранить документ со встроенными TrueType‑шрифтами.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setSaveSubsetFonts(boolean value) {#setSaveSubsetFonts-boolean}
```
public void setSaveSubsetFonts(boolean value)
```


Указывает, следует ли сохранять подмножество встроенных TrueType‑шрифтов вместе с документом. Значение свойства по умолчанию — false.

Эта опция работает только когда свойство [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) установлено в true.

 **Remarks:** 

Эта опция работает только с форматами DOC, DOCX и RTF.

 **Examples:** 

Показывает, как сохранить документ со встроенными TrueType‑шрифтами.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

