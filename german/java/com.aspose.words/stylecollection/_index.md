---
title: "StyleCollection"
linktitle: "StyleCollection"
second_title: "Aspose.Words für Java"
description: "Eine Sammlung von Style-Objekten, die sowohl die integrierten als auch benutzerdefinierten Stile in einem Dokument in Java darstellen."
type: docs
weight: 642
url: /de/java/com.aspose.words/stylecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class StyleCollection implements Cloneable, Iterable
```

Eine Sammlung von [Style](../../com.aspose.words/style/) Objekten, die sowohl die integrierten als auch benutzerdefinierten Stile in einem Dokument darstellen.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Styles and Themes ][Working with Styles and Themes].

 **Examples:** 

Zeigt, wie man einen Absatzstil mit Listformatierung erstellt und verwendet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```


[Working with Styles and Themes]: https://docs.aspose.com/words/java/working-with-styles-and-themes/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(int type, String name)](#add-int-java.lang.String) |  |
| [addCopy(Style style)](#addCopy-com.aspose.words.Style) | Kopiert einen Stil in diese Sammlung. |
| [clearQuickStyleGallery()](#clearQuickStyleGallery) | Entfernt alle Stile aus dem Quick Style Gallery-Panel. |
| [get(int index)](#get-int) | Liefert einen Stil nach Index. |
| [get(String name)](#get-java.lang.String) | Ruft einen Stil aus der Sammlung ab. |
| [getByStyleIdentifier(int sti)](#getByStyleIdentifier-int) |  |
| [getCount()](#getCount) | Liefert die Anzahl der Stile in der Sammlung. |
| [getDefaultFont()](#getDefaultFont) | Liefert die standardmäßige Textformatierung des Dokuments. |
| [getDefaultParagraphFormat()](#getDefaultParagraphFormat) | Liefert die standardmäßige Absatzformatierung des Dokuments. |
| [getDocument()](#getDocument) | Ruft das zugehörige Dokument ab. |
| [iterator()](#iterator) | Liefert ein Enumerator-Objekt, das die Stile in alphabetischer Reihenfolge ihrer Namen aufzählt. |
### add(int type, String name) {#add-int-java.lang.String}
```
public Style add(int type, String name)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Typ | int |  |
| name | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style/)
### addCopy(Style style) {#addCopy-com.aspose.words.Style}
```
public Style addCopy(Style style)
```


Kopiert einen Stil in diese Sammlung.

 **Remarks:** 

Der zu kopierende Stil kann zum selben Dokument wie auch zu einem anderen Dokument gehören.

Verknüpfter Stil wird kopiert.

Diese Methode kopiert keine Basisstile.

Wenn die Sammlung bereits einen Stil mit demselben Namen enthält, wird ein neuer Name automatisch erzeugt, indem das Suffix "\\_number" ab 0 hinzugefügt wird, z. B. "Normal\\_0", "Heading 1\\_1" usw. Verwenden Sie den Setter [Style.getName()](../../com.aspose.words/style/\\#getName) / [Style.setName(java.lang.String)](../../com.aspose.words/style/\\#setName-java.lang.String), um den Namen des importierten Stils zu ändern.

 **Examples:** 

Zeigt, wie man den Stil eines Dokuments klont.

```

 Document doc = new Document();

 // The AddCopy method creates a copy of the specified style and
 // automatically generates a new name for the style, such as "Heading 1_0".
 Style newStyle = doc.getStyles().addCopy(doc.getStyles().get("Heading 1"));

 // Use the style's "Name" property to change the style's identifying name.
 newStyle.setName("My Heading 1");

 // Our document now has two identical looking styles with different names.
 // Changing settings of one of the styles do not affect the other.
 newStyle.getFont().setColor(Color.RED);

 Assert.assertEquals("My Heading 1", newStyle.getName());
 Assert.assertEquals("Heading 1", doc.getStyles().get("Heading 1").getName());

 Assert.assertEquals(doc.getStyles().get("Heading 1").getType(), newStyle.getType());
 Assert.assertEquals(doc.getStyles().get("Heading 1").getFont().getName(), newStyle.getFont().getName());
 Assert.assertEquals(doc.getStyles().get("Heading 1").getFont().getSize(), newStyle.getFont().getSize());
 Assert.assertNotEquals(doc.getStyles().get("Heading 1").getFont().getColor(), newStyle.getFont().getColor());
 
```

Zeigt, wie man einen Stil von einem Dokument in ein anderes Dokument importiert.

```

 Document srcDoc = new Document();

 // Create a custom style for the source document.
 Style srcStyle = srcDoc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 srcStyle.getFont().setColor(Color.RED);

 // Import the source document's custom style into the destination document.
 Document dstDoc = new Document();
 Style newStyle = dstDoc.getStyles().addCopy(srcStyle);

 // The imported style has an appearance identical to its source style.
 Assert.assertEquals("MyStyle", newStyle.getName());
 Assert.assertEquals(Color.RED.getRGB(), newStyle.getFont().getColor().getRGB());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style/) | Zu kopierender Stil. |

**Returns:**
[Style](../../com.aspose.words/style/) - Copied style ready for usage.
### clearQuickStyleGallery() {#clearQuickStyleGallery}
```
public void clearQuickStyleGallery()
```


Entfernt alle Stile aus dem Quick Style Gallery-Panel.

 **Examples:** 

Zeigt, wie man Stile aus dem Style Gallery-Panel entfernt.

```

 Document doc = new Document();

 // Note that remove styles work only with DOCX format for now.
 doc.getStyles().clearQuickStyleGallery();

 doc.save(getArtifactsDir() + "Styles.RemoveStylesFromStyleGallery.docx");
 
```

### get(int index) {#get-int}
```
public Style get(int index)
```


Liefert einen Stil nach Index.

 **Examples:** 

Zeigt, wie man einen Stil zur Stilsammlung eines Dokuments hinzufügt.

```

 Document doc = new Document();

 // Set default parameters for new styles that we may later add to this collection.
 StyleCollection styles = doc.getStyles();
 styles.getDefaultFont().setName("Courier New");

 // If we add a style of the "StyleType.Paragraph", the collection will apply the values of
 // its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
 styles.getDefaultParagraphFormat().setFirstLineIndent(15.0);

 // Add a style, and then verify that it has the default settings.
 styles.add(StyleType.PARAGRAPH, "MyStyle");

 Assert.assertEquals("Courier New", styles.get(4).getFont().getName());
 Assert.assertEquals(15.0, styles.get("MyStyle").getParagraphFormat().getFirstLineIndent());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |

**Returns:**
[Style](../../com.aspose.words/style/) - A style by index.
### get(String name) {#get-java.lang.String}
```
public Style get(String name)
```


Ruft einen Stil aus der Sammlung ab.  Holt einen Stil anhand des Namens oder eines Alias.

 **Remarks:** 

Groß-/Kleinschreibung beachten, gibt  null  zurück, wenn der Stil mit dem angegebenen Namen nicht gefunden wird.

Wenn dies ein englischer Name eines integrierten Stils ist, der noch nicht existiert, wird er automatisch erstellt.

 **Examples:** 

Zeigt, wann das Seitenlayout des Dokuments neu berechnet werden soll.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Saving a document to PDF, to an image, or printing for the first time will automatically
 // cache the layout of the document within its pages.
 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.1.pdf");

 // Modify the document in some way.
 doc.getStyles().get("Normal").getFont().setSize(6.0);
 doc.getSections().get(0).getPageSetup().setOrientation(Orientation.LANDSCAPE);
 doc.getSections().get(0).getPageSetup().setMargins(Margins.MIRRORED);

 // In the current version of Aspose.Words, modifying the document does not automatically rebuild
 // the cached page layout. If we wish for the cached layout
 // to stay up to date, we will need to update it manually.
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.2.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style/) - The corresponding [Style](../../com.aspose.words/style/) value.
### getByStyleIdentifier(int sti) {#getByStyleIdentifier-int}
```
public Style getByStyleIdentifier(int sti)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sti | int |  |

**Returns:**
[Style](../../com.aspose.words/style/)
### getCount() {#getCount}
```
public int getCount()
```


Liefert die Anzahl der Stile in der Sammlung.

 **Examples:** 

Zeigt, wie man einen Stil zur Stilsammlung eines Dokuments hinzufügt.

```

 Document doc = new Document();

 // Set default parameters for new styles that we may later add to this collection.
 StyleCollection styles = doc.getStyles();
 styles.getDefaultFont().setName("Courier New");

 // If we add a style of the "StyleType.Paragraph", the collection will apply the values of
 // its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
 styles.getDefaultParagraphFormat().setFirstLineIndent(15.0);

 // Add a style, and then verify that it has the default settings.
 styles.add(StyleType.PARAGRAPH, "MyStyle");

 Assert.assertEquals("Courier New", styles.get(4).getFont().getName());
 Assert.assertEquals(15.0, styles.get("MyStyle").getParagraphFormat().getFirstLineIndent());
 
```

**Returns:**
int - Die Anzahl der Stile in der Sammlung.
### getDefaultFont() {#getDefaultFont}
```
public Font getDefaultFont()
```


Liefert die standardmäßige Textformatierung des Dokuments.

 **Remarks:** 

Beachten Sie, dass dokumentweite Vorgaben in Microsoft Word 2007 eingeführt wurden und nur in OOXML‑Formaten ( [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX)) vollständig unterstützt werden. Ältere Dokumentformate unterstützen diese Funktion nur eingeschränkt und können lediglich Schriftartnamen speichern.

 **Examples:** 

Zeigt, wie man einen Stil zur Stilsammlung eines Dokuments hinzufügt.

```

 Document doc = new Document();

 // Set default parameters for new styles that we may later add to this collection.
 StyleCollection styles = doc.getStyles();
 styles.getDefaultFont().setName("Courier New");

 // If we add a style of the "StyleType.Paragraph", the collection will apply the values of
 // its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
 styles.getDefaultParagraphFormat().setFirstLineIndent(15.0);

 // Add a style, and then verify that it has the default settings.
 styles.add(StyleType.PARAGRAPH, "MyStyle");

 Assert.assertEquals("Courier New", styles.get(4).getFont().getName());
 Assert.assertEquals(15.0, styles.get("MyStyle").getParagraphFormat().getFirstLineIndent());
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - Document default text formatting.
### getDefaultParagraphFormat() {#getDefaultParagraphFormat}
```
public ParagraphFormat getDefaultParagraphFormat()
```


Liefert die standardmäßige Absatzformatierung des Dokuments.

 **Remarks:** 

Beachten Sie, dass dokumentweite Vorgaben in Microsoft Word 2007 eingeführt wurden und nur in OOXML‑Formaten ( [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX)) vollständig unterstützt werden. Ältere Dokumentformate unterstützen die standardmäßige Absatzformatierung des Dokuments nicht.

 **Examples:** 

Zeigt, wie man einen Stil zur Stilsammlung eines Dokuments hinzufügt.

```

 Document doc = new Document();

 // Set default parameters for new styles that we may later add to this collection.
 StyleCollection styles = doc.getStyles();
 styles.getDefaultFont().setName("Courier New");

 // If we add a style of the "StyleType.Paragraph", the collection will apply the values of
 // its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
 styles.getDefaultParagraphFormat().setFirstLineIndent(15.0);

 // Add a style, and then verify that it has the default settings.
 styles.add(StyleType.PARAGRAPH, "MyStyle");

 Assert.assertEquals("Courier New", styles.get(4).getFont().getName());
 Assert.assertEquals(15.0, styles.get("MyStyle").getParagraphFormat().getFirstLineIndent());
 
```

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - Document default paragraph formatting.
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Ruft das zugehörige Dokument ab.

 **Examples:** 

Zeigt, wie auf die Stilsammlung eines Dokuments zugegriffen wird.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The owner document.
### iterator() {#iterator}
```
public Iterator iterator()
```


Liefert ein Enumerator-Objekt, das die Stile in alphabetischer Reihenfolge ihrer Namen aufzählt.

 **Examples:** 

Zeigt, wie auf die Stilsammlung eines Dokuments zugegriffen wird.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.util.Iterator
