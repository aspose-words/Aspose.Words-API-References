---
title: "ToaCategories"
linktitle: "ToaCategories"
second_title: "Aspose.Words für Java"
description: "Stellt eine Tabelle von Autoritätskategorien in Java dar."
type: docs
weight: 689
url: /de/java/com.aspose.words/toacategories/
---

**Inheritance:**
java.lang.Object
```
public class ToaCategories
```

Stellt eine Tabelle von Autoritätskategorien dar.

Weitere Informationen finden Sie im Dokumentationsartikel [ Working with Fields ][Working with Fields].

 **Examples:** 

Zeigt, wie man einen Satz von Kategorien für TOA‑Felder angibt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // TOA fields can filter their entries by categories defined in this collection.
 ToaCategories toaCategories = new ToaCategories();
 doc.getFieldOptions().setToaCategories(toaCategories);

 // This collection of categories comes with default values, which we can overwrite with custom values.
 Assert.assertEquals("Cases", toaCategories.get(1));
 Assert.assertEquals("Statutes", toaCategories.get(2));

 toaCategories.set(1, "My Category 1");
 toaCategories.set(2, "My Category 2");

 // We can always access the default values via this collection.
 Assert.assertEquals("Cases", ToaCategories.getDefaultCategories().get(1));
 Assert.assertEquals("Statutes", ToaCategories.getDefaultCategories().get(2));

 // Insert 2 TOA fields. TOA fields create an entry for each TA field in the document.
 // Use the "\c" switch to select the index of a category from our collection.
 //  With this switch, a TOA field will only pick up entries from TA fields that
 // also have a "\c" switch with a matching category index. Each TOA field will also display
 // the name of the category that its "\c" switch points to.
 builder.insertField("TOA \\c 1 \\h", null);
 builder.insertField("TOA \\c 2 \\h", null);
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Insert TOA entries across 2 categories. Our first TOA field will receive one entry,
 // from the second TA field whose "\c" switch also points to the first category.
 // The second TOA field will have two entries from the other two TA fields.
 builder.insertField("TA \\c 2 \\l \"entry 1\"");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertField("TA \\c 1 \\l \"entry 2\"");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertField("TA \\c 2 \\l \"entry 3\"");

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.TOA.Categories.docx");
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [ToaCategories()](#ToaCategories) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get(int number)](#get-int) | Liefert die Kategorienüberschrift anhand der Kategorienummer. |
| [getDefaultCategories()](#getDefaultCategories) | Liefert die Standardtabelle der Autoritätskategorien. |
| [set(int number, String value)](#set-int-java.lang.String) | Setzt die Kategorienüberschrift anhand der Kategorienummer. |
### ToaCategories() {#ToaCategories}
```
public ToaCategories()
```


Initialisiert eine neue Instanz dieser Klasse.

### get(int number) {#get-int}
```
public String get(int number)
```


Liefert die Kategorienüberschrift anhand der Kategorienummer.

 **Examples:** 

Zeigt, wie man einen Satz von Kategorien für TOA‑Felder angibt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // TOA fields can filter their entries by categories defined in this collection.
 ToaCategories toaCategories = new ToaCategories();
 doc.getFieldOptions().setToaCategories(toaCategories);

 // This collection of categories comes with default values, which we can overwrite with custom values.
 Assert.assertEquals("Cases", toaCategories.get(1));
 Assert.assertEquals("Statutes", toaCategories.get(2));

 toaCategories.set(1, "My Category 1");
 toaCategories.set(2, "My Category 2");

 // We can always access the default values via this collection.
 Assert.assertEquals("Cases", ToaCategories.getDefaultCategories().get(1));
 Assert.assertEquals("Statutes", ToaCategories.getDefaultCategories().get(2));

 // Insert 2 TOA fields. TOA fields create an entry for each TA field in the document.
 // Use the "\c" switch to select the index of a category from our collection.
 //  With this switch, a TOA field will only pick up entries from TA fields that
 // also have a "\c" switch with a matching category index. Each TOA field will also display
 // the name of the category that its "\c" switch points to.
 builder.insertField("TOA \\c 1 \\h", null);
 builder.insertField("TOA \\c 2 \\h", null);
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Insert TOA entries across 2 categories. Our first TOA field will receive one entry,
 // from the second TA field whose "\c" switch also points to the first category.
 // The second TOA field will have two entries from the other two TA fields.
 builder.insertField("TA \\c 2 \\l \"entry 1\"");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertField("TA \\c 1 \\l \"entry 2\"");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertField("TA \\c 2 \\l \"entry 3\"");

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.TOA.Categories.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Nummer | int |  |

**Returns:**
java.lang.String - Die Kategorienüberschrift nach Kategorienummer.
### getDefaultCategories() {#getDefaultCategories}
```
public static ToaCategories getDefaultCategories()
```


Liefert die Standardtabelle der Autoritätskategorien.

 **Remarks:** 

Verwenden Sie die [FieldOptions.getToaCategories()](../../com.aspose.words/fieldoptions/\#getToaCategories) / [FieldOptions.setToaCategories(com.aspose.words.ToaCategories)](../../com.aspose.words/fieldoptions/\#setToaCategories-com.aspose.words.ToaCategories) Eigenschaft, um die Kategorien des Tabellenverzeichnisses für ein einzelnes Dokument anzugeben.

 **Examples:** 

Zeigt, wie man einen Satz von Kategorien für TOA‑Felder angibt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // TOA fields can filter their entries by categories defined in this collection.
 ToaCategories toaCategories = new ToaCategories();
 doc.getFieldOptions().setToaCategories(toaCategories);

 // This collection of categories comes with default values, which we can overwrite with custom values.
 Assert.assertEquals("Cases", toaCategories.get(1));
 Assert.assertEquals("Statutes", toaCategories.get(2));

 toaCategories.set(1, "My Category 1");
 toaCategories.set(2, "My Category 2");

 // We can always access the default values via this collection.
 Assert.assertEquals("Cases", ToaCategories.getDefaultCategories().get(1));
 Assert.assertEquals("Statutes", ToaCategories.getDefaultCategories().get(2));

 // Insert 2 TOA fields. TOA fields create an entry for each TA field in the document.
 // Use the "\c" switch to select the index of a category from our collection.
 //  With this switch, a TOA field will only pick up entries from TA fields that
 // also have a "\c" switch with a matching category index. Each TOA field will also display
 // the name of the category that its "\c" switch points to.
 builder.insertField("TOA \\c 1 \\h", null);
 builder.insertField("TOA \\c 2 \\h", null);
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Insert TOA entries across 2 categories. Our first TOA field will receive one entry,
 // from the second TA field whose "\c" switch also points to the first category.
 // The second TOA field will have two entries from the other two TA fields.
 builder.insertField("TA \\c 2 \\l \"entry 1\"");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertField("TA \\c 1 \\l \"entry 2\"");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertField("TA \\c 2 \\l \"entry 3\"");

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.TOA.Categories.docx");
 
```

**Returns:**
[ToaCategories](../../com.aspose.words/toacategories/) - The default table of authorities categories.
### set(int number, String value) {#set-int-java.lang.String}
```
public void set(int number, String value)
```


Setzt die Kategorienüberschrift anhand der Kategorienummer.

 **Examples:** 

Zeigt, wie man einen Satz von Kategorien für TOA‑Felder angibt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // TOA fields can filter their entries by categories defined in this collection.
 ToaCategories toaCategories = new ToaCategories();
 doc.getFieldOptions().setToaCategories(toaCategories);

 // This collection of categories comes with default values, which we can overwrite with custom values.
 Assert.assertEquals("Cases", toaCategories.get(1));
 Assert.assertEquals("Statutes", toaCategories.get(2));

 toaCategories.set(1, "My Category 1");
 toaCategories.set(2, "My Category 2");

 // We can always access the default values via this collection.
 Assert.assertEquals("Cases", ToaCategories.getDefaultCategories().get(1));
 Assert.assertEquals("Statutes", ToaCategories.getDefaultCategories().get(2));

 // Insert 2 TOA fields. TOA fields create an entry for each TA field in the document.
 // Use the "\c" switch to select the index of a category from our collection.
 //  With this switch, a TOA field will only pick up entries from TA fields that
 // also have a "\c" switch with a matching category index. Each TOA field will also display
 // the name of the category that its "\c" switch points to.
 builder.insertField("TOA \\c 1 \\h", null);
 builder.insertField("TOA \\c 2 \\h", null);
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Insert TOA entries across 2 categories. Our first TOA field will receive one entry,
 // from the second TA field whose "\c" switch also points to the first category.
 // The second TOA field will have two entries from the other two TA fields.
 builder.insertField("TA \\c 2 \\l \"entry 1\"");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertField("TA \\c 1 \\l \"entry 2\"");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertField("TA \\c 2 \\l \"entry 3\"");

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.TOA.Categories.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Nummer | int |  |
| Wert | java.lang.String | Die Kategorienüberschrift nach Kategorienummer. |

