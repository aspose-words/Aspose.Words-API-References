---
title: "ViewOptions"
linktitle: "ViewOptions"
second_title: "Aspose.Words para Java"
description: "Proporciona varias opciones que controlan cómo se muestra un documento en Microsoft Word en Java."
type: docs
weight: 714
url: /es/java/com.aspose.words/viewoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ViewOptions implements Cloneable
```

Proporciona varias opciones que controlan cómo se muestra un documento en Microsoft Word.

Para obtener más información, visite el artículo de documentación [ Trabajar con Opciones y Apariencia de Documentos Word ][Trabajar con Opciones y Apariencia de Documentos Word].

 **Examples:** 

Muestra cómo establecer un factor de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

Muestra cómo establecer un tipo de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
 // to automatically zoom the document to fit the width of the page.
 // Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
 // to automatically zoom the document to make the entire first page visible.
 // Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
 // to automatically zoom the document to fit the inner text margins of the first page.
 doc.getViewOptions().setZoomType(zoomType);

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomType.doc");
 
```


[Work with Options and Appearance of Word Documents]: https://docs.aspose.com/words/java/work-with-word-document-options-and-appearance/
## Métodos

| Método | Descripción |
| --- | --- |
| [getDisplayBackgroundShape()](#getDisplayBackgroundShape) | Controla la visualización de la forma de fondo en la vista de diseño de impresión. |
| [getDoNotDisplayPageBoundaries()](#getDoNotDisplayPageBoundaries) | Desactiva la visualización del espacio entre la parte superior del texto y el borde superior de la página. |
| [getFormsDesign()](#getFormsDesign) | Especifica si el documento está en modo de diseño de formularios. |
| [getViewType()](#getViewType) | Controla el modo de vista en Microsoft Word. |
| [getZoomPercent()](#getZoomPercent) | Obtiene el porcentaje al que desea ver su documento. |
| [getZoomType()](#getZoomType) | Obtiene un valor de zoom basado en el tamaño de la ventana. |
| [setDisplayBackgroundShape(boolean value)](#setDisplayBackgroundShape-boolean) | Controla la visualización de la forma de fondo en la vista de diseño de impresión. |
| [setDoNotDisplayPageBoundaries(boolean value)](#setDoNotDisplayPageBoundaries-boolean) | Desactiva la visualización del espacio entre la parte superior del texto y el borde superior de la página. |
| [setFormsDesign(boolean value)](#setFormsDesign-boolean) | Especifica si el documento está en modo de diseño de formularios. |
| [setViewType(int value)](#setViewType-int) | Controla el modo de vista en Microsoft Word. |
| [setZoomPercent(int value)](#setZoomPercent-int) | Establece el porcentaje al que desea ver su documento. |
| [setZoomType(int value)](#setZoomType-int) | Establece un valor de zoom basado en el tamaño de la ventana. |
### getDisplayBackgroundShape() {#getDisplayBackgroundShape}
```
public boolean getDisplayBackgroundShape()
```


Controla la visualización de la forma de fondo en la vista de diseño de impresión.

 **Examples:** 

Muestra cómo ocultar/mostrar imágenes de fondo del documento en las opciones de vista.

```

 // Use an HTML string to create a new document with a flat background color.
 final String HTML =
         "\r\n                \r\n                    Hello world!\r\n                \r\n            ";

 Document doc = new Document(new ByteArrayInputStream(HTML.getBytes()));

 // The source for the document has a flat color background,
 // the presence of which will set the "DisplayBackgroundShape" flag to "true".
 Assert.assertTrue(doc.getViewOptions().getDisplayBackgroundShape());

 // Keep the "DisplayBackgroundShape" as "true" to get the document to display the background color.
 // This may affect some text colors to improve visibility.
 // Set the "DisplayBackgroundShape" to "false" to not display the background color.
 doc.getViewOptions().setDisplayBackgroundShape(displayBackgroundShape);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayBackgroundShape.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getDoNotDisplayPageBoundaries() {#getDoNotDisplayPageBoundaries}
```
public boolean getDoNotDisplayPageBoundaries()
```


Desactiva la visualización del espacio entre la parte superior del texto y el borde superior de la página.

 **Examples:** 

Muestra cómo ocultar el espacio vertical y los encabezados/pies de página en las opciones de vista.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert content that spans across 3 pages.
 builder.writeln("Paragraph 1, Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 2, Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 3, Page 3.");

 // Insert a header and a footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("This is the footer.");

 // This document contains a small amount of content that takes up a few full pages worth of space.
 // Set the "DoNotDisplayPageBoundaries" flag to "true" to get older versions of Microsoft Word to omit headers,
 // footers, and much of the vertical whitespace when displaying our document.
 // Set the "DoNotDisplayPageBoundaries" flag to "false" to get older versions of Microsoft Word
 // to normally display our document.
 doc.getViewOptions().setDoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayPageBoundaries.doc");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getFormsDesign() {#getFormsDesign}
```
public boolean getFormsDesign()
```


Especifica si el documento está en modo de diseño de formularios.

 **Remarks:** 

Actualmente funciona solo para documentos en formato WordML.

 **Examples:** 

Muestra cómo habilitar/deshabilitar el modo de diseño de formularios.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "FormsDesign" property to "false" to keep forms design mode disabled.
 // Set the "FormsDesign" property to "true" to enable forms design mode.
 doc.getViewOptions().setFormsDesign(useFormsDesign);

 doc.save(getArtifactsDir() + "ViewOptions.FormsDesign.xml");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getViewType() {#getViewType}
```
public int getViewType()
```


Controla el modo de vista en Microsoft Word.

 **Remarks:** 

Aunque Aspose.Words puede leer y escribir esta opción, su uso es específico de la aplicación. Por ejemplo, MS Word 2013 no respeta el valor de esta opción.

 **Examples:** 

Muestra cómo establecer un factor de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Returns:**
int - El valor  int  correspondiente. El valor devuelto es una de las constantes [ViewType](../../com.aspose.words/viewtype/).
### getZoomPercent() {#getZoomPercent}
```
public int getZoomPercent()
```


Obtiene el porcentaje al que desea ver su documento.

 **Remarks:** 

Aunque Aspose.Words puede leer y escribir esta opción, su uso es específico de la aplicación. Por ejemplo, MS Word 2013 no respeta el valor de esta opción.

 **Examples:** 

Muestra cómo establecer un factor de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Returns:**
int - El porcentaje al que desea ver su documento.
### getZoomType() {#getZoomType}
```
public int getZoomType()
```


Obtiene un valor de zoom basado en el tamaño de la ventana.

 **Examples:** 

Muestra cómo establecer un factor de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

Muestra cómo establecer un tipo de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
 // to automatically zoom the document to fit the width of the page.
 // Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
 // to automatically zoom the document to make the entire first page visible.
 // Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
 // to automatically zoom the document to fit the inner text margins of the first page.
 doc.getViewOptions().setZoomType(zoomType);

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomType.doc");
 
```

**Returns:**
int - Un valor de zoom basado en el tamaño de la ventana. El valor devuelto es una de las constantes [ZoomType](../../com.aspose.words/zoomtype/).
### setDisplayBackgroundShape(boolean value) {#setDisplayBackgroundShape-boolean}
```
public void setDisplayBackgroundShape(boolean value)
```


Controla la visualización de la forma de fondo en la vista de diseño de impresión.

 **Examples:** 

Muestra cómo ocultar/mostrar imágenes de fondo del documento en las opciones de vista.

```

 // Use an HTML string to create a new document with a flat background color.
 final String HTML =
         "\r\n                \r\n                    Hello world!\r\n                \r\n            ";

 Document doc = new Document(new ByteArrayInputStream(HTML.getBytes()));

 // The source for the document has a flat color background,
 // the presence of which will set the "DisplayBackgroundShape" flag to "true".
 Assert.assertTrue(doc.getViewOptions().getDisplayBackgroundShape());

 // Keep the "DisplayBackgroundShape" as "true" to get the document to display the background color.
 // This may affect some text colors to improve visibility.
 // Set the "DisplayBackgroundShape" to "false" to not display the background color.
 doc.getViewOptions().setDisplayBackgroundShape(displayBackgroundShape);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayBackgroundShape.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setDoNotDisplayPageBoundaries(boolean value) {#setDoNotDisplayPageBoundaries-boolean}
```
public void setDoNotDisplayPageBoundaries(boolean value)
```


Desactiva la visualización del espacio entre la parte superior del texto y el borde superior de la página.

 **Examples:** 

Muestra cómo ocultar el espacio vertical y los encabezados/pies de página en las opciones de vista.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert content that spans across 3 pages.
 builder.writeln("Paragraph 1, Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 2, Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 3, Page 3.");

 // Insert a header and a footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("This is the footer.");

 // This document contains a small amount of content that takes up a few full pages worth of space.
 // Set the "DoNotDisplayPageBoundaries" flag to "true" to get older versions of Microsoft Word to omit headers,
 // footers, and much of the vertical whitespace when displaying our document.
 // Set the "DoNotDisplayPageBoundaries" flag to "false" to get older versions of Microsoft Word
 // to normally display our document.
 doc.getViewOptions().setDoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayPageBoundaries.doc");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setFormsDesign(boolean value) {#setFormsDesign-boolean}
```
public void setFormsDesign(boolean value)
```


Especifica si el documento está en modo de diseño de formularios.

 **Remarks:** 

Actualmente funciona solo para documentos en formato WordML.

 **Examples:** 

Muestra cómo habilitar/deshabilitar el modo de diseño de formularios.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "FormsDesign" property to "false" to keep forms design mode disabled.
 // Set the "FormsDesign" property to "true" to enable forms design mode.
 doc.getViewOptions().setFormsDesign(useFormsDesign);

 doc.save(getArtifactsDir() + "ViewOptions.FormsDesign.xml");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setViewType(int value) {#setViewType-int}
```
public void setViewType(int value)
```


Controla el modo de vista en Microsoft Word.

 **Remarks:** 

Aunque Aspose.Words puede leer y escribir esta opción, su uso es específico de la aplicación. Por ejemplo, MS Word 2013 no respeta el valor de esta opción.

 **Examples:** 

Muestra cómo establecer un factor de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor  int  correspondiente. El valor debe ser una de las constantes [ViewType](../../com.aspose.words/viewtype/). |

### setZoomPercent(int value) {#setZoomPercent-int}
```
public void setZoomPercent(int value)
```


Establece el porcentaje al que desea ver su documento.

 **Remarks:** 

Aunque Aspose.Words puede leer y escribir esta opción, su uso es específico de la aplicación. Por ejemplo, MS Word 2013 no respeta el valor de esta opción.

 **Examples:** 

Muestra cómo establecer un factor de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El porcentaje al que desea ver su documento. |

### setZoomType(int value) {#setZoomType-int}
```
public void setZoomType(int value)
```


Establece un valor de zoom basado en el tamaño de la ventana.

 **Examples:** 

Muestra cómo establecer un factor de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

Muestra cómo establecer un tipo de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
 // to automatically zoom the document to fit the width of the page.
 // Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
 // to automatically zoom the document to make the entire first page visible.
 // Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
 // to automatically zoom the document to fit the inner text margins of the first page.
 doc.getViewOptions().setZoomType(zoomType);

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomType.doc");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Un valor de zoom basado en el tamaño de la ventana. El valor debe ser una de las constantes [ZoomType](../../com.aspose.words/zoomtype/). |

