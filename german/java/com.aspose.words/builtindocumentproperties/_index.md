---
title: "BuiltInDocumentProperties"
linktitle: "BuiltInDocumentProperties"
second_title: "Aspose.Words für Java"
description: "Eine Sammlung von integrierten Dokumenteigenschaften in Java."
type: docs
weight: 57
url: /de/java/com.aspose.words/builtindocumentproperties/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.DocumentPropertyCollection](../../com.aspose.words/documentpropertycollection/)
```
public class BuiltInDocumentProperties extends DocumentPropertyCollection
```

Eine Sammlung von integrierten Dokumenteigenschaften.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Work with Document Properties ][Work with Document Properties].

 **Remarks:** 

Bietet Zugriff auf [DocumentProperty](../../com.aspose.words/documentproperty/)‑Objekte über deren Namen (unter Verwendung eines Indexers) und über eine Reihe typisierter Eigenschaften, die Werte des entsprechenden Typs zurückgeben.

Die Namen der Eigenschaften sind nicht zwischen Groß‑ und Kleinschreibung unterscheidend.

Die Eigenschaften in der Sammlung werden alphabetisch nach Namen sortiert.


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [clear()](#clear) | Entfernt alle Eigenschaften aus der Sammlung. |
| [contains(String name)](#contains-java.lang.String) | Gibt  true  zurück, wenn eine Eigenschaft mit dem angegebenen Namen in der Sammlung existiert. |
| [get(int index)](#get-int) | Gibt ein [DocumentProperty](../../com.aspose.words/documentproperty/) Objekt nach Index zurück. |
| [get(String name)](#get-java.lang.String) | Gibt ein [DocumentProperty](../../com.aspose.words/documentproperty/)‑Objekt zurück. |
| [getAuthor()](#getAuthor) | Ermittelt den Namen des Autors des Dokuments. |
| [getBytes()](#getBytes) | Stellt eine Schätzung der Anzahl von Bytes im Dokument dar. |
| [getCategory()](#getCategory) | Ermittelt die Kategorie des Dokuments. |
| [getCharacters()](#getCharacters) | Stellt eine Schätzung der Anzahl von Zeichen im Dokument dar. |
| [getCharactersWithSpaces()](#getCharactersWithSpaces) | Stellt eine Schätzung der Anzahl von Zeichen (einschließlich Leerzeichen) im Dokument dar. |
| [getComments()](#getComments) | Ermittelt die Dokumentkommentare. |
| [getCompany()](#getCompany) | Ermittelt die Firmen‑Eigenschaft. |
| [getContentStatus()](#getContentStatus) | Ermittelt den Inhaltsstatus des Dokuments. |
| [getContentType()](#getContentType) | Ermittelt den Inhaltstyp des Dokuments. |
| [getCount()](#getCount) | Ermittelt die Anzahl der Elemente in der Sammlung. |
| [getCreatedTime()](#getCreatedTime) | Ermittelt das Erstellungsdatum des Dokuments in UTC. |
| [getHeadingPairs()](#getHeadingPairs) | Gibt die Dokumentüberschriften und deren Namen an. |
| [getHyperlinkBase()](#getHyperlinkBase) | Gibt die Basiszeichenfolge an, die für die Auswertung relativer Hyperlinks in diesem Dokument verwendet wird. |
| [getHyperlinksChanged()](#getHyperlinksChanged) | Gibt an, ob Hyperlinks in einem Dokument geändert wurden. |
| [getKeywords()](#getKeywords) | Ermittelt die Schlüsselwörter des Dokuments. |
| [getLastPrinted()](#getLastPrinted) | Ermittelt das Datum, an dem das Dokument zuletzt in UTC gedruckt wurde. |
| [getLastSavedBy()](#getLastSavedBy) | Ermittelt den Namen des letzten Autors. |
| [getLastSavedTime()](#getLastSavedTime) | Ermittelt die Uhrzeit der letzten Speicherung in UTC. |
| [getLines()](#getLines) | Stellt eine Schätzung der Zeilenanzahl im Dokument dar. |
| [getLinksUpToDate()](#getLinksUpToDate) | Gibt an, ob Hyperlinks in einem Dokument aktuell sind. |
| [getManager()](#getManager) | Ermittelt die Manager-Eigenschaft. |
| [getNameOfApplication()](#getNameOfApplication) | Ermittelt den Namen der Anwendung. |
| [getPages()](#getPages) | Stellt eine Schätzung der Seitenanzahl im Dokument dar. |
| [getParagraphs()](#getParagraphs) | Stellt eine Schätzung der Absatzanzahl im Dokument dar. |
| [getRevisionNumber()](#getRevisionNumber) | Ermittelt die Revisionsnummer des Dokuments. |
| [getScaleCrop()](#getScaleCrop) | Gibt an, ob das Dokument‑Vorschaubild beschnitten oder skaliert wird, um in die Anzeige zu passen. |
| [getSecurity()](#getSecurity) | Gibt die Sicherheitsstufe eines Dokuments als numerischen Wert an. |
| [getSharedDocument()](#getSharedDocument) | Gibt an, ob das Dokument ein freigegebenes Dokument ist. |
| [getSubject()](#getSubject) | Ermittelt den Betreff des Dokuments. |
| [getTemplate()](#getTemplate) | Ermittelt den informativen Namen der Dokumentvorlage. |
| [getThumbnail()](#getThumbnail) | Ermittelt oder legt das Vorschaubild des Dokuments fest. |
| [getTitle()](#getTitle) | Ermittelt den Titel des Dokuments. |
| [getTitlesOfParts()](#getTitlesOfParts) | Jeder String im Array gibt den Namen eines Teils im Dokument an. |
| [getTotalEditingTime()](#getTotalEditingTime) | Ermittelt die gesamte Bearbeitungszeit in Minuten. |
| [getVersion()](#getVersion) | Stellt die Versionsnummer der Anwendung dar, die das Dokument erstellt hat. |
| [getWords()](#getWords) | Stellt eine Schätzung der Wortanzahl im Dokument dar. |
| [indexOf(String name)](#indexOf-java.lang.String) | Ermittelt den Index einer Eigenschaft anhand ihres Namens. |
| [iterator()](#iterator) | Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [remove(String name)](#remove-java.lang.String) | Entfernt eine Eigenschaft mit dem angegebenen Namen aus der Sammlung. |
| [removeAt(int index)](#removeAt-int) | Entfernt eine Eigenschaft am angegebenen Index. |
| [setAuthor(String value)](#setAuthor-java.lang.String) | Legt den Namen des Autors des Dokuments fest. |
| [setBytes(int value)](#setBytes-int) | Stellt eine Schätzung der Anzahl von Bytes im Dokument dar. |
| [setCategory(String value)](#setCategory-java.lang.String) | Legt die Kategorie des Dokuments fest. |
| [setCharacters(int value)](#setCharacters-int) | Stellt eine Schätzung der Anzahl von Zeichen im Dokument dar. |
| [setCharactersWithSpaces(int value)](#setCharactersWithSpaces-int) | Stellt eine Schätzung der Anzahl von Zeichen (einschließlich Leerzeichen) im Dokument dar. |
| [setComments(String value)](#setComments-java.lang.String) | Legt die Dokumentkommentare fest. |
| [setCompany(String value)](#setCompany-java.lang.String) | Legt die Firmen-Eigenschaft fest. |
| [setContentStatus(String value)](#setContentStatus-java.lang.String) | Legt den Inhaltsstatus des Dokuments fest. |
| [setContentType(String value)](#setContentType-java.lang.String) | Legt den Inhaltstyp des Dokuments fest. |
| [setCreatedTime(Date value)](#setCreatedTime-java.util.Date) | Legt das Erstellungsdatum des Dokuments in UTC fest. |
| [setHeadingPairs(Object[] value)](#setHeadingPairs-java.lang.Object) | Gibt die Dokumentüberschriften und deren Namen an. |
| [setHyperlinkBase(String value)](#setHyperlinkBase-java.lang.String) | Gibt die Basiszeichenfolge an, die für die Auswertung relativer Hyperlinks in diesem Dokument verwendet wird. |
| [setKeywords(String value)](#setKeywords-java.lang.String) | Legt die Dokument-Schlüsselwörter fest. |
| [setLastPrinted(Date value)](#setLastPrinted-java.util.Date) | Legt das Datum fest, an dem das Dokument zuletzt in UTC gedruckt wurde. |
| [setLastSavedBy(String value)](#setLastSavedBy-java.lang.String) | Legt den Namen des letzten Autors fest. |
| [setLastSavedTime(Date value)](#setLastSavedTime-java.util.Date) | Legt die Uhrzeit der letzten Speicherung in UTC fest. |
| [setLines(int value)](#setLines-int) | Stellt eine Schätzung der Zeilenanzahl im Dokument dar. |
| [setLinksUpToDate(boolean value)](#setLinksUpToDate-boolean) | Gibt an, ob Hyperlinks in einem Dokument aktuell sind. |
| [setManager(String value)](#setManager-java.lang.String) | Legt die Manager-Eigenschaft fest. |
| [setNameOfApplication(String value)](#setNameOfApplication-java.lang.String) | Legt den Namen der Anwendung fest. |
| [setPages(int value)](#setPages-int) | Stellt eine Schätzung der Seitenanzahl im Dokument dar. |
| [setParagraphs(int value)](#setParagraphs-int) | Stellt eine Schätzung der Absatzanzahl im Dokument dar. |
| [setRevisionNumber(int value)](#setRevisionNumber-int) | Legt die Dokumentversionsnummer fest. |
| [setSecurity(int value)](#setSecurity-int) | Gibt die Sicherheitsstufe eines Dokuments als numerischen Wert an. |
| [setSubject(String value)](#setSubject-java.lang.String) | Legt den Betreff des Dokuments fest. |
| [setTemplate(String value)](#setTemplate-java.lang.String) | Legt den informativen Namen der Dokumentvorlage fest. |
| [setThumbnail(byte[] value)](#setThumbnail-byte) | Ermittelt oder legt das Vorschaubild des Dokuments fest. |
| [setTitle(String value)](#setTitle-java.lang.String) | Legt den Titel des Dokuments fest. |
| [setTitlesOfParts(String[] value)](#setTitlesOfParts-java.lang.String) | Jeder String im Array gibt den Namen eines Teils im Dokument an. |
| [setTotalEditingTime(int value)](#setTotalEditingTime-int) | Legt die gesamte Bearbeitungszeit in Minuten fest. |
| [setVersion(int value)](#setVersion-int) | Stellt die Versionsnummer der Anwendung dar, die das Dokument erstellt hat. |
| [setWords(int value)](#setWords-int) | Stellt eine Schätzung der Wortanzahl im Dokument dar. |
### clear() {#clear}
```
public void clear()
```


Entfernt alle Eigenschaften aus der Sammlung.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

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


Gibt  true  zurück, wenn eine Eigenschaft mit dem angegebenen Namen in der Sammlung existiert.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der nicht‑groß-/kleinschreibungssensible Name der Eigenschaft. |

**Returns:**
boolean -  true  wenn die Eigenschaft in der Sammlung existiert;  false  sonst.
### get(int index) {#get-int}
```
public DocumentProperty get(int index)
```


Gibt ein [DocumentProperty](../../com.aspose.words/documentproperty/) Objekt nach Index zurück.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteigenschaften arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int | Nullbasierter Index des zu holenden [DocumentProperty](../../com.aspose.words/documentproperty/). |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - A [DocumentProperty](../../com.aspose.words/documentproperty/) object by index.
### get(String name) {#get-java.lang.String}
```
public DocumentProperty get(String name)
```


Gibt ein [DocumentProperty](../../com.aspose.words/documentproperty/) Objekt zurück.  Gibt ein [DocumentProperty](../../com.aspose.words/documentproperty/) Objekt anhand des Namens der Eigenschaft zurück.

 **Remarks:** 

Die Zeichenkettennamen der Eigenschaften entsprechen den Namen der typisierten Eigenschaften, die von [BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties/) verfügbar sind.

Wenn Sie eine Eigenschaft anfordern, die im Dokument nicht vorhanden ist, deren Name jedoch als gültiger integrierter Name erkannt wird, wird ein neues [DocumentProperty](../../com.aspose.words/documentproperty/) erstellt, zur Sammlung hinzugefügt und zurückgegeben. Der neu erstellten Eigenschaft wird ein Standardwert zugewiesen (leere Zeichenkette, Null,  false  oder DateTime.MinValue, abhängig vom Typ der integrierten Eigenschaft).

Wenn Sie eine Eigenschaft anfordern, die im Dokument nicht vorhanden ist und deren Name nicht als integrierter Name erkannt wird, wird ein  null  zurückgegeben.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteigenschaften arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der nicht‑groß-/kleinschreibungssensible Name der abzurufenden Eigenschaft. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The corresponding [DocumentProperty](../../com.aspose.words/documentproperty/) value.
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Ermittelt den Namen des Autors des Dokuments.

 **Examples:** 

Zeigt, wie man mit integrierten Dokumenteigenschaften in der Kategorie \"Description\" arbeitet.

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
java.lang.String - Der Name des Autors des Dokuments.
### getBytes() {#getBytes}
```
public int getBytes()
```


Stellt eine Schätzung der Anzahl von Bytes im Dokument dar.

 **Remarks:** 

Microsoft Word setzt diese Eigenschaft nicht immer.

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
int - Der entsprechende int-Wert.
### getCategory() {#getCategory}
```
public String getCategory()
```


Ermittelt die Kategorie des Dokuments.

 **Examples:** 

Zeigt, wie man mit integrierten Dokumenteigenschaften in der Kategorie \"Description\" arbeitet.

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
java.lang.String - Die Kategorie des Dokuments.
### getCharacters() {#getCharacters}
```
public int getCharacters()
```


Stellt eine Schätzung der Anzahl von Zeichen im Dokument dar.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft, wenn Sie [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount) aufrufen.

 **Examples:** 

Zeigt, wie man alle Listeneinträge in einem Dokument aktualisiert.

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

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
int - Der entsprechende int-Wert.
### getCharactersWithSpaces() {#getCharactersWithSpaces}
```
public int getCharactersWithSpaces()
```


Stellt eine Schätzung der Anzahl von Zeichen (einschließlich Leerzeichen) im Dokument dar.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft, wenn Sie [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount) aufrufen.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
int - Der entsprechende int-Wert.
### getComments() {#getComments}
```
public String getComments()
```


Ermittelt die Dokumentkommentare.

 **Examples:** 

Zeigt, wie man mit integrierten Dokumenteigenschaften in der Kategorie \"Description\" arbeitet.

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
java.lang.String - Die Dokumentkommentare.
### getCompany() {#getCompany}
```
public String getCompany()
```


Ermittelt die Firmen‑Eigenschaft.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
java.lang.String - Die Firmen-Eigenschaft.
### getContentStatus() {#getContentStatus}
```
public String getContentStatus()
```


Ermittelt den Inhaltsstatus des Dokuments.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
java.lang.String - Der Inhaltsstatus des Dokuments.
### getContentType() {#getContentType}
```
public String getContentType()
```


Ermittelt den Inhaltstyp des Dokuments.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
java.lang.String - Der Inhaltstyp des Dokuments.
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt die Anzahl der Elemente in der Sammlung.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteigenschaften arbeitet.

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
int - Anzahl der Elemente in der Sammlung.
### getCreatedTime() {#getCreatedTime}
```
public Date getCreatedTime()
```


Ermittelt das Erstellungsdatum des Dokuments in UTC.

 **Remarks:** 

Für Dokumente, die aus dem RTF-Format stammen, gibt diese Eigenschaft die lokale Zeit des Rechners des Autors zum Zeitpunkt der Dokumenterstellung zurück.

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
java.util.Date - Datum der Dokumenterstellung in UTC.
### getHeadingPairs() {#getHeadingPairs}
```
public Object[] getHeadingPairs()
```


Gibt die Dokumentüberschriften und deren Namen an.

 **Remarks:** 

Jedes Überschrifts-Paar belegt zwei Elemente in diesem Array.

Das erste Element des Paares ist ein java.lang.String und gibt den Überschriftsnamen an. Das zweite Element des Paares ist ein int und gibt die Anzahl der Dokumentteile für diese Überschrift in der Eigenschaft [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String) an.

Die Gesamtsumme der Zählwerte für alle Überschrifts-Paare in dieser Eigenschaft muss gleich der Anzahl der Elemente in der Eigenschaft [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String) sein.

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt die Beziehung zwischen den Eigenschaften "HeadingPairs" und "TitlesOfParts".

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
java.lang.Object[] - Der entsprechende java.lang.Object[]-Wert.
### getHyperlinkBase() {#getHyperlinkBase}
```
public String getHyperlinkBase()
```


Gibt die Basiszeichenfolge an, die für die Auswertung relativer Hyperlinks in diesem Dokument verwendet wird.

 **Remarks:** 

Aspose.Words verwendet diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man den Basisanteil eines Hyperlinks in den Dokumenteneigenschaften speichert.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getHyperlinksChanged() {#getHyperlinksChanged}
```
public boolean getHyperlinksChanged()
```


Gibt an, ob Hyperlinks in einem Dokument geändert wurden.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man erweiterte Eigenschaften abruft.

```

 Document doc = new Document(getMyDir() + "Extended properties.docx");
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getScaleCrop());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getSharedDocument());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getHyperlinksChanged());
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getKeywords() {#getKeywords}
```
public String getKeywords()
```


Ermittelt die Schlüsselwörter des Dokuments.

 **Examples:** 

Zeigt, wie man mit integrierten Dokumenteigenschaften in der Kategorie \"Description\" arbeitet.

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
java.lang.String - Die Dokument-Schlüsselwörter.
### getLastPrinted() {#getLastPrinted}
```
public Date getLastPrinted()
```


Ermittelt das Datum, an dem das Dokument zuletzt in UTC gedruckt wurde.

 **Remarks:** 

Für Dokumente, die aus dem RTF-Format stammen, gibt diese Eigenschaft die lokale Zeit des letzten Druckvorgangs zurück.

Wenn das Dokument nie gedruckt wurde, gibt diese Eigenschaft DateTime.MinValue zurück.

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
java.util.Date - Das Datum, an dem das Dokument zuletzt in UTC gedruckt wurde.
### getLastSavedBy() {#getLastSavedBy}
```
public String getLastSavedBy()
```


Ermittelt den Namen des letzten Autors.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
java.lang.String - Der Name des letzten Autors.
### getLastSavedTime() {#getLastSavedTime}
```
public Date getLastSavedTime()
```


Ermittelt die Uhrzeit der letzten Speicherung in UTC.

 **Remarks:** 

Für Dokumente, die aus dem RTF-Format stammen, gibt diese Eigenschaft die lokale Zeit der letzten Speicheroperation zurück.

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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

Zeigt, wie das Feld SAVEDATE verwendet wird, um das Datum/Uhrzeit der zuletzt mit Microsoft Word durchgeführten Speicheroperation des Dokuments anzuzeigen.

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
java.util.Date - Die Zeit der letzten Speicherung in UTC.
### getLines() {#getLines}
```
public int getLines()
```


Stellt eine Schätzung der Zeilenanzahl im Dokument dar.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft, wenn Sie [Document.updateWordCount(boolean)](../../com.aspose.words/document/\#updateWordCount-boolean) aufrufen.

 **Examples:** 

Zeigt, wie man alle Listeneinträge in einem Dokument aktualisiert.

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

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
int - Der entsprechende int-Wert.
### getLinksUpToDate() {#getLinksUpToDate}
```
public boolean getLinksUpToDate()
```


Gibt an, ob Hyperlinks in einem Dokument aktuell sind.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
boolean - Der entsprechende  boolean  Wert.
### getManager() {#getManager}
```
public String getManager()
```


Ermittelt die Manager-Eigenschaft.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
java.lang.String - Die Manager‑Eigenschaft.
### getNameOfApplication() {#getNameOfApplication}
```
public String getNameOfApplication()
```


Ermittelt den Namen der Anwendung.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
java.lang.String - Der Name der Anwendung.
### getPages() {#getPages}
```
public int getPages()
```


Stellt eine Schätzung der Seitenanzahl im Dokument dar.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft, wenn Sie [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) aufrufen.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
int - Der entsprechende int-Wert.
### getParagraphs() {#getParagraphs}
```
public int getParagraphs()
```


Stellt eine Schätzung der Absatzanzahl im Dokument dar.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft, wenn Sie [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount) aufrufen.

 **Examples:** 

Zeigt, wie man alle Listeneinträge in einem Dokument aktualisiert.

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

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
int - Der entsprechende int-Wert.
### getRevisionNumber() {#getRevisionNumber}
```
public int getRevisionNumber()
```


Ermittelt die Revisionsnummer des Dokuments.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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

Zeigt, wie man mit REVNUM‑Feldern arbeitet.

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
int - Die Dokumentversionsnummer.
### getScaleCrop() {#getScaleCrop}
```
public boolean getScaleCrop()
```


Gibt an, ob das Dokument‑Vorschaubild beschnitten oder skaliert wird, um in die Anzeige zu passen.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man erweiterte Eigenschaften abruft.

```

 Document doc = new Document(getMyDir() + "Extended properties.docx");
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getScaleCrop());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getSharedDocument());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getHyperlinksChanged());
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getSecurity() {#getSecurity}
```
public int getSecurity()
```


Gibt die Sicherheitsstufe eines Dokuments als numerischen Wert an.

 **Remarks:** 

Verwenden Sie diese Eigenschaft nur zu Informationszwecken, da Microsoft Word diese Eigenschaft nicht immer setzt. Diese Eigenschaft ist nur in DOC‑ und OOXML‑Dokumenten verfügbar.

Um ein Dokument zu schützen oder den Schutz aufzuheben, verwenden Sie die **M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)**‑ und [Document.unprotect()](../../com.aspose.words/document/\#unprotect)‑Methoden.

Aspose.Words aktualisiert diese Eigenschaft vor dem Speichern eines Dokuments auf einen korrekten Wert.

 **Examples:** 

Zeigt, wie Dokumenteigenschaften verwendet werden, um die Sicherheitsstufe eines Dokuments anzuzeigen.

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
int - Der entsprechende int‑Wert. Der zurückgegebene Wert ist eine bitweise Kombination der Konstanten von [DocumentSecurity](../../com.aspose.words/documentsecurity/).
### getSharedDocument() {#getSharedDocument}
```
public boolean getSharedDocument()
```


Gibt an, ob das Dokument ein freigegebenes Dokument ist.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man erweiterte Eigenschaften abruft.

```

 Document doc = new Document(getMyDir() + "Extended properties.docx");
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getScaleCrop());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getSharedDocument());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getHyperlinksChanged());
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getSubject() {#getSubject}
```
public String getSubject()
```


Ermittelt den Betreff des Dokuments.

 **Examples:** 

Zeigt, wie man mit integrierten Dokumenteigenschaften in der Kategorie \"Description\" arbeitet.

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
java.lang.String - Der Betreff des Dokuments.
### getTemplate() {#getTemplate}
```
public String getTemplate()
```


Ermittelt den informativen Namen der Dokumentvorlage.

 **Remarks:** 

In Microsoft Word dient diese Eigenschaft nur zu Informationszwecken und enthält normalerweise nur den Dateinamen der Vorlage ohne Pfad.

Ein leerer String bedeutet, dass das Dokument an die Normal‑Vorlage angehängt ist.

Um den tatsächlichen Namen der angehängten Vorlage zu erhalten oder festzulegen, verwenden Sie die Eigenschaft [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String).

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
java.lang.String - Der informative Name der Dokumentvorlage.
### getThumbnail() {#getThumbnail}
```
public byte[] getThumbnail()
```


Ermittelt oder legt das Vorschaubild des Dokuments fest.

**Returns:**
byte[] - Der entsprechende byte[]-Wert.
### getTitle() {#getTitle}
```
public String getTitle()
```


Ermittelt den Titel des Dokuments.

 **Examples:** 

Zeigt, wie man mit integrierten Dokumenteigenschaften in der Kategorie \"Description\" arbeitet.

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
java.lang.String - Der Titel des Dokuments.
### getTitlesOfParts() {#getTitlesOfParts}
```
public String[] getTitlesOfParts()
```


Jeder String im Array gibt den Namen eines Teils im Dokument an.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt die Beziehung zwischen den Eigenschaften "HeadingPairs" und "TitlesOfParts".

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
java.lang.String[] - Der entsprechende java.lang.String[]‑Wert.
### getTotalEditingTime() {#getTotalEditingTime}
```
public int getTotalEditingTime()
```


Ermittelt die gesamte Bearbeitungszeit in Minuten.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
int - Die gesamte Bearbeitungszeit in Minuten.
### getVersion() {#getVersion}
```
public int getVersion()
```


Stellt die Versionsnummer der Anwendung dar, die das Dokument erstellt hat.

 **Remarks:** 

Wenn ein Dokument von Microsoft Word erstellt wurde, stellen die oberen 16 Bits die Hauptversion und die unteren 16 Bits die Build‑Nummer dar.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
int - Der entsprechende int-Wert.
### getWords() {#getWords}
```
public int getWords()
```


Stellt eine Schätzung der Wortanzahl im Dokument dar.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft, wenn Sie [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount) aufrufen.

 **Examples:** 

Zeigt, wie man alle Listeneinträge in einem Dokument aktualisiert.

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

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
int - Der entsprechende int-Wert.
### indexOf(String name) {#indexOf-java.lang.String}
```
public int indexOf(String name)
```


Ermittelt den Index einer Eigenschaft anhand ihres Namens.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der nicht‑groß-/kleinschreibungssensible Name der Eigenschaft. |

**Returns:**
int - Der nullbasierte Index. Negativer Wert, wenn nicht gefunden.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

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


Entfernt eine Eigenschaft mit dem angegebenen Namen aus der Sammlung.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der nicht‑groß-/kleinschreibungssensible Name der Eigenschaft. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Entfernt eine Eigenschaft am angegebenen Index.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der nullbasierte Index. |

### setAuthor(String value) {#setAuthor-java.lang.String}
```
public void setAuthor(String value)
```


Legt den Namen des Autors des Dokuments fest.

 **Examples:** 

Zeigt, wie man mit integrierten Dokumenteigenschaften in der Kategorie \"Description\" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Name des Autors des Dokuments. |

### setBytes(int value) {#setBytes-int}
```
public void setBytes(int value)
```


Stellt eine Schätzung der Anzahl von Bytes im Dokument dar.

 **Remarks:** 

Microsoft Word setzt diese Eigenschaft nicht immer.

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setCategory(String value) {#setCategory-java.lang.String}
```
public void setCategory(String value)
```


Legt die Kategorie des Dokuments fest.

 **Examples:** 

Zeigt, wie man mit integrierten Dokumenteigenschaften in der Kategorie \"Description\" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Die Kategorie des Dokuments. |

### setCharacters(int value) {#setCharacters-int}
```
public void setCharacters(int value)
```


Stellt eine Schätzung der Anzahl von Zeichen im Dokument dar.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft, wenn Sie [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount) aufrufen.

 **Examples:** 

Zeigt, wie man alle Listeneinträge in einem Dokument aktualisiert.

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

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setCharactersWithSpaces(int value) {#setCharactersWithSpaces-int}
```
public void setCharactersWithSpaces(int value)
```


Stellt eine Schätzung der Anzahl von Zeichen (einschließlich Leerzeichen) im Dokument dar.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft, wenn Sie [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount) aufrufen.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setComments(String value) {#setComments-java.lang.String}
```
public void setComments(String value)
```


Legt die Dokumentkommentare fest.

 **Examples:** 

Zeigt, wie man mit integrierten Dokumenteigenschaften in der Kategorie \"Description\" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Die Dokumentkommentare. |

### setCompany(String value) {#setCompany-java.lang.String}
```
public void setCompany(String value)
```


Legt die Firmen-Eigenschaft fest.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Die Company-Eigenschaft. |

### setContentStatus(String value) {#setContentStatus-java.lang.String}
```
public void setContentStatus(String value)
```


Legt den Inhaltsstatus des Dokuments fest.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Inhaltsstatus des Dokuments. |

### setContentType(String value) {#setContentType-java.lang.String}
```
public void setContentType(String value)
```


Legt den Inhaltstyp des Dokuments fest.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Inhaltstyp des Dokuments. |

### setCreatedTime(Date value) {#setCreatedTime-java.util.Date}
```
public void setCreatedTime(Date value)
```


Legt das Erstellungsdatum des Dokuments in UTC fest.

 **Remarks:** 

Für Dokumente, die aus dem RTF-Format stammen, gibt diese Eigenschaft die lokale Zeit des Rechners des Autors zum Zeitpunkt der Dokumenterstellung zurück.

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.util.Date | Datum der Dokumenterstellung in UTC. |

### setHeadingPairs(Object[] value) {#setHeadingPairs-java.lang.Object}
```
public void setHeadingPairs(Object[] value)
```


Gibt die Dokumentüberschriften und deren Namen an.

 **Remarks:** 

Jedes Überschrifts-Paar belegt zwei Elemente in diesem Array.

Das erste Element des Paares ist ein java.lang.String und gibt den Überschriftsnamen an. Das zweite Element des Paares ist ein int und gibt die Anzahl der Dokumentteile für diese Überschrift in der Eigenschaft [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String) an.

Die Gesamtsumme der Zählwerte für alle Überschrifts-Paare in dieser Eigenschaft muss gleich der Anzahl der Elemente in der Eigenschaft [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String) sein.

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt die Beziehung zwischen den Eigenschaften "HeadingPairs" und "TitlesOfParts".

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.Object[] | Der entsprechende java.lang.Object[]-Wert. |

### setHyperlinkBase(String value) {#setHyperlinkBase-java.lang.String}
```
public void setHyperlinkBase(String value)
```


Gibt die Basiszeichenfolge an, die für die Auswertung relativer Hyperlinks in diesem Dokument verwendet wird.

 **Remarks:** 

Aspose.Words verwendet diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man den Basisanteil eines Hyperlinks in den Dokumenteneigenschaften speichert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setKeywords(String value) {#setKeywords-java.lang.String}
```
public void setKeywords(String value)
```


Legt die Dokument-Schlüsselwörter fest.

 **Examples:** 

Zeigt, wie man mit integrierten Dokumenteigenschaften in der Kategorie \"Description\" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Die Dokumentschlüsselwörter. |

### setLastPrinted(Date value) {#setLastPrinted-java.util.Date}
```
public void setLastPrinted(Date value)
```


Legt das Datum fest, an dem das Dokument zuletzt in UTC gedruckt wurde.

 **Remarks:** 

Für Dokumente, die aus dem RTF-Format stammen, gibt diese Eigenschaft die lokale Zeit des letzten Druckvorgangs zurück.

Wenn das Dokument nie gedruckt wurde, gibt diese Eigenschaft DateTime.MinValue zurück.

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.util.Date | Das Datum, an dem das Dokument zuletzt in UTC gedruckt wurde. |

### setLastSavedBy(String value) {#setLastSavedBy-java.lang.String}
```
public void setLastSavedBy(String value)
```


Legt den Namen des letzten Autors fest.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Name des letzten Autors. |

### setLastSavedTime(Date value) {#setLastSavedTime-java.util.Date}
```
public void setLastSavedTime(Date value)
```


Legt die Uhrzeit der letzten Speicherung in UTC fest.

 **Remarks:** 

Für Dokumente, die aus dem RTF-Format stammen, gibt diese Eigenschaft die lokale Zeit der letzten Speicheroperation zurück.

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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

Zeigt, wie das Feld SAVEDATE verwendet wird, um das Datum/Uhrzeit der zuletzt mit Microsoft Word durchgeführten Speicheroperation des Dokuments anzuzeigen.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.util.Date | Die Uhrzeit der letzten Speicherung in UTC. |

### setLines(int value) {#setLines-int}
```
public void setLines(int value)
```


Stellt eine Schätzung der Zeilenanzahl im Dokument dar.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft, wenn Sie [Document.updateWordCount(boolean)](../../com.aspose.words/document/\#updateWordCount-boolean) aufrufen.

 **Examples:** 

Zeigt, wie man alle Listeneinträge in einem Dokument aktualisiert.

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

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setLinksUpToDate(boolean value) {#setLinksUpToDate-boolean}
```
public void setLinksUpToDate(boolean value)
```


Gibt an, ob Hyperlinks in einem Dokument aktuell sind.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setManager(String value) {#setManager-java.lang.String}
```
public void setManager(String value)
```


Legt die Manager-Eigenschaft fest.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Die Manager-Eigenschaft. |

### setNameOfApplication(String value) {#setNameOfApplication-java.lang.String}
```
public void setNameOfApplication(String value)
```


Legt den Namen der Anwendung fest.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Name der Anwendung. |

### setPages(int value) {#setPages-int}
```
public void setPages(int value)
```


Stellt eine Schätzung der Seitenanzahl im Dokument dar.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft, wenn Sie [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) aufrufen.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setParagraphs(int value) {#setParagraphs-int}
```
public void setParagraphs(int value)
```


Stellt eine Schätzung der Absatzanzahl im Dokument dar.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft, wenn Sie [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount) aufrufen.

 **Examples:** 

Zeigt, wie man alle Listeneinträge in einem Dokument aktualisiert.

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

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setRevisionNumber(int value) {#setRevisionNumber-int}
```
public void setRevisionNumber(int value)
```


Legt die Dokumentversionsnummer fest.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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

Zeigt, wie man mit REVNUM‑Feldern arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Die Dokumentversionsnummer. |

### setSecurity(int value) {#setSecurity-int}
```
public void setSecurity(int value)
```


Gibt die Sicherheitsstufe eines Dokuments als numerischen Wert an.

 **Remarks:** 

Verwenden Sie diese Eigenschaft nur zu Informationszwecken, da Microsoft Word diese Eigenschaft nicht immer setzt. Diese Eigenschaft ist nur in DOC‑ und OOXML‑Dokumenten verfügbar.

Um ein Dokument zu schützen oder den Schutz aufzuheben, verwenden Sie die **M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)**‑ und [Document.unprotect()](../../com.aspose.words/document/\#unprotect)‑Methoden.

Aspose.Words aktualisiert diese Eigenschaft vor dem Speichern eines Dokuments auf einen korrekten Wert.

 **Examples:** 

Zeigt, wie Dokumenteigenschaften verwendet werden, um die Sicherheitsstufe eines Dokuments anzuzeigen.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende  int  Wert. Der Wert muss eine bitweise Kombination der [DocumentSecurity](../../com.aspose.words/documentsecurity/) Konstanten sein. |

### setSubject(String value) {#setSubject-java.lang.String}
```
public void setSubject(String value)
```


Legt den Betreff des Dokuments fest.

 **Examples:** 

Zeigt, wie man mit integrierten Dokumenteigenschaften in der Kategorie \"Description\" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Betreff des Dokuments. |

### setTemplate(String value) {#setTemplate-java.lang.String}
```
public void setTemplate(String value)
```


Legt den informativen Namen der Dokumentvorlage fest.

 **Remarks:** 

In Microsoft Word dient diese Eigenschaft nur zu Informationszwecken und enthält normalerweise nur den Dateinamen der Vorlage ohne Pfad.

Ein leerer String bedeutet, dass das Dokument an die Normal‑Vorlage angehängt ist.

Um den tatsächlichen Namen der angehängten Vorlage zu erhalten oder festzulegen, verwenden Sie die Eigenschaft [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String).

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Informationsname der Dokumentvorlage. |

### setThumbnail(byte[] value) {#setThumbnail-byte}
```
public void setThumbnail(byte[] value)
```


Ermittelt oder legt das Vorschaubild des Dokuments fest.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | byte[] | Der entsprechende byte[]-Wert. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


Legt den Titel des Dokuments fest.

 **Examples:** 

Zeigt, wie man mit integrierten Dokumenteigenschaften in der Kategorie \"Description\" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Titel des Dokuments. |

### setTitlesOfParts(String[] value) {#setTitlesOfParts-java.lang.String}
```
public void setTitlesOfParts(String[] value)
```


Jeder String im Array gibt den Namen eines Teils im Dokument an.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft nicht.

 **Examples:** 

Zeigt die Beziehung zwischen den Eigenschaften "HeadingPairs" und "TitlesOfParts".

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String[] | Der entsprechende java.lang.String[]-Wert. |

### setTotalEditingTime(int value) {#setTotalEditingTime-int}
```
public void setTotalEditingTime(int value)
```


Legt die gesamte Bearbeitungszeit in Minuten fest.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Die gesamte Bearbeitungszeit in Minuten. |

### setVersion(int value) {#setVersion-int}
```
public void setVersion(int value)
```


Stellt die Versionsnummer der Anwendung dar, die das Dokument erstellt hat.

 **Remarks:** 

Wenn ein Dokument von Microsoft Word erstellt wurde, stellen die oberen 16 Bits die Hauptversion und die unteren 16 Bits die Build‑Nummer dar.

 **Examples:** 

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Origin" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setWords(int value) {#setWords-int}
```
public void setWords(int value)
```


Stellt eine Schätzung der Wortanzahl im Dokument dar.

 **Remarks:** 

Aspose.Words aktualisiert diese Eigenschaft, wenn Sie [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount) aufrufen.

 **Examples:** 

Zeigt, wie man alle Listeneinträge in einem Dokument aktualisiert.

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

Zeigt, wie man mit Dokumenteigenschaften in der Kategorie "Content" arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

