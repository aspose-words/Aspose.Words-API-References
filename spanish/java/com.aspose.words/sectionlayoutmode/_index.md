---
title: "SectionLayoutMode"
linktitle: "SectionLayoutMode"
second_title: "Aspose.Words para Java"
description: "Especifica el modo de diseño para una sección que permite definir el comportamiento de la cuadrícula del documento en Java."
type: docs
weight: 607
url: /es/java/com.aspose.words/sectionlayoutmode/
---

**Inheritance:**
java.lang.Object
```
public class SectionLayoutMode
```

Especifica el modo de diseño para una sección que permite definir el comportamiento de la cuadrícula del documento.

 **Examples:** 

Muestra cómo especificar un para el número de caracteres que cada línea puede tener.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

Muestra cómo especificar un límite para la cantidad de líneas que puede tener cada página.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [DEFAULT](#DEFAULT) | Especifica que no se aplicará ninguna cuadrícula de documento al contenido de la sección correspondiente en el documento. |
| [GRID](#GRID) | Especifica que la sección correspondiente debe tener tanto el interlineado adicional como el interletraje añadido a cada línea y carácter dentro de ella para mantener un número específico de líneas por página y de caracteres por línea. |
| [LINE_GRID](#LINE-GRID) | Especifica que la sección correspondiente debe tener un interlineado adicional añadido a cada línea dentro de ella para mantener el número especificado de líneas por página. |
| [SNAP_TO_CHARS](#SNAP-TO-CHARS) | Especifica que la sección correspondiente debe tener tanto el interlineado adicional como el interletraje añadido a cada línea y carácter dentro de ella para mantener un número específico de líneas por página y de caracteres por línea. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String sectionLayoutModeName)](#fromName-java.lang.String) |  |
| [getName(int sectionLayoutMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sectionLayoutMode)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Especifica que no se aplicará ninguna cuadrícula de documento al contenido de la sección correspondiente en el documento.

### GRID {#GRID}
```
public static int GRID
```


Especifica que la sección correspondiente debe tener tanto el interlineado adicional como el interletraje añadido a cada línea y carácter dentro de ella para mantener un número específico de líneas por página y de caracteres por línea. Los caracteres no se alinearán automáticamente con las líneas de la cuadrícula al escribir.

### LINE_GRID {#LINE-GRID}
```
public static int LINE_GRID
```


Especifica que la sección correspondiente debe tener un interlineado adicional añadido a cada línea dentro de ella para mantener el número especificado de líneas por página.

### SNAP_TO_CHARS {#SNAP-TO-CHARS}
```
public static int SNAP_TO_CHARS
```


Especifica que la sección correspondiente debe tener tanto el interlineado adicional como el interletraje añadido a cada línea y carácter dentro de ella para mantener un número específico de líneas por página y de caracteres por línea. Los caracteres se alinearán automáticamente con las líneas de la cuadrícula al escribir.

### length {#length}
```
public static int length
```


### fromName(String sectionLayoutModeName) {#fromName-java.lang.String}
```
public static int fromName(String sectionLayoutModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sectionLayoutModeName | java.lang.String |  |

**Returns:**
int
### getName(int sectionLayoutMode) {#getName-int}
```
public static String getName(int sectionLayoutMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sectionLayoutMode) {#toString-int}
```
public static String toString(int sectionLayoutMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
