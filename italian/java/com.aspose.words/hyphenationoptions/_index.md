---
title: "HyphenationOptions"
linktitle: "HyphenationOptions"
second_title: "Aspose.Words per Java"
description: "Consente di configurare le opzioni di sillabazione del documento in Java."
type: docs
weight: 388
url: /it/java/com.aspose.words/hyphenationoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class HyphenationOptions implements Cloneable
```

Consente di configurare le opzioni di sillabazione del documento.

Per saperne di più, visita l'articolo di documentazione [ Working with Hyphenation ][Working with Hyphenation].

 **Examples:** 

Mostra come configurare la sillabazione automatica.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```


[Working with Hyphenation]: https://docs.aspose.com/words/java/working-with-hyphenation/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getAutoHyphenation()](#getAutoHyphenation) | Ottiene il valore che determina se la sillabazione automatica è attiva per il documento. |
| [getConsecutiveHyphenLimit()](#getConsecutiveHyphenLimit) | Ottiene il numero massimo di righe consecutive che possono terminare con trattini. |
| [getHyphenateCaps()](#getHyphenateCaps) | Ottiene il valore che determina se le parole scritte in maiuscolo sono sillabate. |
| [getHyphenationZone()](#getHyphenationZone) | Ottiene la distanza in 1/20 di punto dal margine destro entro la quale non si desidera sillabare le parole. |
| [setAutoHyphenation(boolean value)](#setAutoHyphenation-boolean) | Imposta il valore che determina se la sillabazione automatica è attivata per il documento. |
| [setConsecutiveHyphenLimit(int value)](#setConsecutiveHyphenLimit-int) | Imposta il numero massimo di righe consecutive che possono terminare con trattini. |
| [setHyphenateCaps(boolean value)](#setHyphenateCaps-boolean) | Imposta il valore che determina se le parole scritte in maiuscolo sono sillabate. |
| [setHyphenationZone(int value)](#setHyphenationZone-int) | Imposta la distanza in 1/20 di punto dal margine destro entro la quale non si desidera sillabare le parole. |
### getAutoHyphenation() {#getAutoHyphenation}
```
public boolean getAutoHyphenation()
```


Ottiene il valore che determina se la sillabazione automatica è attivata per il documento. Il valore predefinito per questa proprietà è false.

 **Examples:** 

Mostra come configurare la sillabazione automatica.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
boolean - Valore che determina se la sillabazione automatica è attivata per il documento.
### getConsecutiveHyphenLimit() {#getConsecutiveHyphenLimit}
```
public int getConsecutiveHyphenLimit()
```


Ottiene il numero massimo di righe consecutive che possono terminare con trattini. Il valore predefinito per questa proprietà è 0.

 **Remarks:** 

Se il valore di questa proprietà è impostato a 0, qualsiasi numero di righe consecutive può terminare con trattini.

La proprietà non ha effetto quando si salva in formati di pagina fissi, ad es. PDF.

 **Examples:** 

Mostra come configurare la sillabazione automatica.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
int - Il numero massimo di righe consecutive che possono terminare con trattini.
### getHyphenateCaps() {#getHyphenateCaps}
```
public boolean getHyphenateCaps()
```


Ottiene il valore che determina se le parole scritte in maiuscolo sono sillabate. Il valore predefinito per questa proprietà è true.

 **Examples:** 

Mostra come configurare la sillabazione automatica.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
boolean - Valore che determina se le parole scritte in maiuscolo sono sillabate.
### getHyphenationZone() {#getHyphenationZone}
```
public int getHyphenationZone()
```


Ottiene la distanza in 1/20 di punto dal margine destro entro la quale non si desidera sillabare le parole. Il valore predefinito per questa proprietà è 360 (0,25 pollice).

 **Examples:** 

Mostra come configurare la sillabazione automatica.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
int - La distanza in 1/20 di punto dal margine destro entro la quale non si desidera sillabare le parole.
### setAutoHyphenation(boolean value) {#setAutoHyphenation-boolean}
```
public void setAutoHyphenation(boolean value)
```


Imposta il valore che determina se la sillabazione automatica è attivata per il documento. Il valore predefinito per questa proprietà è false.

 **Examples:** 

Mostra come configurare la sillabazione automatica.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Valore che determina se la sillabazione automatica è attivata per il documento. |

### setConsecutiveHyphenLimit(int value) {#setConsecutiveHyphenLimit-int}
```
public void setConsecutiveHyphenLimit(int value)
```


Imposta il numero massimo di righe consecutive che possono terminare con trattini. Il valore predefinito per questa proprietà è 0.

 **Remarks:** 

Se il valore di questa proprietà è impostato a 0, qualsiasi numero di righe consecutive può terminare con trattini.

La proprietà non ha effetto quando si salva in formati di pagina fissi, ad es. PDF.

 **Examples:** 

Mostra come configurare la sillabazione automatica.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il numero massimo di righe consecutive che possono terminare con trattini. |

### setHyphenateCaps(boolean value) {#setHyphenateCaps-boolean}
```
public void setHyphenateCaps(boolean value)
```


Imposta il valore che determina se le parole scritte in maiuscolo sono sillabate. Il valore predefinito per questa proprietà è true.

 **Examples:** 

Mostra come configurare la sillabazione automatica.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Valore che determina se le parole scritte in maiuscolo sono sillabate. |

### setHyphenationZone(int value) {#setHyphenationZone-int}
```
public void setHyphenationZone(int value)
```


Imposta la distanza in 1/20 di punto dal margine destro entro la quale non si desidera sillabare le parole. Il valore predefinito per questa proprietà è 360 (0,25 pollice).

 **Examples:** 

Mostra come configurare la sillabazione automatica.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | La distanza in 1/20 di punto dal margine destro entro la quale non si desidera sillabare le parole. |

