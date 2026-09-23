---
title: "StyleCollection"
linktitle: "StyleCollection"
second_title: "Aspose.Words per Java"
description: "Una raccolta di oggetti Style che rappresentano sia gli stili predefiniti sia quelli definiti dall'utente in un documento Java."
type: docs
weight: 642
url: /it/java/com.aspose.words/stylecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class StyleCollection implements Cloneable, Iterable
```

Una raccolta di oggetti [Style](../../com.aspose.words/style/) che rappresentano sia gli stili predefiniti sia quelli definiti dall'utente in un documento.

Per saperne di più, visita l'articolo di documentazione [ Working with Styles and Themes ][Working with Styles and Themes].

 **Examples:** 

Mostra come creare e utilizzare uno stile di paragrafo con formattazione di elenco.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [add(int type, String name)](#add-int-java.lang.String) |  |
| [addCopy(Style style)](#addCopy-com.aspose.words.Style) | Copia uno stile in questa raccolta. |
| [clearQuickStyleGallery()](#clearQuickStyleGallery) | Rimuove tutti gli stili dal pannello della Galleria Stili Rapidi. |
| [get(int index)](#get-int) | Ottiene uno stile per indice. |
| [get(String name)](#get-java.lang.String) | Recupera uno stile dalla raccolta. |
| [getByStyleIdentifier(int sti)](#getByStyleIdentifier-int) |  |
| [getCount()](#getCount) | Ottiene il numero di stili nella raccolta. |
| [getDefaultFont()](#getDefaultFont) | Ottiene la formattazione del testo predefinita del documento. |
| [getDefaultParagraphFormat()](#getDefaultParagraphFormat) | Ottiene la formattazione del paragrafo predefinita del documento. |
| [getDocument()](#getDocument) | Ottiene il documento proprietario. |
| [iterator()](#iterator) | Ottiene un oggetto enumeratore che elencherà gli stili in ordine alfabetico dei loro nomi. |
### add(int type, String name) {#add-int-java.lang.String}
```
public Style add(int type, String name)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tipo | int |  |
| name | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style/)
### addCopy(Style style) {#addCopy-com.aspose.words.Style}
```
public Style addCopy(Style style)
```


Copia uno stile in questa raccolta.

 **Remarks:** 

Lo stile da copiare può appartenere allo stesso documento o a un documento diverso.

Lo stile collegato è copiato.

Questo metodo non copia gli stili di base.

Se la raccolta contiene già uno stile con lo stesso nome, allora il nuovo nome viene generato automaticamente aggiungendo il suffisso \"\\_number\" a partire da 0, ad esempio \"Normal\\_0\", \"Heading 1\\_1\" ecc. Usa il setter [Style.getName()](../../com.aspose.words/style/\#getName) / [Style.setName(java.lang.String)](../../com.aspose.words/style/\#setName-java.lang.String) per modificare il nome dello stile importato.

 **Examples:** 

Mostra come clonare lo stile di un documento.

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

Mostra come importare uno stile da un documento a un documento diverso.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style/) | Stile da copiare. |

**Returns:**
[Style](../../com.aspose.words/style/) - Copied style ready for usage.
### clearQuickStyleGallery() {#clearQuickStyleGallery}
```
public void clearQuickStyleGallery()
```


Rimuove tutti gli stili dal pannello della Galleria Stili Rapidi.

 **Examples:** 

Mostra come rimuovere gli stili dal pannello della Galleria Stili.

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


Ottiene uno stile per indice.

 **Examples:** 

Mostra come aggiungere uno Style alla raccolta di stili di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |

**Returns:**
[Style](../../com.aspose.words/style/) - A style by index.
### get(String name) {#get-java.lang.String}
```
public Style get(String name)
```


Recupera uno stile dalla raccolta.  Ottiene uno stile per nome o alias.

 **Remarks:** 

Sensibile alle maiuscole/minuscole, restituisce  null  se lo stile con il nome specificato non viene trovato.

Se questo è un nome inglese di uno stile predefinito che non esiste ancora, lo crea automaticamente.

 **Examples:** 

Mostra quando ricalcolare il layout della pagina del documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style/) - The corresponding [Style](../../com.aspose.words/style/) value.
### getByStyleIdentifier(int sti) {#getByStyleIdentifier-int}
```
public Style getByStyleIdentifier(int sti)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sti | int |  |

**Returns:**
[Style](../../com.aspose.words/style/)
### getCount() {#getCount}
```
public int getCount()
```


Ottiene il numero di stili nella raccolta.

 **Examples:** 

Mostra come aggiungere uno Style alla raccolta di stili di un documento.

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
int - Il numero di stili nella collezione.
### getDefaultFont() {#getDefaultFont}
```
public Font getDefaultFont()
```


Ottiene la formattazione del testo predefinita del documento.

 **Remarks:** 

Nota che le impostazioni predefinite a livello di documento sono state introdotte in Microsoft Word 2007 e sono supportate pienamente solo nei formati OOXML ( [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX)) . I formati di documento precedenti hanno un supporto limitato per questa funzionalità e possono essere memorizzati solo i nomi dei font.

 **Examples:** 

Mostra come aggiungere uno Style alla raccolta di stili di un documento.

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


Ottiene la formattazione del paragrafo predefinita del documento.

 **Remarks:** 

Nota che le impostazioni predefinite a livello di documento sono state introdotte in Microsoft Word 2007 e sono supportate pienamente solo nei formati OOXML ( [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX)) . I formati di documento precedenti non supportano la formattazione predefinita dei paragrafi a livello di documento.

 **Examples:** 

Mostra come aggiungere uno Style alla raccolta di stili di un documento.

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


Ottiene il documento proprietario.

 **Examples:** 

Mostra come accedere alla raccolta di stili di un documento.

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


Ottiene un oggetto enumeratore che elencherà gli stili in ordine alfabetico dei loro nomi.

 **Examples:** 

Mostra come accedere alla raccolta di stili di un documento.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.util.Iterator
