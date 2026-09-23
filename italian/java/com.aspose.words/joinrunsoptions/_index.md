---
title: "JoinRunsOptions"
linktitle: "JoinRunsOptions"
second_title: "Aspose.Words per Java"
description: "Fornisce flag di configurazione per l'operazione di unione dei run in Java."
type: docs
weight: 406
url: /it/java/com.aspose.words/joinrunsoptions/
---

**Inheritance:**
java.lang.Object
```
public class JoinRunsOptions
```

Fornisce flag di configurazione per l'operazione di join runs.

 **Examples:** 

Mostra come unire i run con la stessa formattazione ignorando gli attributi ridondanti e insignificanti.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create runs with identical visible formatting but some internal differences.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(12.0);
 builder.write("Hello ");
 builder.write("world");

 // Verify runs before join.
 Assert.assertEquals(2, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello ", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());
 Assert.assertEquals("world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(1).getText());

 // Configure options to ignore redundant and insignificant attributes during join.
 JoinRunsOptions options = new JoinRunsOptions();
 options.setIgnoreRedundant(true); // Ignore redundant run properties that don't affect appearance.
 options.setIgnoreInsignificant(true); // Ignore insignificant differences like whitespace-only runs.

 // Join runs that have the same visible formatting using the extended options.
 doc.getFirstSection().getBody().getFirstParagraph().joinRunsWithSameFormatting(options);

 // Verify that runs were successfully joined.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());

 doc.save(getArtifactsDir() + "Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
 
```
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getIgnoreInsignificant()](#getIgnoreInsignificant) | True indica che gli attributi insignificanti di tutti i run saranno ignorati durante l'unione dei run con la stessa formattazione. |
| [getIgnoreRedundant()](#getIgnoreRedundant) | True indica che gli attributi ridondanti di tutti i run saranno ignorati durante l'unione dei run con la stessa formattazione. |
| [getIgnoreSpacing()](#getIgnoreSpacing) | True indica che gli attributi di spaziatura di tutti i run saranno ignorati durante l'unione dei run con la stessa formattazione. |
| [setIgnoreInsignificant(boolean value)](#setIgnoreInsignificant-boolean) | True indica che gli attributi insignificanti di tutti i run saranno ignorati durante l'unione dei run con la stessa formattazione. |
| [setIgnoreRedundant(boolean value)](#setIgnoreRedundant-boolean) | True indica che gli attributi ridondanti di tutti i run saranno ignorati durante l'unione dei run con la stessa formattazione. |
| [setIgnoreSpacing(boolean value)](#setIgnoreSpacing-boolean) | True indica che gli attributi di spaziatura di tutti i run saranno ignorati durante l'unione dei run con la stessa formattazione. |
### getIgnoreInsignificant() {#getIgnoreInsignificant}
```
public boolean getIgnoreInsignificant()
```


True indica che gli attributi insignificanti di tutti i run saranno ignorati durante l'unione dei run con la stessa formattazione.

 **Remarks:** 

Gli attributi insignificanti sono quegli attributi che non hanno un effetto evidente sulla formattazione di un run con il contenuto di testo fornito. Il valore predefinito è False.

**Returns:**
boolean - Il valore booleano corrispondente.
### getIgnoreRedundant() {#getIgnoreRedundant}
```
public boolean getIgnoreRedundant()
```


True indica che gli attributi ridondanti di tutti i run saranno ignorati durante l'unione dei run con la stessa formattazione.

 **Remarks:** 

Gli attributi ridondanti sono quegli attributi che non influenzano il run con il contenuto di testo fornito. Il valore predefinito è False.

**Returns:**
boolean - Il valore booleano corrispondente.
### getIgnoreSpacing() {#getIgnoreSpacing}
```
public boolean getIgnoreSpacing()
```


True indica che gli attributi di spaziatura di tutti i run saranno ignorati durante l'unione dei run con la stessa formattazione.

 **Remarks:** 

Il valore predefinito è False.

**Returns:**
boolean - Il valore booleano corrispondente.
### setIgnoreInsignificant(boolean value) {#setIgnoreInsignificant-boolean}
```
public void setIgnoreInsignificant(boolean value)
```


True indica che gli attributi insignificanti di tutti i run saranno ignorati durante l'unione dei run con la stessa formattazione.

 **Remarks:** 

Gli attributi insignificanti sono quegli attributi che non hanno un effetto evidente sulla formattazione di un run con il contenuto di testo fornito. Il valore predefinito è False.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setIgnoreRedundant(boolean value) {#setIgnoreRedundant-boolean}
```
public void setIgnoreRedundant(boolean value)
```


True indica che gli attributi ridondanti di tutti i run saranno ignorati durante l'unione dei run con la stessa formattazione.

 **Remarks:** 

Gli attributi ridondanti sono quegli attributi che non influenzano il run con il contenuto di testo fornito. Il valore predefinito è False.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setIgnoreSpacing(boolean value) {#setIgnoreSpacing-boolean}
```
public void setIgnoreSpacing(boolean value)
```


True indica che gli attributi di spaziatura di tutti i run saranno ignorati durante l'unione dei run con la stessa formattazione.

 **Remarks:** 

Il valore predefinito è False.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

