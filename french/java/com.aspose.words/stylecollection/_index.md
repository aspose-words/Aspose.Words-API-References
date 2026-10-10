---
title: "StyleCollection"
linktitle: "StyleCollection"
second_title: "Aspose.Words pour Java"
description: "Une collection d'objets Style qui représentent à la fois les styles intégrés et les styles définis par l'utilisateur dans un document en Java."
type: docs
weight: 642
url: /fr/java/com.aspose.words/stylecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class StyleCollection implements Cloneable, Iterable
```

Une collection d'objets [Style](../../com.aspose.words/style/) qui représentent à la fois les styles intégrés et les styles définis par l'utilisateur dans un document.

Pour en savoir plus, consultez l'article de documentation [ Working with Styles and Themes ][Working with Styles and Themes].

 **Examples:** 

Montre comment créer et utiliser un style de paragraphe avec un formatage de liste.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [add(int type, String name)](#add-int-java.lang.String) |  |
| [addCopy(Style style)](#addCopy-com.aspose.words.Style) | Copie un style dans cette collection. |
| [clearQuickStyleGallery()](#clearQuickStyleGallery) | Supprime tous les styles du panneau de la galerie de styles rapides. |
| [get(int index)](#get-int) | Obtient un style par indice. |
| [get(String name)](#get-java.lang.String) | Récupère un style de la collection. |
| [getByStyleIdentifier(int sti)](#getByStyleIdentifier-int) |  |
| [getCount()](#getCount) | Obtient le nombre de styles dans la collection. |
| [getDefaultFont()](#getDefaultFont) | Obtient le formatage de texte par défaut du document. |
| [getDefaultParagraphFormat()](#getDefaultParagraphFormat) | Obtient le formatage de paragraphe par défaut du document. |
| [getDocument()](#getDocument) | Obtient le document propriétaire. |
| [iterator()](#iterator) | Obtient un objet énumérateur qui énumérera les styles par ordre alphabétique de leurs noms. |
### add(int type, String name) {#add-int-java.lang.String}
```
public Style add(int type, String name)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| type | int |  |
| nom | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style/)
### addCopy(Style style) {#addCopy-com.aspose.words.Style}
```
public Style addCopy(Style style)
```


Copie un style dans cette collection.

 **Remarks:** 

Le style à copier peut appartenir au même document ainsi qu'à un document différent.

Le style lié est copié.

Cette méthode ne copie pas les styles de base.

Si la collection contient déjà un style portant le même nom, alors un nouveau nom est généré automatiquement en ajoutant le suffixe \"\\_number\" à partir de 0, par ex. \"Normal\\_0\", \"Heading 1\\_1\", etc. Utilisez le setter [Style.getName()](../../com.aspose.words/style/\\#getName) / [Style.setName(java.lang.String)](../../com.aspose.words/style/\\#setName-java.lang.String) pour modifier le nom du style importé.

 **Examples:** 

Montre comment cloner le style d'un document.

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

Montre comment importer un style d'un document vers un autre document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style/) | Style à copier. |

**Returns:**
[Style](../../com.aspose.words/style/) - Copied style ready for usage.
### clearQuickStyleGallery() {#clearQuickStyleGallery}
```
public void clearQuickStyleGallery()
```


Supprime tous les styles du panneau de la galerie de styles rapides.

 **Examples:** 

Montre comment supprimer les styles du panneau de la galerie de styles.

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


Obtient un style par indice.

 **Examples:** 

Montre comment ajouter un Style à la collection de styles d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[Style](../../com.aspose.words/style/) - A style by index.
### get(String name) {#get-java.lang.String}
```
public Style get(String name)
```


Récupère un style de la collection.  Obtient un style par nom ou alias.

 **Remarks:** 

Sensible à la casse, renvoie  null  si le style avec le nom donné n'est pas trouvé.

Si c'est un nom anglais d'un style intégré qui n'existe pas encore, il le crée automatiquement.

 **Examples:** 

Montre quand recalculer la mise en page du document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style/) - The corresponding [Style](../../com.aspose.words/style/) value.
### getByStyleIdentifier(int sti) {#getByStyleIdentifier-int}
```
public Style getByStyleIdentifier(int sti)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sti | int |  |

**Returns:**
[Style](../../com.aspose.words/style/)
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre de styles dans la collection.

 **Examples:** 

Montre comment ajouter un Style à la collection de styles d'un document.

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
int - Le nombre de styles dans la collection.
### getDefaultFont() {#getDefaultFont}
```
public Font getDefaultFont()
```


Obtient le formatage de texte par défaut du document.

 **Remarks:** 

Notez que les paramètres par défaut au niveau du document ont été introduits dans Microsoft Word 2007 et ne sont entièrement pris en charge que dans les formats OOXML ( [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX)). Les formats de document antérieurs offrent un support limité pour cette fonctionnalité et seuls les noms de polices peuvent être enregistrés.

 **Examples:** 

Montre comment ajouter un Style à la collection de styles d'un document.

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


Obtient le formatage de paragraphe par défaut du document.

 **Remarks:** 

Notez que les paramètres par défaut au niveau du document ont été introduits dans Microsoft Word 2007 et ne sont entièrement pris en charge que dans les formats OOXML ( [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX)). Les formats de document antérieurs ne prennent pas en charge le formatage de paragraphe par défaut du document.

 **Examples:** 

Montre comment ajouter un Style à la collection de styles d'un document.

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


Obtient le document propriétaire.

 **Examples:** 

Montre comment accéder à la collection de styles d'un document.

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


Obtient un objet énumérateur qui énumérera les styles par ordre alphabétique de leurs noms.

 **Examples:** 

Montre comment accéder à la collection de styles d'un document.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.util.Iterator
