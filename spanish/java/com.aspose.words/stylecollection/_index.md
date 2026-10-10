---
title: "StyleCollection"
linktitle: "StyleCollection"
second_title: "Aspose.Words para Java"
description: "Una colección de objetos Style que representan tanto los estilos incorporados como los definidos por el usuario en un documento en Java."
type: docs
weight: 642
url: /es/java/com.aspose.words/stylecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class StyleCollection implements Cloneable, Iterable
```

Una colección de [Style](../../com.aspose.words/style/) objetos que representan tanto los estilos incorporados como los definidos por el usuario en un documento.

Para obtener más información, visite el artículo de documentación [ Working with Styles and Themes ][Working with Styles and Themes].

 **Examples:** 

Muestra cómo crear y usar un estilo de párrafo con formato de lista.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [add(int type, String name)](#add-int-java.lang.String) |  |
| [addCopy(Style style)](#addCopy-com.aspose.words.Style) | Copia un estilo en esta colección. |
| [clearQuickStyleGallery()](#clearQuickStyleGallery) | Elimina todos los estilos del panel de la Galería de Estilos Rápidos. |
| [get(int index)](#get-int) | Obtiene un estilo por índice. |
| [get(String name)](#get-java.lang.String) | Recupera un estilo de la colección. |
| [getByStyleIdentifier(int sti)](#getByStyleIdentifier-int) |  |
| [getCount()](#getCount) | Obtiene el número de estilos en la colección. |
| [getDefaultFont()](#getDefaultFont) | Obtiene el formato de texto predeterminado del documento. |
| [getDefaultParagraphFormat()](#getDefaultParagraphFormat) | Obtiene el formato de párrafo predeterminado del documento. |
| [getDocument()](#getDocument) | Obtiene el documento propietario. |
| [iterator()](#iterator) | Obtiene un objeto enumerador que enumerará los estilos en orden alfabético de sus nombres. |
### add(int type, String name) {#add-int-java.lang.String}
```
public Style add(int type, String name)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tipo | int |  |
| nombre | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style/)
### addCopy(Style style) {#addCopy-com.aspose.words.Style}
```
public Style addCopy(Style style)
```


Copia un estilo en esta colección.

 **Remarks:** 

El estilo a copiar puede pertenecer al mismo documento así como a un documento diferente.

Se copia el estilo vinculado.

Este método no copia los estilos base.

Si la colección ya contiene un estilo con el mismo nombre, entonces se genera automáticamente un nuevo nombre añadiendo el sufijo "\_number" a partir de 0, p.ej. "Normal\_0", "Heading 1\_1", etc. Utilice el setter [Style.getName()](../../com.aspose.words/style/\#getName) / [Style.setName(java.lang.String)](../../com.aspose.words/style/\#setName-java.lang.String) para cambiar el nombre del estilo importado.

 **Examples:** 

Muestra cómo clonar el estilo de un documento.

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

Muestra cómo importar un estilo de un documento a otro documento diferente.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style/) | Estilo a copiar. |

**Returns:**
[Style](../../com.aspose.words/style/) - Copied style ready for usage.
### clearQuickStyleGallery() {#clearQuickStyleGallery}
```
public void clearQuickStyleGallery()
```


Elimina todos los estilos del panel de la Galería de Estilos Rápidos.

 **Examples:** 

Muestra cómo eliminar estilos del panel de la Galería de Estilos.

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


Obtiene un estilo por índice.

 **Examples:** 

Muestra cómo agregar un Style a la colección de estilos de un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

**Returns:**
[Style](../../com.aspose.words/style/) - A style by index.
### get(String name) {#get-java.lang.String}
```
public Style get(String name)
```


Recupera un estilo de la colección.  Obtiene un estilo por nombre o alias.

 **Remarks:** 

Sensible a mayúsculas y minúsculas, devuelve  null  si no se encuentra el estilo con el nombre especificado.

Si este es un nombre en inglés de un estilo incorporado que aún no existe, lo crea automáticamente.

 **Examples:** 

Muestra cuándo recalcular el diseño de página del documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style/) - The corresponding [Style](../../com.aspose.words/style/) value.
### getByStyleIdentifier(int sti) {#getByStyleIdentifier-int}
```
public Style getByStyleIdentifier(int sti)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sti | int |  |

**Returns:**
[Style](../../com.aspose.words/style/)
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de estilos en la colección.

 **Examples:** 

Muestra cómo agregar un Style a la colección de estilos de un documento.

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
int - El número de estilos en la colección.
### getDefaultFont() {#getDefaultFont}
```
public Font getDefaultFont()
```


Obtiene el formato de texto predeterminado del documento.

 **Remarks:** 

Tenga en cuenta que los valores predeterminados a nivel de documento se introdujeron en Microsoft Word 2007 y solo son compatibles totalmente en los formatos OOXML ( [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX)). Los formatos de documento anteriores tienen soporte limitado para esta característica y solo se pueden almacenar los nombres de fuentes.

 **Examples:** 

Muestra cómo agregar un Style a la colección de estilos de un documento.

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


Obtiene el formato de párrafo predeterminado del documento.

 **Remarks:** 

Tenga en cuenta que los valores predeterminados a nivel de documento se introdujeron en Microsoft Word 2007 y solo son compatibles totalmente en los formatos OOXML ( [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX)). Los formatos de documento anteriores no admiten la configuración de formato de párrafo predeterminado del documento.

 **Examples:** 

Muestra cómo agregar un Style a la colección de estilos de un documento.

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


Obtiene el documento propietario.

 **Examples:** 

Muestra cómo acceder a la colección de estilos de un documento.

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


Obtiene un objeto enumerador que enumerará los estilos en orden alfabético de sus nombres.

 **Examples:** 

Muestra cómo acceder a la colección de estilos de un documento.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.util.Iterator
