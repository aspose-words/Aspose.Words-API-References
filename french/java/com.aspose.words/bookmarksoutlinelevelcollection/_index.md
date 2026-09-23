---
title: "BookmarksOutlineLevelCollection"
linktitle: "BookmarksOutlineLevelCollection"
second_title: "Aspose.Words pour Java"
description: "Une collection des niveaux de plan des signets individuels en Java."
type: docs
weight: 45
url: /fr/java/com.aspose.words/bookmarksoutlinelevelcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BookmarksOutlineLevelCollection implements Iterable
```

Une collection de niveaux de plan de signets individuels.

Pour en savoir plus, consultez l'article de documentation [ Working with Bookmarks ][Working with Bookmarks].

 **Remarks:** 

La clé est un nom de signet sous forme de chaîne insensible à la casse. La valeur est un niveau de plan de signet de type int.

Le niveau de plan du signet peut être une valeur de 0 à 9. Spécifiez 0 et le signet Word ne sera pas affiché dans le plan du document. Spécifiez 1 et le signet Word sera affiché dans le plan du document au niveau 1 ; 2 pour le niveau 2, etc.

 **Examples:** 

Montre comment définir les niveaux de plan pour les signets.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```


[Working with Bookmarks]: https://docs.aspose.com/words/java/working-with-bookmarks/
## Méthodes

| Méthode | Description |
| --- | --- |
| [add(String name, int outlineLevel)](#add-java.lang.String-int) | Ajoute un signet à la collection. |
| [clear()](#clear) | Supprime tous les éléments de la collection. |
| [contains(String name)](#contains-java.lang.String) | Détermine si la collection contient un signet portant le nom donné. |
| [get(int index)](#get-int) | Obtient le niveau de plan d'un signet à l'index spécifié. |
| [get(String name)](#get-java.lang.String) | Fournit l'accès aux éléments de la collection. |
| [getCount()](#getCount) | Obtient le nombre d'éléments contenus dans la collection. |
| [indexOfKey(String name)](#indexOfKey-java.lang.String) | Renvoie l'index basé sur zéro du signet spécifié dans la collection. |
| [iterator()](#iterator) | Renvoie un objet itérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [remove(String name)](#remove-java.lang.String) | Supprime un signet avec le nom spécifié de la collection. |
| [removeAt(int index)](#removeAt-int) | Supprime un signet à l'index spécifié. |
| [set(int index, int value)](#set-int-int) | Définit le niveau de contour d'un signet à l'index spécifié. |
| [set(String name, int value)](#set-java.lang.String-int) | Fournit l'accès aux éléments de la collection. |
### add(String name, int outlineLevel) {#add-java.lang.String-int}
```
public void add(String name, int outlineLevel)
```


Ajoute un signet à la collection.

 **Examples:** 

Montre comment définir les niveaux de plan pour les signets.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom insensible à la casse du signet à ajouter. |
| outlineLevel | int | Le niveau de contour du signet. Plage valide de 0 à 9. |

### clear() {#clear}
```
public void clear()
```


Supprime tous les éléments de la collection.

 **Examples:** 

Montre comment définir les niveaux de plan pour les signets.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Détermine si la collection contient un signet portant le nom donné.

 **Examples:** 

Montre comment définir les niveaux de plan pour les signets.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Nom insensible à la casse du signet à localiser. |

**Returns:**
booléen -  true  si l'élément est trouvé dans la collection ; sinon,  false .
### get(int index) {#get-int}
```
public int get(int index)
```


Obtient le niveau de plan d'un signet à l'index spécifié.

 **Examples:** 

Montre comment définir les niveaux de plan pour les signets.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | Indice basé sur zéro du signet. |

**Returns:**
int - Le niveau de contour du signet. Plage valide de 0 à 9.
### get(String name) {#get-java.lang.String}
```
public int get(String name)
```


Fournit l'accès aux éléments de la collection.  Obtient ou définit un niveau de contour de signet par le nom du signet.

 **Examples:** 

Montre comment définir les niveaux de plan pour les signets.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Nom insensible à la casse du signet. |

**Returns:**
int - Le niveau de contour du signet. Plage valide de 0 à 9.
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre d'éléments contenus dans la collection.

 **Examples:** 

Montre comment définir les niveaux de plan pour les signets.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Returns:**
int - Le nombre d'éléments contenus dans la collection.
### indexOfKey(String name) {#indexOfKey-java.lang.String}
```
public int indexOfKey(String name)
```


Renvoie l'index basé sur zéro du signet spécifié dans la collection.

 **Examples:** 

Montre comment définir les niveaux de plan pour les signets.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom insensible à la casse du signet. |

**Returns:**
int - L'index basé sur zéro. Valeur négative si non trouvé.
### iterator() {#iterator}
```
public Iterator iterator()
```


Renvoie un objet itérateur qui peut être utilisé pour parcourir tous les éléments de la collection.

**Returns:**
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Supprime un signet avec le nom spécifié de la collection.

 **Examples:** 

Montre comment définir les niveaux de plan pour les signets.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom insensible à la casse du signet. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Supprime un signet à l'index spécifié.

 **Examples:** 

Montre comment définir les niveaux de plan pour les signets.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index basé sur zéro. |

### set(int index, int value) {#set-int-int}
```
public void set(int index, int value)
```


Définit le niveau de contour d'un signet à l'index spécifié.

 **Examples:** 

Montre comment définir les niveaux de plan pour les signets.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | Indice basé sur zéro du signet. |
| valeur | int | Le niveau de contour du signet. Plage valide de 0 à 9. |

### set(String name, int value) {#set-java.lang.String-int}
```
public void set(String name, int value)
```


Fournit l'accès aux éléments de la collection.  Obtient ou définit un niveau de contour de signet par le nom du signet.

 **Examples:** 

Montre comment définir les niveaux de plan pour les signets.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Nom insensible à la casse du signet. |
| valeur | int | Le niveau de contour du signet. Plage valide de 0 à 9. |

