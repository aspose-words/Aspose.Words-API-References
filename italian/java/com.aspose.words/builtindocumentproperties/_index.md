---
title: "BuiltInDocumentProperties"
linktitle: "BuiltInDocumentProperties"
second_title: "Aspose.Words per Java"
description: "Una raccolta di proprietà di documento integrate in Java."
type: docs
weight: 57
url: /it/java/com.aspose.words/builtindocumentproperties/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.DocumentPropertyCollection](../../com.aspose.words/documentpropertycollection/)
```
public class BuiltInDocumentProperties extends DocumentPropertyCollection
```

Una raccolta di proprietà di documento integrate.

Per saperne di più, visita l'articolo di documentazione [ Work with Document Properties ][Work with Document Properties].

 **Remarks:** 

Fornisce l'accesso agli oggetti [DocumentProperty](../../com.aspose.words/documentproperty/) per nome (utilizzando un indicizzatore) e tramite un insieme di proprietà tipizzate che restituiscono valori dei tipi appropriati.

I nomi delle proprietà non distinguono tra maiuscole e minuscole.

Le proprietà nella raccolta sono ordinate alfabeticamente per nome.


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [clear()](#clear) | Rimuove tutte le proprietà dalla raccolta. |
| [contains(String name)](#contains-java.lang.String) | Restituisce  true  se una proprietà con il nome specificato esiste nella raccolta. |
| [get(int index)](#get-int) | Restituisce un oggetto [DocumentProperty](../../com.aspose.words/documentproperty/) per indice. |
| [get(String name)](#get-java.lang.String) | Restituisce un oggetto [DocumentProperty](../../com.aspose.words/documentproperty/). |
| [getAuthor()](#getAuthor) | Ottiene il nome dell'autore del documento. |
| [getBytes()](#getBytes) | Rappresenta una stima del numero di byte nel documento. |
| [getCategory()](#getCategory) | Ottiene la categoria del documento. |
| [getCharacters()](#getCharacters) | Rappresenta una stima del numero di caratteri nel documento. |
| [getCharactersWithSpaces()](#getCharactersWithSpaces) | Rappresenta una stima del numero di caratteri (spazi inclusi) nel documento. |
| [getComments()](#getComments) | Ottiene i commenti del documento. |
| [getCompany()](#getCompany) | Ottiene la proprietà azienda. |
| [getContentStatus()](#getContentStatus) | Ottiene lo stato del contenuto del documento. |
| [getContentType()](#getContentType) | Ottiene il tipo di contenuto del documento. |
| [getCount()](#getCount) | Ottiene il numero di elementi nella raccolta. |
| [getCreatedTime()](#getCreatedTime) | Ottiene la data di creazione del documento in UTC. |
| [getHeadingPairs()](#getHeadingPairs) | Specifica le intestazioni del documento e i loro nomi. |
| [getHyperlinkBase()](#getHyperlinkBase) | Specifica la stringa base utilizzata per valutare i collegamenti ipertestuali relativi in questo documento. |
| [getHyperlinksChanged()](#getHyperlinksChanged) | Indica se i collegamenti ipertestuali in un documento sono stati modificati. |
| [getKeywords()](#getKeywords) | Ottiene le parole chiave del documento. |
| [getLastPrinted()](#getLastPrinted) | Ottiene la data in cui il documento è stato stampato l'ultima volta in UTC. |
| [getLastSavedBy()](#getLastSavedBy) | Ottiene il nome dell'ultimo autore. |
| [getLastSavedTime()](#getLastSavedTime) | Ottiene l'ora dell'ultimo salvataggio in UTC. |
| [getLines()](#getLines) | Rappresenta una stima del numero di righe nel documento. |
| [getLinksUpToDate()](#getLinksUpToDate) | Indica se i collegamenti ipertestuali in un documento sono aggiornati. |
| [getManager()](#getManager) | Ottiene la proprietà manager. |
| [getNameOfApplication()](#getNameOfApplication) | Ottiene il nome dell'applicazione. |
| [getPages()](#getPages) | Rappresenta una stima del numero di pagine nel documento. |
| [getParagraphs()](#getParagraphs) | Rappresenta una stima del numero di paragrafi nel documento. |
| [getRevisionNumber()](#getRevisionNumber) | Ottiene il numero di revisione del documento. |
| [getScaleCrop()](#getScaleCrop) | Indica se la miniatura del documento è ritagliata o scalata per adattarsi allo schermo. |
| [getSecurity()](#getSecurity) | Specifica il livello di sicurezza di un documento come valore numerico. |
| [getSharedDocument()](#getSharedDocument) | Indica se il documento è condiviso. |
| [getSubject()](#getSubject) | Ottiene l'oggetto del documento. |
| [getTemplate()](#getTemplate) | Ottiene il nome informativo del modello di documento. |
| [getThumbnail()](#getThumbnail) | Ottiene o imposta la miniatura del documento. |
| [getTitle()](#getTitle) | Ottiene il titolo del documento. |
| [getTitlesOfParts()](#getTitlesOfParts) | Ogni stringa nell'array specifica il nome di una parte del documento. |
| [getTotalEditingTime()](#getTotalEditingTime) | Ottiene il tempo totale di modifica in minuti. |
| [getVersion()](#getVersion) | Rappresenta il numero di versione dell'applicazione che ha creato il documento. |
| [getWords()](#getWords) | Rappresenta una stima del numero di parole nel documento. |
| [indexOf(String name)](#indexOf-java.lang.String) | Ottiene l'indice di una proprietà per nome. |
| [iterator()](#iterator) | Restituisce un oggetto iteratore che può essere usato per iterare su tutti gli elementi nella collezione. |
| [remove(String name)](#remove-java.lang.String) | Rimuove una proprietà con il nome specificato dalla raccolta. |
| [removeAt(int index)](#removeAt-int) | Rimuove una proprietà all'indice specificato. |
| [setAuthor(String value)](#setAuthor-java.lang.String) | Imposta il nome dell'autore del documento. |
| [setBytes(int value)](#setBytes-int) | Rappresenta una stima del numero di byte nel documento. |
| [setCategory(String value)](#setCategory-java.lang.String) | Imposta la categoria del documento. |
| [setCharacters(int value)](#setCharacters-int) | Rappresenta una stima del numero di caratteri nel documento. |
| [setCharactersWithSpaces(int value)](#setCharactersWithSpaces-int) | Rappresenta una stima del numero di caratteri (spazi inclusi) nel documento. |
| [setComments(String value)](#setComments-java.lang.String) | Imposta i commenti del documento. |
| [setCompany(String value)](#setCompany-java.lang.String) | Imposta la proprietà azienda. |
| [setContentStatus(String value)](#setContentStatus-java.lang.String) | Imposta lo stato del contenuto del documento. |
| [setContentType(String value)](#setContentType-java.lang.String) | Imposta il tipo di contenuto del documento. |
| [setCreatedTime(Date value)](#setCreatedTime-java.util.Date) | Imposta la data di creazione del documento in UTC. |
| [setHeadingPairs(Object[] value)](#setHeadingPairs-java.lang.Object) | Specifica le intestazioni del documento e i loro nomi. |
| [setHyperlinkBase(String value)](#setHyperlinkBase-java.lang.String) | Specifica la stringa base utilizzata per valutare i collegamenti ipertestuali relativi in questo documento. |
| [setKeywords(String value)](#setKeywords-java.lang.String) | Imposta le parole chiave del documento. |
| [setLastPrinted(Date value)](#setLastPrinted-java.util.Date) | Imposta la data in cui il documento è stato stampato l'ultima volta in UTC. |
| [setLastSavedBy(String value)](#setLastSavedBy-java.lang.String) | Imposta il nome dell'ultimo autore. |
| [setLastSavedTime(Date value)](#setLastSavedTime-java.util.Date) | Imposta l'ora dell'ultimo salvataggio in UTC. |
| [setLines(int value)](#setLines-int) | Rappresenta una stima del numero di righe nel documento. |
| [setLinksUpToDate(boolean value)](#setLinksUpToDate-boolean) | Indica se i collegamenti ipertestuali in un documento sono aggiornati. |
| [setManager(String value)](#setManager-java.lang.String) | Imposta la proprietà manager. |
| [setNameOfApplication(String value)](#setNameOfApplication-java.lang.String) | Imposta il nome dell'applicazione. |
| [setPages(int value)](#setPages-int) | Rappresenta una stima del numero di pagine nel documento. |
| [setParagraphs(int value)](#setParagraphs-int) | Rappresenta una stima del numero di paragrafi nel documento. |
| [setRevisionNumber(int value)](#setRevisionNumber-int) | Imposta il numero di revisione del documento. |
| [setSecurity(int value)](#setSecurity-int) | Specifica il livello di sicurezza di un documento come valore numerico. |
| [setSubject(String value)](#setSubject-java.lang.String) | Imposta l'oggetto del documento. |
| [setTemplate(String value)](#setTemplate-java.lang.String) | Imposta il nome informativo del modello di documento. |
| [setThumbnail(byte[] value)](#setThumbnail-byte) | Ottiene o imposta la miniatura del documento. |
| [setTitle(String value)](#setTitle-java.lang.String) | Imposta il titolo del documento. |
| [setTitlesOfParts(String[] value)](#setTitlesOfParts-java.lang.String) | Ogni stringa nell'array specifica il nome di una parte del documento. |
| [setTotalEditingTime(int value)](#setTotalEditingTime-int) | Imposta il tempo totale di modifica in minuti. |
| [setVersion(int value)](#setVersion-int) | Rappresenta il numero di versione dell'applicazione che ha creato il documento. |
| [setWords(int value)](#setWords-int) | Rappresenta una stima del numero di parole nel documento. |
### clear() {#clear}
```
public void clear()
```


Rimuove tutte le proprietà dalla raccolta.

 **Examples:** 

Mostra come lavorare con le proprietà personalizzate di un documento.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Restituisce  true  se una proprietà con il nome specificato esiste nella raccolta.

 **Examples:** 

Mostra come lavorare con le proprietà personalizzate di un documento.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome della proprietà senza distinzione tra maiuscole e minuscole. |

**Returns:**
boolean -  true  se la proprietà esiste nella raccolta;  false  altrimenti.
### get(int index) {#get-int}
```
public DocumentProperty get(int index)
```


Restituisce un oggetto [DocumentProperty](../../com.aspose.words/documentproperty/) per indice.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

 **Examples:** 

Mostra come lavorare con le proprietà personalizzate del documento.

```

 Document doc = new Document(getMyDir() + "Properties.docx");

 // Every document contains a collection of custom properties, which, like the built-in properties, are key-value pairs.
 // The document has a fixed list of built-in properties. The user creates all of the custom properties.
 Assert.assertEquals("Value of custom document property", doc.getCustomDocumentProperties().get("CustomProperty").toString());

 doc.getCustomDocumentProperties().add("CustomProperty2", "Value of custom document property #2");

 System.out.println("Custom Properties:");
 for (DocumentProperty customDocumentProperty : doc.getCustomDocumentProperties()) {
     System.out.println(customDocumentProperty.getName());
     System.out.println(MessageFormat.format("\tType:\t{0}", customDocumentProperty.getType()));
     System.out.println(MessageFormat.format("\tValue:\t\"{0}\"", customDocumentProperty.getValue()));
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int | Indice basato su zero del [DocumentProperty](../../com.aspose.words/documentproperty/) da recuperare. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - A [DocumentProperty](../../com.aspose.words/documentproperty/) object by index.
### get(String name) {#get-java.lang.String}
```
public DocumentProperty get(String name)
```


Restituisce un oggetto [DocumentProperty](../../com.aspose.words/documentproperty/).  Restituisce un oggetto [DocumentProperty](../../com.aspose.words/documentproperty/) per nome della proprietà.

 **Remarks:** 

I nomi stringa delle proprietà corrispondono ai nomi delle proprietà tipizzate disponibili da [BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties/).

Se richiedi una proprietà che non è presente nel documento, ma il nome della proprietà è riconosciuto come un nome incorporato valido, viene creata una nuova [DocumentProperty](../../com.aspose.words/documentproperty/), aggiunta alla collezione e restituita. Alla proprietà appena creata viene assegnato un valore predefinito (stringa vuota, zero,  false  o DateTime.MinValue a seconda del tipo della proprietà incorporata).

Se richiedi una proprietà che non è presente nel documento e il nome non è riconosciuto come nome incorporato, viene restituito un  null .

 **Examples:** 

Mostra come lavorare con le proprietà personalizzate del documento.

```

 Document doc = new Document(getMyDir() + "Properties.docx");

 // Every document contains a collection of custom properties, which, like the built-in properties, are key-value pairs.
 // The document has a fixed list of built-in properties. The user creates all of the custom properties.
 Assert.assertEquals("Value of custom document property", doc.getCustomDocumentProperties().get("CustomProperty").toString());

 doc.getCustomDocumentProperties().add("CustomProperty2", "Value of custom document property #2");

 System.out.println("Custom Properties:");
 for (DocumentProperty customDocumentProperty : doc.getCustomDocumentProperties()) {
     System.out.println(customDocumentProperty.getName());
     System.out.println(MessageFormat.format("\tType:\t{0}", customDocumentProperty.getType()));
     System.out.println(MessageFormat.format("\tValue:\t\"{0}\"", customDocumentProperty.getValue()));
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome della proprietà senza distinzione tra maiuscole e minuscole da recuperare. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The corresponding [DocumentProperty](../../com.aspose.words/documentproperty/) value.
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Ottiene il nome dell'autore del documento.

 **Examples:** 

Mostra come lavorare con le proprietà di documento incorporate nella categoria "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Returns:**
java.lang.String - Il nome dell'autore del documento.
### getBytes() {#getBytes}
```
public int getBytes()
```


Rappresenta una stima del numero di byte nel documento.

 **Remarks:** 

Microsoft Word non imposta sempre questa proprietà.

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
int - Il valore  int  corrispondente.
### getCategory() {#getCategory}
```
public String getCategory()
```


Ottiene la categoria del documento.

 **Examples:** 

Mostra come lavorare con le proprietà di documento incorporate nella categoria "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Returns:**
java.lang.String - La categoria del documento.
### getCharacters() {#getCharacters}
```
public int getCharacters()
```


Rappresenta una stima del numero di caratteri nel documento.

 **Remarks:** 

Aspose.Words aggiorna questa proprietà quando chiami [Document.updateWordCount()](../../com.aspose.words/document/\\#updateWordCount).

 **Examples:** 

Mostra come aggiornare tutte le etichette delle liste in un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
int - Il valore  int  corrispondente.
### getCharactersWithSpaces() {#getCharactersWithSpaces}
```
public int getCharactersWithSpaces()
```


Rappresenta una stima del numero di caratteri (spazi inclusi) nel documento.

 **Remarks:** 

Aspose.Words aggiorna questa proprietà quando chiami [Document.updateWordCount()](../../com.aspose.words/document/\\#updateWordCount).

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
int - Il valore  int  corrispondente.
### getComments() {#getComments}
```
public String getComments()
```


Ottiene i commenti del documento.

 **Examples:** 

Mostra come lavorare con le proprietà di documento incorporate nella categoria "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Returns:**
java.lang.String - I commenti del documento.
### getCompany() {#getCompany}
```
public String getCompany()
```


Ottiene la proprietà azienda.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
java.lang.String - La proprietà azienda.
### getContentStatus() {#getContentStatus}
```
public String getContentStatus()
```


Ottiene lo stato del contenuto del documento.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
java.lang.String - Lo stato del contenuto del documento.
### getContentType() {#getContentType}
```
public String getContentType()
```


Ottiene il tipo di contenuto del documento.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
java.lang.String - Il tipo di contenuto del documento.
### getCount() {#getCount}
```
public int getCount()
```


Ottiene il numero di elementi nella raccolta.

 **Examples:** 

Mostra come lavorare con le proprietà personalizzate del documento.

```

 Document doc = new Document(getMyDir() + "Properties.docx");

 // Every document contains a collection of custom properties, which, like the built-in properties, are key-value pairs.
 // The document has a fixed list of built-in properties. The user creates all of the custom properties.
 Assert.assertEquals("Value of custom document property", doc.getCustomDocumentProperties().get("CustomProperty").toString());

 doc.getCustomDocumentProperties().add("CustomProperty2", "Value of custom document property #2");

 System.out.println("Custom Properties:");
 for (DocumentProperty customDocumentProperty : doc.getCustomDocumentProperties()) {
     System.out.println(customDocumentProperty.getName());
     System.out.println(MessageFormat.format("\tType:\t{0}", customDocumentProperty.getType()));
     System.out.println(MessageFormat.format("\tValue:\t\"{0}\"", customDocumentProperty.getValue()));
 }
 
```

**Returns:**
int - Numero di elementi nella raccolta.
### getCreatedTime() {#getCreatedTime}
```
public Date getCreatedTime()
```


Ottiene la data di creazione del documento in UTC.

 **Remarks:** 

Per i documenti originati dal formato RTF questa proprietà restituisce l'ora locale della macchina dell'autore al momento della creazione del documento.

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
java.util.Date - Data di creazione del documento in UTC.
### getHeadingPairs() {#getHeadingPairs}
```
public Object[] getHeadingPairs()
```


Specifica le intestazioni del documento e i loro nomi.

 **Remarks:** 

Ogni coppia di intestazioni occupa due elementi in questo array.

Il primo elemento della coppia è un java.lang.String e specifica il nome dell'intestazione. Il secondo elemento della coppia è un int e specifica il conteggio delle parti del documento per questa intestazione nella proprietà [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\\#setTitlesOfParts-java.lang.String).

La somma totale dei conteggi per tutte le coppie di intestazioni in questa proprietà deve essere uguale al numero di elementi nella proprietà [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\\#setTitlesOfParts-java.lang.String).

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra la relazione tra le proprietà "HeadingPairs" e "TitlesOfParts".

```

 Document doc = new Document(getMyDir() + "Heading pairs and titles of parts.docx");

 // We can find the combined values of these collections via
 // "File" -> "Properties" -> "Advanced Properties" -> "Contents" tab.
 // The HeadingPairs property is a collection of  pairs that
 // determines how many document parts a heading spans across.
 Object[] headingPairs = doc.getBuiltInDocumentProperties().getHeadingPairs();

 // The TitlesOfParts property contains the names of parts that belong to the above headings.
 String[] titlesOfParts = doc.getBuiltInDocumentProperties().getTitlesOfParts();

 int headingPairsIndex = 0;
 int titlesOfPartsIndex = 0;
 while (headingPairsIndex < headingPairs.length) {
     System.out.println(MessageFormat.format("Parts for {0}:", headingPairs[headingPairsIndex++]));
     int partsCount = (int) headingPairs[headingPairsIndex++];

     for (int i = 0; i < partsCount; i++)
         System.out.println(MessageFormat.format("\t\"{0}\"", titlesOfParts[titlesOfPartsIndex++]));
 }
 
```

**Returns:**
java.lang.Object[] - Il valore java.lang.Object[] corrispondente.
### getHyperlinkBase() {#getHyperlinkBase}
```
public String getHyperlinkBase()
```


Specifica la stringa base utilizzata per valutare i collegamenti ipertestuali relativi in questo documento.

 **Remarks:** 

Aspose.Words non utilizza questa proprietà.

 **Examples:** 

Mostra come memorizzare la parte base di un collegamento ipertestuale nelle proprietà del documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a relative hyperlink to a document in the local file system named "Document.docx".
 // Clicking on the link in Microsoft Word will open the designated document, if it is available.
 builder.insertHyperlink("Relative hyperlink", "Document.docx", false);

 // This link is relative. If there is no "Document.docx" in the same folder
 // as the document that contains this link, the link will be broken.
 Assert.assertFalse(new File(getArtifactsDir() + "Document.docx").exists());
 doc.save(getArtifactsDir() + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

 // The document we are trying to link to is in a different directory to the one we are planning to save the document in.
 // We could fix links like this by putting an absolute filename in each one.
 // Alternatively, we could provide a base link that every hyperlink with a relative filename
 // will prepend to its link when we click on it.
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();
 properties.setHyperlinkBase(getMyDir());

 Assert.assertTrue(new File(properties.getHyperlinkBase() + ((FieldHyperlink) doc.getRange().getFields().get(0)).getAddress()).exists());

 doc.save(getArtifactsDir() + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
 
```

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getHyperlinksChanged() {#getHyperlinksChanged}
```
public boolean getHyperlinksChanged()
```


Indica se i collegamenti ipertestuali in un documento sono stati modificati.

 **Remarks:** 

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come ottenere le proprietà estese.

```

 Document doc = new Document(getMyDir() + "Extended properties.docx");
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getScaleCrop());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getSharedDocument());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getHyperlinksChanged());
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getKeywords() {#getKeywords}
```
public String getKeywords()
```


Ottiene le parole chiave del documento.

 **Examples:** 

Mostra come lavorare con le proprietà di documento incorporate nella categoria "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Returns:**
java.lang.String - Le parole chiave del documento.
### getLastPrinted() {#getLastPrinted}
```
public Date getLastPrinted()
```


Ottiene la data in cui il documento è stato stampato l'ultima volta in UTC.

 **Remarks:** 

Per i documenti originati dal formato RTF questa proprietà restituisce l'ora locale dell'ultima operazione di stampa.

Se il documento non è mai stato stampato, questa proprietà restituirà DateTime.MinValue.

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
java.util.Date - La data in cui il documento è stato stampato l'ultima volta in UTC.
### getLastSavedBy() {#getLastSavedBy}
```
public String getLastSavedBy()
```


Ottiene il nome dell'ultimo autore.

 **Remarks:** 

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
java.lang.String - Il nome dell'ultimo autore.
### getLastSavedTime() {#getLastSavedTime}
```
public Date getLastSavedTime()
```


Ottiene l'ora dell'ultimo salvataggio in UTC.

 **Remarks:** 

Per i documenti originati dal formato RTF questa proprietà restituisce l'ora locale dell'ultima operazione di salvataggio.

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

Mostra come utilizzare il campo SAVEDATE per visualizzare la data/ora dell'operazione di salvataggio più recente del documento eseguita con Microsoft Word.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln(" Date this document was last saved:");

 // We can use the SAVEDATE field to display the last save operation's date and time on the document.
 // The save operation that these fields refer to is the manual save in an application like Microsoft Word,
 // not the document's Save method.
 // Below are three different calendar types according to which the SAVEDATE field can display the date/time.
 // 1 -  Islamic Lunar Calendar:
 builder.write("According to the Lunar Calendar - ");
 FieldSaveDate field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseLunarCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\h", field.getFieldCode());

 // 2 -  Umm al-Qura calendar:
 builder.write("\nAccording to the Umm al-Qura calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseUmAlQuraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\u", field.getFieldCode());

 // 3 -  Indian National calendar:
 builder.write("\nAccording to the Indian National calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseSakaEraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\s", field.getFieldCode());

 // The SAVEDATE fields draw their date/time values from the LastSavedTime built-in property.
 // The document's Save method will not update this value, but we can still update it manually.
 doc.getBuiltInDocumentProperties().setLastSavedTime(new Date());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SAVEDATE.docx");
 
```

**Returns:**
java.util.Date - L'ora dell'ultimo salvataggio in UTC.
### getLines() {#getLines}
```
public int getLines()
```


Rappresenta una stima del numero di righe nel documento.

 **Remarks:** 

Aspose.Words aggiorna questa proprietà quando si chiama [Document.updateWordCount(boolean)](../../com.aspose.words/document/\#updateWordCount-boolean).

 **Examples:** 

Mostra come aggiornare tutte le etichette delle liste in un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
int - Il valore  int  corrispondente.
### getLinksUpToDate() {#getLinksUpToDate}
```
public boolean getLinksUpToDate()
```


Indica se i collegamenti ipertestuali in un documento sono aggiornati.

 **Remarks:** 

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getManager() {#getManager}
```
public String getManager()
```


Ottiene la proprietà manager.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
java.lang.String - La proprietà manager.
### getNameOfApplication() {#getNameOfApplication}
```
public String getNameOfApplication()
```


Ottiene il nome dell'applicazione.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
java.lang.String - Il nome dell'applicazione.
### getPages() {#getPages}
```
public int getPages()
```


Rappresenta una stima del numero di pagine nel documento.

 **Remarks:** 

Aspose.Words aggiorna questa proprietà quando si chiama [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
int - Il valore  int  corrispondente.
### getParagraphs() {#getParagraphs}
```
public int getParagraphs()
```


Rappresenta una stima del numero di paragrafi nel documento.

 **Remarks:** 

Aspose.Words aggiorna questa proprietà quando chiami [Document.updateWordCount()](../../com.aspose.words/document/\\#updateWordCount).

 **Examples:** 

Mostra come aggiornare tutte le etichette delle liste in un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
int - Il valore  int  corrispondente.
### getRevisionNumber() {#getRevisionNumber}
```
public int getRevisionNumber()
```


Ottiene il numero di revisione del documento.

 **Remarks:** 

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

Mostra come lavorare con i campi REVNUM.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Current revision #");

 // Insert a REVNUM field, which displays the document's current revision number property.
 FieldRevNum field = (FieldRevNum) builder.insertField(FieldType.FIELD_REVISION_NUM, true);

 Assert.assertEquals(" REVNUM ", field.getFieldCode());
 Assert.assertEquals("1", field.getResult());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getRevisionNumber());

 // This property counts how many times a document has been saved in Microsoft Word,
 // and is unrelated to tracked revisions. We can find it by right clicking the document in Windows Explorer
 // via Properties -> Details. We can update this property manually.
 doc.getBuiltInDocumentProperties().setRevisionNumber(doc.getBuiltInDocumentProperties().getRevisionNumber() + 1);
 field.update();

 Assert.assertEquals("2", field.getResult());
 
```

**Returns:**
int - Il numero di revisione del documento.
### getScaleCrop() {#getScaleCrop}
```
public boolean getScaleCrop()
```


Indica se la miniatura del documento è ritagliata o scalata per adattarsi allo schermo.

 **Remarks:** 

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come ottenere le proprietà estese.

```

 Document doc = new Document(getMyDir() + "Extended properties.docx");
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getScaleCrop());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getSharedDocument());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getHyperlinksChanged());
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getSecurity() {#getSecurity}
```
public int getSecurity()
```


Specifica il livello di sicurezza di un documento come valore numerico.

 **Remarks:** 

Utilizzare questa proprietà solo a scopo informativo perché Microsoft Word non imposta sempre questa proprietà. Questa proprietà è disponibile solo nei documenti DOC e OOXML.

Per proteggere o rimuovere la protezione di un documento utilizzare i metodi **M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** e [Document.unprotect()](../../com.aspose.words/document/\#unprotect).

Aspose.Words aggiorna questa proprietà a un valore corretto prima di salvare un documento.

 **Examples:** 

Mostra come utilizzare le proprietà del documento per visualizzare il livello di sicurezza di un documento.

```

 Document doc = new Document();

 Assert.assertEquals(DocumentSecurity.NONE, doc.getBuiltInDocumentProperties().getSecurity());

 // If we configure a document to be read-only, it will display this status using the "Security" built-in property.
 doc.getWriteProtection().setReadOnlyRecommended(true);
 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyRecommended.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_RECOMMENDED,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyRecommended.docx").getBuiltInDocumentProperties().getSecurity());

 // Write-protect a document, and then verify its security level.
 doc = new Document();

 Assert.assertFalse(doc.getWriteProtection().isWriteProtected());

 doc.getWriteProtection().setPassword("MyPassword");

 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));
 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyEnforced.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_ENFORCED,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyEnforced.docx").getBuiltInDocumentProperties().getSecurity());

 // "Security" is a descriptive property. We can edit its value manually.
 doc = new Document();

 doc.protect(ProtectionType.ALLOW_ONLY_COMMENTS, "MyPassword");
 doc.getBuiltInDocumentProperties().setSecurity(DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS);
 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").getBuiltInDocumentProperties().getSecurity());
 
```

**Returns:**
int - Il valore int corrispondente. Il valore restituito è una combinazione bitwise delle costanti [DocumentSecurity](../../com.aspose.words/documentsecurity/).
### getSharedDocument() {#getSharedDocument}
```
public boolean getSharedDocument()
```


Indica se il documento è condiviso.

 **Remarks:** 

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come ottenere le proprietà estese.

```

 Document doc = new Document(getMyDir() + "Extended properties.docx");
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getScaleCrop());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getSharedDocument());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getHyperlinksChanged());
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getSubject() {#getSubject}
```
public String getSubject()
```


Ottiene l'oggetto del documento.

 **Examples:** 

Mostra come lavorare con le proprietà di documento incorporate nella categoria "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Returns:**
java.lang.String - L'oggetto del documento.
### getTemplate() {#getTemplate}
```
public String getTemplate()
```


Ottiene il nome informativo del modello di documento.

 **Remarks:** 

In Microsoft Word, questa proprietà è solo a scopo informativo e di solito contiene solo il nome file del modello senza il percorso.

Una stringa vuota indica che il documento è collegato al modello Normal.

Per ottenere o impostare il nome effettivo del modello allegato, utilizzare la proprietà [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String).

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
java.lang.String - Il nome informativo del modello del documento.
### getThumbnail() {#getThumbnail}
```
public byte[] getThumbnail()
```


Ottiene o imposta la miniatura del documento.

**Returns:**
byte[] - Il valore byte[] corrispondente.
### getTitle() {#getTitle}
```
public String getTitle()
```


Ottiene il titolo del documento.

 **Examples:** 

Mostra come lavorare con le proprietà di documento incorporate nella categoria "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Returns:**
java.lang.String - Il titolo del documento.
### getTitlesOfParts() {#getTitlesOfParts}
```
public String[] getTitlesOfParts()
```


Ogni stringa nell'array specifica il nome di una parte del documento.

 **Remarks:** 

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra la relazione tra le proprietà "HeadingPairs" e "TitlesOfParts".

```

 Document doc = new Document(getMyDir() + "Heading pairs and titles of parts.docx");

 // We can find the combined values of these collections via
 // "File" -> "Properties" -> "Advanced Properties" -> "Contents" tab.
 // The HeadingPairs property is a collection of  pairs that
 // determines how many document parts a heading spans across.
 Object[] headingPairs = doc.getBuiltInDocumentProperties().getHeadingPairs();

 // The TitlesOfParts property contains the names of parts that belong to the above headings.
 String[] titlesOfParts = doc.getBuiltInDocumentProperties().getTitlesOfParts();

 int headingPairsIndex = 0;
 int titlesOfPartsIndex = 0;
 while (headingPairsIndex < headingPairs.length) {
     System.out.println(MessageFormat.format("Parts for {0}:", headingPairs[headingPairsIndex++]));
     int partsCount = (int) headingPairs[headingPairsIndex++];

     for (int i = 0; i < partsCount; i++)
         System.out.println(MessageFormat.format("\t\"{0}\"", titlesOfParts[titlesOfPartsIndex++]));
 }
 
```

**Returns:**
java.lang.String[] - Il valore java.lang.String[] corrispondente.
### getTotalEditingTime() {#getTotalEditingTime}
```
public int getTotalEditingTime()
```


Ottiene il tempo totale di modifica in minuti.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
int - Il tempo totale di modifica in minuti.
### getVersion() {#getVersion}
```
public int getVersion()
```


Rappresenta il numero di versione dell'applicazione che ha creato il documento.

 **Remarks:** 

Quando un documento è stato creato da Microsoft Word, i 16 bit più alti rappresentano la versione principale e i 16 bit più bassi rappresentano il numero di build.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
int - Il valore  int  corrispondente.
### getWords() {#getWords}
```
public int getWords()
```


Rappresenta una stima del numero di parole nel documento.

 **Remarks:** 

Aspose.Words aggiorna questa proprietà quando chiami [Document.updateWordCount()](../../com.aspose.words/document/\\#updateWordCount).

 **Examples:** 

Mostra come aggiornare tutte le etichette delle liste in un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
int - Il valore  int  corrispondente.
### indexOf(String name) {#indexOf-java.lang.String}
```
public int indexOf(String name)
```


Ottiene l'indice di una proprietà per nome.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

 **Examples:** 

Mostra come lavorare con le proprietà personalizzate di un documento.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome della proprietà senza distinzione tra maiuscole e minuscole. |

**Returns:**
int - L'indice basato su zero. Valore negativo se non trovato.
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un oggetto iteratore che può essere usato per iterare su tutti gli elementi nella collezione.

 **Examples:** 

Mostra come lavorare con le proprietà personalizzate di un documento.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Returns:**
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Rimuove una proprietà con il nome specificato dalla raccolta.

 **Examples:** 

Mostra come lavorare con le proprietà personalizzate di un documento.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome della proprietà senza distinzione tra maiuscole e minuscole. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Rimuove una proprietà all'indice specificato.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

 **Examples:** 

Mostra come lavorare con le proprietà personalizzate di un documento.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice basato su zero. |

### setAuthor(String value) {#setAuthor-java.lang.String}
```
public void setAuthor(String value)
```


Imposta il nome dell'autore del documento.

 **Examples:** 

Mostra come lavorare con le proprietà di documento incorporate nella categoria "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il nome dell'autore del documento. |

### setBytes(int value) {#setBytes-int}
```
public void setBytes(int value)
```


Rappresenta una stima del numero di byte nel documento.

 **Remarks:** 

Microsoft Word non imposta sempre questa proprietà.

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il valore  int  corrispondente. |

### setCategory(String value) {#setCategory-java.lang.String}
```
public void setCategory(String value)
```


Imposta la categoria del documento.

 **Examples:** 

Mostra come lavorare con le proprietà di documento incorporate nella categoria "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | La categoria del documento. |

### setCharacters(int value) {#setCharacters-int}
```
public void setCharacters(int value)
```


Rappresenta una stima del numero di caratteri nel documento.

 **Remarks:** 

Aspose.Words aggiorna questa proprietà quando chiami [Document.updateWordCount()](../../com.aspose.words/document/\\#updateWordCount).

 **Examples:** 

Mostra come aggiornare tutte le etichette delle liste in un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il valore  int  corrispondente. |

### setCharactersWithSpaces(int value) {#setCharactersWithSpaces-int}
```
public void setCharactersWithSpaces(int value)
```


Rappresenta una stima del numero di caratteri (spazi inclusi) nel documento.

 **Remarks:** 

Aspose.Words aggiorna questa proprietà quando chiami [Document.updateWordCount()](../../com.aspose.words/document/\\#updateWordCount).

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il valore  int  corrispondente. |

### setComments(String value) {#setComments-java.lang.String}
```
public void setComments(String value)
```


Imposta i commenti del documento.

 **Examples:** 

Mostra come lavorare con le proprietà di documento incorporate nella categoria "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | I commenti del documento. |

### setCompany(String value) {#setCompany-java.lang.String}
```
public void setCompany(String value)
```


Imposta la proprietà azienda.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | La proprietà company. |

### setContentStatus(String value) {#setContentStatus-java.lang.String}
```
public void setContentStatus(String value)
```


Imposta lo stato del contenuto del documento.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Lo stato del contenuto del documento. |

### setContentType(String value) {#setContentType-java.lang.String}
```
public void setContentType(String value)
```


Imposta il tipo di contenuto del documento.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il tipo di contenuto del documento. |

### setCreatedTime(Date value) {#setCreatedTime-java.util.Date}
```
public void setCreatedTime(Date value)
```


Imposta la data di creazione del documento in UTC.

 **Remarks:** 

Per i documenti originati dal formato RTF questa proprietà restituisce l'ora locale della macchina dell'autore al momento della creazione del documento.

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.util.Date | Data di creazione del documento in UTC. |

### setHeadingPairs(Object[] value) {#setHeadingPairs-java.lang.Object}
```
public void setHeadingPairs(Object[] value)
```


Specifica le intestazioni del documento e i loro nomi.

 **Remarks:** 

Ogni coppia di intestazioni occupa due elementi in questo array.

Il primo elemento della coppia è un java.lang.String e specifica il nome dell'intestazione. Il secondo elemento della coppia è un int e specifica il conteggio delle parti del documento per questa intestazione nella proprietà [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\\#setTitlesOfParts-java.lang.String).

La somma totale dei conteggi per tutte le coppie di intestazioni in questa proprietà deve essere uguale al numero di elementi nella proprietà [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\\#setTitlesOfParts-java.lang.String).

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra la relazione tra le proprietà "HeadingPairs" e "TitlesOfParts".

```

 Document doc = new Document(getMyDir() + "Heading pairs and titles of parts.docx");

 // We can find the combined values of these collections via
 // "File" -> "Properties" -> "Advanced Properties" -> "Contents" tab.
 // The HeadingPairs property is a collection of  pairs that
 // determines how many document parts a heading spans across.
 Object[] headingPairs = doc.getBuiltInDocumentProperties().getHeadingPairs();

 // The TitlesOfParts property contains the names of parts that belong to the above headings.
 String[] titlesOfParts = doc.getBuiltInDocumentProperties().getTitlesOfParts();

 int headingPairsIndex = 0;
 int titlesOfPartsIndex = 0;
 while (headingPairsIndex < headingPairs.length) {
     System.out.println(MessageFormat.format("Parts for {0}:", headingPairs[headingPairsIndex++]));
     int partsCount = (int) headingPairs[headingPairsIndex++];

     for (int i = 0; i < partsCount; i++)
         System.out.println(MessageFormat.format("\t\"{0}\"", titlesOfParts[titlesOfPartsIndex++]));
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.Object[] | Il valore java.lang.Object[] corrispondente. |

### setHyperlinkBase(String value) {#setHyperlinkBase-java.lang.String}
```
public void setHyperlinkBase(String value)
```


Specifica la stringa base utilizzata per valutare i collegamenti ipertestuali relativi in questo documento.

 **Remarks:** 

Aspose.Words non utilizza questa proprietà.

 **Examples:** 

Mostra come memorizzare la parte base di un collegamento ipertestuale nelle proprietà del documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a relative hyperlink to a document in the local file system named "Document.docx".
 // Clicking on the link in Microsoft Word will open the designated document, if it is available.
 builder.insertHyperlink("Relative hyperlink", "Document.docx", false);

 // This link is relative. If there is no "Document.docx" in the same folder
 // as the document that contains this link, the link will be broken.
 Assert.assertFalse(new File(getArtifactsDir() + "Document.docx").exists());
 doc.save(getArtifactsDir() + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

 // The document we are trying to link to is in a different directory to the one we are planning to save the document in.
 // We could fix links like this by putting an absolute filename in each one.
 // Alternatively, we could provide a base link that every hyperlink with a relative filename
 // will prepend to its link when we click on it.
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();
 properties.setHyperlinkBase(getMyDir());

 Assert.assertTrue(new File(properties.getHyperlinkBase() + ((FieldHyperlink) doc.getRange().getFields().get(0)).getAddress()).exists());

 doc.save(getArtifactsDir() + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setKeywords(String value) {#setKeywords-java.lang.String}
```
public void setKeywords(String value)
```


Imposta le parole chiave del documento.

 **Examples:** 

Mostra come lavorare con le proprietà di documento incorporate nella categoria "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Le parole chiave del documento. |

### setLastPrinted(Date value) {#setLastPrinted-java.util.Date}
```
public void setLastPrinted(Date value)
```


Imposta la data in cui il documento è stato stampato l'ultima volta in UTC.

 **Remarks:** 

Per i documenti originati dal formato RTF questa proprietà restituisce l'ora locale dell'ultima operazione di stampa.

Se il documento non è mai stato stampato, questa proprietà restituirà DateTime.MinValue.

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.util.Date | La data in cui il documento è stato stampato per l'ultima volta in UTC. |

### setLastSavedBy(String value) {#setLastSavedBy-java.lang.String}
```
public void setLastSavedBy(String value)
```


Imposta il nome dell'ultimo autore.

 **Remarks:** 

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il nome dell'ultimo autore. |

### setLastSavedTime(Date value) {#setLastSavedTime-java.util.Date}
```
public void setLastSavedTime(Date value)
```


Imposta l'ora dell'ultimo salvataggio in UTC.

 **Remarks:** 

Per i documenti originati dal formato RTF questa proprietà restituisce l'ora locale dell'ultima operazione di salvataggio.

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

Mostra come utilizzare il campo SAVEDATE per visualizzare la data/ora dell'operazione di salvataggio più recente del documento eseguita con Microsoft Word.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln(" Date this document was last saved:");

 // We can use the SAVEDATE field to display the last save operation's date and time on the document.
 // The save operation that these fields refer to is the manual save in an application like Microsoft Word,
 // not the document's Save method.
 // Below are three different calendar types according to which the SAVEDATE field can display the date/time.
 // 1 -  Islamic Lunar Calendar:
 builder.write("According to the Lunar Calendar - ");
 FieldSaveDate field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseLunarCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\h", field.getFieldCode());

 // 2 -  Umm al-Qura calendar:
 builder.write("\nAccording to the Umm al-Qura calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseUmAlQuraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\u", field.getFieldCode());

 // 3 -  Indian National calendar:
 builder.write("\nAccording to the Indian National calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseSakaEraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\s", field.getFieldCode());

 // The SAVEDATE fields draw their date/time values from the LastSavedTime built-in property.
 // The document's Save method will not update this value, but we can still update it manually.
 doc.getBuiltInDocumentProperties().setLastSavedTime(new Date());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SAVEDATE.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.util.Date | L'ora dell'ultimo salvataggio in UTC. |

### setLines(int value) {#setLines-int}
```
public void setLines(int value)
```


Rappresenta una stima del numero di righe nel documento.

 **Remarks:** 

Aspose.Words aggiorna questa proprietà quando si chiama [Document.updateWordCount(boolean)](../../com.aspose.words/document/\#updateWordCount-boolean).

 **Examples:** 

Mostra come aggiornare tutte le etichette delle liste in un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il valore  int  corrispondente. |

### setLinksUpToDate(boolean value) {#setLinksUpToDate-boolean}
```
public void setLinksUpToDate(boolean value)
```


Indica se i collegamenti ipertestuali in un documento sono aggiornati.

 **Remarks:** 

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setManager(String value) {#setManager-java.lang.String}
```
public void setManager(String value)
```


Imposta la proprietà manager.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | La proprietà manager. |

### setNameOfApplication(String value) {#setNameOfApplication-java.lang.String}
```
public void setNameOfApplication(String value)
```


Imposta il nome dell'applicazione.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il nome dell'applicazione. |

### setPages(int value) {#setPages-int}
```
public void setPages(int value)
```


Rappresenta una stima del numero di pagine nel documento.

 **Remarks:** 

Aspose.Words aggiorna questa proprietà quando si chiama [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il valore  int  corrispondente. |

### setParagraphs(int value) {#setParagraphs-int}
```
public void setParagraphs(int value)
```


Rappresenta una stima del numero di paragrafi nel documento.

 **Remarks:** 

Aspose.Words aggiorna questa proprietà quando chiami [Document.updateWordCount()](../../com.aspose.words/document/\\#updateWordCount).

 **Examples:** 

Mostra come aggiornare tutte le etichette delle liste in un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il valore  int  corrispondente. |

### setRevisionNumber(int value) {#setRevisionNumber-int}
```
public void setRevisionNumber(int value)
```


Imposta il numero di revisione del documento.

 **Remarks:** 

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

Mostra come lavorare con i campi REVNUM.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Current revision #");

 // Insert a REVNUM field, which displays the document's current revision number property.
 FieldRevNum field = (FieldRevNum) builder.insertField(FieldType.FIELD_REVISION_NUM, true);

 Assert.assertEquals(" REVNUM ", field.getFieldCode());
 Assert.assertEquals("1", field.getResult());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getRevisionNumber());

 // This property counts how many times a document has been saved in Microsoft Word,
 // and is unrelated to tracked revisions. We can find it by right clicking the document in Windows Explorer
 // via Properties -> Details. We can update this property manually.
 doc.getBuiltInDocumentProperties().setRevisionNumber(doc.getBuiltInDocumentProperties().getRevisionNumber() + 1);
 field.update();

 Assert.assertEquals("2", field.getResult());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il numero di revisione del documento. |

### setSecurity(int value) {#setSecurity-int}
```
public void setSecurity(int value)
```


Specifica il livello di sicurezza di un documento come valore numerico.

 **Remarks:** 

Utilizzare questa proprietà solo a scopo informativo perché Microsoft Word non imposta sempre questa proprietà. Questa proprietà è disponibile solo nei documenti DOC e OOXML.

Per proteggere o rimuovere la protezione di un documento utilizzare i metodi **M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** e [Document.unprotect()](../../com.aspose.words/document/\#unprotect).

Aspose.Words aggiorna questa proprietà a un valore corretto prima di salvare un documento.

 **Examples:** 

Mostra come utilizzare le proprietà del documento per visualizzare il livello di sicurezza di un documento.

```

 Document doc = new Document();

 Assert.assertEquals(DocumentSecurity.NONE, doc.getBuiltInDocumentProperties().getSecurity());

 // If we configure a document to be read-only, it will display this status using the "Security" built-in property.
 doc.getWriteProtection().setReadOnlyRecommended(true);
 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyRecommended.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_RECOMMENDED,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyRecommended.docx").getBuiltInDocumentProperties().getSecurity());

 // Write-protect a document, and then verify its security level.
 doc = new Document();

 Assert.assertFalse(doc.getWriteProtection().isWriteProtected());

 doc.getWriteProtection().setPassword("MyPassword");

 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));
 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyEnforced.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_ENFORCED,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyEnforced.docx").getBuiltInDocumentProperties().getSecurity());

 // "Security" is a descriptive property. We can edit its value manually.
 doc = new Document();

 doc.protect(ProtectionType.ALLOW_ONLY_COMMENTS, "MyPassword");
 doc.getBuiltInDocumentProperties().setSecurity(DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS);
 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").getBuiltInDocumentProperties().getSecurity());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una combinazione bitwise delle costanti [DocumentSecurity](../../com.aspose.words/documentsecurity/). |

### setSubject(String value) {#setSubject-java.lang.String}
```
public void setSubject(String value)
```


Imposta l'oggetto del documento.

 **Examples:** 

Mostra come lavorare con le proprietà di documento incorporate nella categoria "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | L'oggetto del documento. |

### setTemplate(String value) {#setTemplate-java.lang.String}
```
public void setTemplate(String value)
```


Imposta il nome informativo del modello di documento.

 **Remarks:** 

In Microsoft Word, questa proprietà è solo a scopo informativo e di solito contiene solo il nome file del modello senza il percorso.

Una stringa vuota indica che il documento è collegato al modello Normal.

Per ottenere o impostare il nome effettivo del modello allegato, utilizzare la proprietà [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String).

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il nome informativo del modello di documento. |

### setThumbnail(byte[] value) {#setThumbnail-byte}
```
public void setThumbnail(byte[] value)
```


Ottiene o imposta la miniatura del documento.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | byte[] | Il valore byte[] corrispondente. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


Imposta il titolo del documento.

 **Examples:** 

Mostra come lavorare con le proprietà di documento incorporate nella categoria "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il titolo del documento. |

### setTitlesOfParts(String[] value) {#setTitlesOfParts-java.lang.String}
```
public void setTitlesOfParts(String[] value)
```


Ogni stringa nell'array specifica il nome di una parte del documento.

 **Remarks:** 

Aspose.Words non aggiorna questa proprietà.

 **Examples:** 

Mostra la relazione tra le proprietà "HeadingPairs" e "TitlesOfParts".

```

 Document doc = new Document(getMyDir() + "Heading pairs and titles of parts.docx");

 // We can find the combined values of these collections via
 // "File" -> "Properties" -> "Advanced Properties" -> "Contents" tab.
 // The HeadingPairs property is a collection of  pairs that
 // determines how many document parts a heading spans across.
 Object[] headingPairs = doc.getBuiltInDocumentProperties().getHeadingPairs();

 // The TitlesOfParts property contains the names of parts that belong to the above headings.
 String[] titlesOfParts = doc.getBuiltInDocumentProperties().getTitlesOfParts();

 int headingPairsIndex = 0;
 int titlesOfPartsIndex = 0;
 while (headingPairsIndex < headingPairs.length) {
     System.out.println(MessageFormat.format("Parts for {0}:", headingPairs[headingPairsIndex++]));
     int partsCount = (int) headingPairs[headingPairsIndex++];

     for (int i = 0; i < partsCount; i++)
         System.out.println(MessageFormat.format("\t\"{0}\"", titlesOfParts[titlesOfPartsIndex++]));
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String[] | Il valore java.lang.String[] corrispondente. |

### setTotalEditingTime(int value) {#setTotalEditingTime-int}
```
public void setTotalEditingTime(int value)
```


Imposta il tempo totale di modifica in minuti.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il tempo totale di modifica in minuti. |

### setVersion(int value) {#setVersion-int}
```
public void setVersion(int value)
```


Rappresenta il numero di versione dell'applicazione che ha creato il documento.

 **Remarks:** 

Quando un documento è stato creato da Microsoft Word, i 16 bit più alti rappresentano la versione principale e i 16 bit più bassi rappresentano il numero di build.

 **Examples:** 

Mostra come lavorare con le proprietà del documento nella categoria "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il valore  int  corrispondente. |

### setWords(int value) {#setWords-int}
```
public void setWords(int value)
```


Rappresenta una stima del numero di parole nel documento.

 **Remarks:** 

Aspose.Words aggiorna questa proprietà quando chiami [Document.updateWordCount()](../../com.aspose.words/document/\\#updateWordCount).

 **Examples:** 

Mostra come aggiornare tutte le etichette delle liste in un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Mostra come lavorare con le proprietà del documento nella categoria "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il valore  int  corrispondente. |

