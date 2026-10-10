---
title: "SectionLayoutMode"
linktitle: "SectionLayoutMode"
second_title: "Aspose.Words per Java"
description: "Specifica la modalità di layout per una sezione consentendo di definire il comportamento della griglia del documento in Java."
type: docs
weight: 607
url: /it/java/com.aspose.words/sectionlayoutmode/
---

**Inheritance:**
java.lang.Object
```
public class SectionLayoutMode
```

Specifica la modalità di layout per una sezione consentendo di definire il comportamento della griglia del documento.

 **Examples:** 

Mostra come specificare un valore per il numero di caratteri che ogni riga può avere.

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

Mostra come specificare un limite per il numero di righe che ogni pagina può contenere.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [DEFAULT](#DEFAULT) | Specifica che nessuna griglia del documento deve essere applicata al contenuto della sezione corrispondente nel documento. |
| [GRID](#GRID) | Specifica che la sezione corrispondente deve avere sia l'interlinea aggiuntiva che l'interlinea dei caratteri aggiunte a ogni riga e carattere al suo interno, al fine di mantenere un numero specifico di righe per pagina e di caratteri per riga. |
| [LINE_GRID](#LINE-GRID) | Specifica che la sezione corrispondente deve avere un'interlinea aggiuntiva aggiunta a ogni riga al suo interno, al fine di mantenere il numero specificato di righe per pagina. |
| [SNAP_TO_CHARS](#SNAP-TO-CHARS) | Specifica che la sezione corrispondente deve avere sia l'interlinea aggiuntiva che l'interlinea dei caratteri aggiunte a ogni riga e carattere al suo interno, al fine di mantenere un numero specifico di righe per pagina e di caratteri per riga. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String sectionLayoutModeName)](#fromName-java.lang.String) |  |
| [getName(int sectionLayoutMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sectionLayoutMode)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Specifica che nessuna griglia del documento deve essere applicata al contenuto della sezione corrispondente nel documento.

### GRID {#GRID}
```
public static int GRID
```


Specifica che la sezione corrispondente deve avere sia l'interlinea aggiuntiva che l'interlinea dei caratteri aggiunte a ogni riga e carattere al suo interno, al fine di mantenere un numero specifico di righe per pagina e di caratteri per riga. I caratteri non saranno allineati automaticamente con le linee della griglia durante la digitazione.

### LINE_GRID {#LINE-GRID}
```
public static int LINE_GRID
```


Specifica che la sezione corrispondente deve avere un'interlinea aggiuntiva aggiunta a ogni riga al suo interno, al fine di mantenere il numero specificato di righe per pagina.

### SNAP_TO_CHARS {#SNAP-TO-CHARS}
```
public static int SNAP_TO_CHARS
```


Specifica che la sezione corrispondente deve avere sia l'interlinea aggiuntiva che l'interlinea dei caratteri aggiunte a ogni riga e carattere al suo interno, al fine di mantenere un numero specifico di righe per pagina e di caratteri per riga. I caratteri saranno allineati automaticamente con le linee della griglia durante la digitazione.

### length {#length}
```
public static int length
```


### fromName(String sectionLayoutModeName) {#fromName-java.lang.String}
```
public static int fromName(String sectionLayoutModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sectionLayoutModeName | java.lang.String |  |

**Returns:**
int
### getName(int sectionLayoutMode) {#getName-int}
```
public static String getName(int sectionLayoutMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
