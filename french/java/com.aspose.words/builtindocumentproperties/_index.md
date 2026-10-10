---
title: "BuiltInDocumentProperties"
linktitle: "BuiltInDocumentProperties"
second_title: "Aspose.Words pour Java"
description: "Une collection de propriétés de document intégrées en Java."
type: docs
weight: 57
url: /fr/java/com.aspose.words/builtindocumentproperties/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.DocumentPropertyCollection](../../com.aspose.words/documentpropertycollection/)
```
public class BuiltInDocumentProperties extends DocumentPropertyCollection
```

Une collection de propriétés de document intégrées.

Pour en savoir plus, consultez l’article de documentation [ Work with Document Properties ][Work with Document Properties].

 **Remarks:** 

Fournit un accès aux objets [DocumentProperty](../../com.aspose.words/documentproperty/) par leurs noms (à l'aide d'un indexeur) et via un ensemble de propriétés typées qui renvoient des valeurs des types appropriés.

Les noms des propriétés ne sont pas sensibles à la casse.

Les propriétés de la collection sont triées alphabétiquement par nom.


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Méthodes

| Méthode | Description |
| --- | --- |
| [clear()](#clear) | Supprime toutes les propriétés de la collection. |
| [contains(String name)](#contains-java.lang.String) | Renvoie  true  si une propriété portant le nom spécifié existe dans la collection. |
| [get(int index)](#get-int) | Renvoie un objet [DocumentProperty](../../com.aspose.words/documentproperty/) par indice. |
| [get(String name)](#get-java.lang.String) | Renvoie un objet [DocumentProperty](../../com.aspose.words/documentproperty/). |
| [getAuthor()](#getAuthor) | Obtient le nom de l'auteur du document. |
| [getBytes()](#getBytes) | Représente une estimation du nombre d'octets dans le document. |
| [getCategory()](#getCategory) | Obtient la catégorie du document. |
| [getCharacters()](#getCharacters) | Représente une estimation du nombre de caractères dans le document. |
| [getCharactersWithSpaces()](#getCharactersWithSpaces) | Représente une estimation du nombre de caractères (espaces inclus) dans le document. |
| [getComments()](#getComments) | Obtient les commentaires du document. |
| [getCompany()](#getCompany) | Obtient la propriété de l'entreprise. |
| [getContentStatus()](#getContentStatus) | Obtient le statut du contenu du document. |
| [getContentType()](#getContentType) | Obtient le type de contenu du document. |
| [getCount()](#getCount) | Obtient le nombre d'éléments dans la collection. |
| [getCreatedTime()](#getCreatedTime) | Obtient la date de création du document en UTC. |
| [getHeadingPairs()](#getHeadingPairs) | Spécifie les titres du document et leurs noms. |
| [getHyperlinkBase()](#getHyperlinkBase) | Spécifie la chaîne de base utilisée pour évaluer les hyperliens relatifs dans ce document. |
| [getHyperlinksChanged()](#getHyperlinksChanged) | Indique si les hyperliens dans un document ont été modifiés. |
| [getKeywords()](#getKeywords) | Obtient les mots-clés du document. |
| [getLastPrinted()](#getLastPrinted) | Obtient la date à laquelle le document a été imprimé pour la dernière fois en UTC. |
| [getLastSavedBy()](#getLastSavedBy) | Obtient le nom du dernier auteur. |
| [getLastSavedTime()](#getLastSavedTime) | Obtient l'heure de la dernière sauvegarde en UTC. |
| [getLines()](#getLines) | Représente une estimation du nombre de lignes dans le document. |
| [getLinksUpToDate()](#getLinksUpToDate) | Indique si les hyperliens dans un document sont à jour. |
| [getManager()](#getManager) | Obtient la propriété manager. |
| [getNameOfApplication()](#getNameOfApplication) | Obtient le nom de l'application. |
| [getPages()](#getPages) | Représente une estimation du nombre de pages dans le document. |
| [getParagraphs()](#getParagraphs) | Représente une estimation du nombre de paragraphes dans le document. |
| [getRevisionNumber()](#getRevisionNumber) | Obtient le numéro de révision du document. |
| [getScaleCrop()](#getScaleCrop) | Indique si la vignette du document est recadrée ou mise à l'échelle pour s'adapter à l'affichage. |
| [getSecurity()](#getSecurity) | Spécifie le niveau de sécurité d'un document sous forme de valeur numérique. |
| [getSharedDocument()](#getSharedDocument) | Indique si le document est un document partagé. |
| [getSubject()](#getSubject) | Obtient le sujet du document. |
| [getTemplate()](#getTemplate) | Obtient le nom informatif du modèle de document. |
| [getThumbnail()](#getThumbnail) | Obtient ou définit la vignette du document. |
| [getTitle()](#getTitle) | Obtient le titre du document. |
| [getTitlesOfParts()](#getTitlesOfParts) | Chaque chaîne du tableau spécifie le nom d'une partie du document. |
| [getTotalEditingTime()](#getTotalEditingTime) | Obtient le temps total d'édition en minutes. |
| [getVersion()](#getVersion) | Représente le numéro de version de l'application qui a créé le document. |
| [getWords()](#getWords) | Représente une estimation du nombre de mots dans le document. |
| [indexOf(String name)](#indexOf-java.lang.String) | Obtient l'indice d'une propriété par son nom. |
| [iterator()](#iterator) | Renvoie un objet itérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [remove(String name)](#remove-java.lang.String) | Supprime une propriété portant le nom spécifié de la collection. |
| [removeAt(int index)](#removeAt-int) | Supprime une propriété à l'indice spécifié. |
| [setAuthor(String value)](#setAuthor-java.lang.String) | Définit le nom de l'auteur du document. |
| [setBytes(int value)](#setBytes-int) | Représente une estimation du nombre d'octets dans le document. |
| [setCategory(String value)](#setCategory-java.lang.String) | Définit la catégorie du document. |
| [setCharacters(int value)](#setCharacters-int) | Représente une estimation du nombre de caractères dans le document. |
| [setCharactersWithSpaces(int value)](#setCharactersWithSpaces-int) | Représente une estimation du nombre de caractères (espaces inclus) dans le document. |
| [setComments(String value)](#setComments-java.lang.String) | Définit les commentaires du document. |
| [setCompany(String value)](#setCompany-java.lang.String) | Définit la propriété de l'entreprise. |
| [setContentStatus(String value)](#setContentStatus-java.lang.String) | Définit le statut du contenu du document. |
| [setContentType(String value)](#setContentType-java.lang.String) | Définit le type de contenu du document. |
| [setCreatedTime(Date value)](#setCreatedTime-java.util.Date) | Définit la date de création du document en UTC. |
| [setHeadingPairs(Object[] value)](#setHeadingPairs-java.lang.Object) | Spécifie les titres du document et leurs noms. |
| [setHyperlinkBase(String value)](#setHyperlinkBase-java.lang.String) | Spécifie la chaîne de base utilisée pour évaluer les hyperliens relatifs dans ce document. |
| [setKeywords(String value)](#setKeywords-java.lang.String) | Définit les mots-clés du document. |
| [setLastPrinted(Date value)](#setLastPrinted-java.util.Date) | Définit la date à laquelle le document a été imprimé pour la dernière fois en UTC. |
| [setLastSavedBy(String value)](#setLastSavedBy-java.lang.String) | Définit le nom du dernier auteur. |
| [setLastSavedTime(Date value)](#setLastSavedTime-java.util.Date) | Définit l'heure de la dernière sauvegarde en UTC. |
| [setLines(int value)](#setLines-int) | Représente une estimation du nombre de lignes dans le document. |
| [setLinksUpToDate(boolean value)](#setLinksUpToDate-boolean) | Indique si les hyperliens dans un document sont à jour. |
| [setManager(String value)](#setManager-java.lang.String) | Définit la propriété du responsable. |
| [setNameOfApplication(String value)](#setNameOfApplication-java.lang.String) | Définit le nom de l'application. |
| [setPages(int value)](#setPages-int) | Représente une estimation du nombre de pages dans le document. |
| [setParagraphs(int value)](#setParagraphs-int) | Représente une estimation du nombre de paragraphes dans le document. |
| [setRevisionNumber(int value)](#setRevisionNumber-int) | Définit le numéro de révision du document. |
| [setSecurity(int value)](#setSecurity-int) | Spécifie le niveau de sécurité d'un document sous forme de valeur numérique. |
| [setSubject(String value)](#setSubject-java.lang.String) | Définit le sujet du document. |
| [setTemplate(String value)](#setTemplate-java.lang.String) | Définit le nom informatif du modèle de document. |
| [setThumbnail(byte[] value)](#setThumbnail-byte) | Obtient ou définit la vignette du document. |
| [setTitle(String value)](#setTitle-java.lang.String) | Définit le titre du document. |
| [setTitlesOfParts(String[] value)](#setTitlesOfParts-java.lang.String) | Chaque chaîne du tableau spécifie le nom d'une partie du document. |
| [setTotalEditingTime(int value)](#setTotalEditingTime-int) | Définit le temps total d'édition en minutes. |
| [setVersion(int value)](#setVersion-int) | Représente le numéro de version de l'application qui a créé le document. |
| [setWords(int value)](#setWords-int) | Représente une estimation du nombre de mots dans le document. |
### clear() {#clear}
```
public void clear()
```


Supprime toutes les propriétés de la collection.

 **Examples:** 

Montre comment travailler avec les propriétés personnalisées d'un document.

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


Renvoie  true  si une propriété portant le nom spécifié existe dans la collection.

 **Examples:** 

Montre comment travailler avec les propriétés personnalisées d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom de la propriété, insensible à la casse. |

**Returns:**
booléen -  true  si la propriété existe dans la collection ;  false  sinon.
### get(int index) {#get-int}
```
public DocumentProperty get(int index)
```


Renvoie un objet [DocumentProperty](../../com.aspose.words/documentproperty/) par indice.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

 **Examples:** 

Montre comment travailler avec des propriétés de document personnalisées.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | Indice basé sur zéro du [DocumentProperty](../../com.aspose.words/documentproperty/) à récupérer. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - A [DocumentProperty](../../com.aspose.words/documentproperty/) object by index.
### get(String name) {#get-java.lang.String}
```
public DocumentProperty get(String name)
```


Renvoie un objet [DocumentProperty](../../com.aspose.words/documentproperty/).  Renvoie un objet [DocumentProperty](../../com.aspose.words/documentproperty/) par le nom de la propriété.

 **Remarks:** 

Les noms de chaîne des propriétés correspondent aux noms des propriétés typées disponibles à partir de [BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties/).

Si vous demandez une propriété qui n'est pas présente dans le document, mais que le nom de la propriété est reconnu comme un nom intégré valide, une nouvelle [DocumentProperty](../../com.aspose.words/documentproperty/) est créée, ajoutée à la collection et renvoyée. La propriété nouvellement créée reçoit une valeur par défaut (chaîne vide, zéro,  false  ou DateTime.MinValue selon le type de la propriété intégrée).

Si vous demandez une propriété qui n'est pas présente dans le document et que le nom n'est pas reconnu comme un nom intégré, un  null  est renvoyé.

 **Examples:** 

Montre comment travailler avec des propriétés de document personnalisées.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom de la propriété, insensible à la casse, à récupérer. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The corresponding [DocumentProperty](../../com.aspose.words/documentproperty/) value.
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Obtient le nom de l'auteur du document.

 **Examples:** 

Montre comment travailler avec les propriétés de document intégrées dans la catégorie "Description".

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
java.lang.String - Le nom de l'auteur du document.
### getBytes() {#getBytes}
```
public int getBytes()
```


Représente une estimation du nombre d'octets dans le document.

 **Remarks:** 

Microsoft Word ne définit pas toujours cette propriété.

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
int - La valeur int correspondante.
### getCategory() {#getCategory}
```
public String getCategory()
```


Obtient la catégorie du document.

 **Examples:** 

Montre comment travailler avec les propriétés de document intégrées dans la catégorie "Description".

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
java.lang.String - La catégorie du document.
### getCharacters() {#getCharacters}
```
public int getCharacters()
```


Représente une estimation du nombre de caractères dans le document.

 **Remarks:** 

Aspose.Words met à jour cette propriété lorsque vous appelez [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Montre comment mettre à jour toutes les étiquettes de listes dans un document.

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

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
int - La valeur int correspondante.
### getCharactersWithSpaces() {#getCharactersWithSpaces}
```
public int getCharactersWithSpaces()
```


Représente une estimation du nombre de caractères (espaces inclus) dans le document.

 **Remarks:** 

Aspose.Words met à jour cette propriété lorsque vous appelez [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
int - La valeur int correspondante.
### getComments() {#getComments}
```
public String getComments()
```


Obtient les commentaires du document.

 **Examples:** 

Montre comment travailler avec les propriétés de document intégrées dans la catégorie "Description".

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
java.lang.String - Les commentaires du document.
### getCompany() {#getCompany}
```
public String getCompany()
```


Obtient la propriété de l'entreprise.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
java.lang.String - La propriété de l'entreprise.
### getContentStatus() {#getContentStatus}
```
public String getContentStatus()
```


Obtient le statut du contenu du document.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
java.lang.String - L'état du contenu du document.
### getContentType() {#getContentType}
```
public String getContentType()
```


Obtient le type de contenu du document.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
java.lang.String - Le type de contenu du document.
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre d'éléments dans la collection.

 **Examples:** 

Montre comment travailler avec des propriétés de document personnalisées.

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
int - Nombre d'éléments dans la collection.
### getCreatedTime() {#getCreatedTime}
```
public Date getCreatedTime()
```


Obtient la date de création du document en UTC.

 **Remarks:** 

Pour les documents provenant du format RTF, cette propriété renvoie l'heure locale de la machine de l'auteur au moment de la création du document.

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
java.util.Date - Date de création du document en UTC.
### getHeadingPairs() {#getHeadingPairs}
```
public Object[] getHeadingPairs()
```


Spécifie les titres du document et leurs noms.

 **Remarks:** 

Chaque paire d'en-têtes occupe deux éléments dans ce tableau.

Le premier élément de la paire est un java.lang.String et spécifie le nom de l'en-tête. Le deuxième élément de la paire est un int et spécifie le nombre de parties du document pour cet en-tête dans la propriété [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String).

La somme totale des comptes pour toutes les paires d'en-têtes dans cette propriété doit être égale au nombre d'éléments dans la propriété [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String).

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre la relation entre les propriétés "HeadingPairs" et "TitlesOfParts".

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
java.lang.Object[] - La valeur java.lang.Object[] correspondante.
### getHyperlinkBase() {#getHyperlinkBase}
```
public String getHyperlinkBase()
```


Spécifie la chaîne de base utilisée pour évaluer les hyperliens relatifs dans ce document.

 **Remarks:** 

Aspose.Words n'utilise pas cette propriété.

 **Examples:** 

Montre comment stocker la partie de base d'un hyperlien dans les propriétés du document.

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
java.lang.String - La valeur java.lang.String correspondante.
### getHyperlinksChanged() {#getHyperlinksChanged}
```
public boolean getHyperlinksChanged()
```


Indique si les hyperliens dans un document ont été modifiés.

 **Remarks:** 

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment obtenir les propriétés étendues.

```

 Document doc = new Document(getMyDir() + "Extended properties.docx");
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getScaleCrop());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getSharedDocument());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getHyperlinksChanged());
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getKeywords() {#getKeywords}
```
public String getKeywords()
```


Obtient les mots-clés du document.

 **Examples:** 

Montre comment travailler avec les propriétés de document intégrées dans la catégorie "Description".

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
java.lang.String - Les mots-clés du document.
### getLastPrinted() {#getLastPrinted}
```
public Date getLastPrinted()
```


Obtient la date à laquelle le document a été imprimé pour la dernière fois en UTC.

 **Remarks:** 

Pour les documents provenant du format RTF, cette propriété renvoie l'heure locale de la dernière opération d'impression.

Si le document n'a jamais été imprimé, cette propriété renverra DateTime.MinValue.

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
java.util.Date - La date à laquelle le document a été imprimé pour la dernière fois en UTC.
### getLastSavedBy() {#getLastSavedBy}
```
public String getLastSavedBy()
```


Obtient le nom du dernier auteur.

 **Remarks:** 

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
java.lang.String - Le nom du dernier auteur.
### getLastSavedTime() {#getLastSavedTime}
```
public Date getLastSavedTime()
```


Obtient l'heure de la dernière sauvegarde en UTC.

 **Remarks:** 

Pour les documents provenant du format RTF, cette propriété renvoie l'heure locale de la dernière opération d'enregistrement.

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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

Montre comment utiliser le champ SAVEDATE pour afficher la date/heure de la dernière opération d'enregistrement du document effectuée avec Microsoft Word.

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
java.util.Date - L'heure du dernier enregistrement en UTC.
### getLines() {#getLines}
```
public int getLines()
```


Représente une estimation du nombre de lignes dans le document.

 **Remarks:** 

Aspose.Words met à jour cette propriété lorsque vous appelez [Document.updateWordCount(boolean)](../../com.aspose.words/document/\#updateWordCount-boolean).

 **Examples:** 

Montre comment mettre à jour toutes les étiquettes de listes dans un document.

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

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
int - La valeur int correspondante.
### getLinksUpToDate() {#getLinksUpToDate}
```
public boolean getLinksUpToDate()
```


Indique si les hyperliens dans un document sont à jour.

 **Remarks:** 

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
boolean - La valeur  boolean  correspondante.
### getManager() {#getManager}
```
public String getManager()
```


Obtient la propriété manager.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
java.lang.String - La propriété manager.
### getNameOfApplication() {#getNameOfApplication}
```
public String getNameOfApplication()
```


Obtient le nom de l'application.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
java.lang.String - Le nom de l'application.
### getPages() {#getPages}
```
public int getPages()
```


Représente une estimation du nombre de pages dans le document.

 **Remarks:** 

Aspose.Words met à jour cette propriété lorsque vous appelez [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
int - La valeur int correspondante.
### getParagraphs() {#getParagraphs}
```
public int getParagraphs()
```


Représente une estimation du nombre de paragraphes dans le document.

 **Remarks:** 

Aspose.Words met à jour cette propriété lorsque vous appelez [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Montre comment mettre à jour toutes les étiquettes de listes dans un document.

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

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
int - La valeur int correspondante.
### getRevisionNumber() {#getRevisionNumber}
```
public int getRevisionNumber()
```


Obtient le numéro de révision du document.

 **Remarks:** 

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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

Montre comment travailler avec les champs REVNUM.

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
int - Le numéro de révision du document.
### getScaleCrop() {#getScaleCrop}
```
public boolean getScaleCrop()
```


Indique si la vignette du document est recadrée ou mise à l'échelle pour s'adapter à l'affichage.

 **Remarks:** 

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment obtenir les propriétés étendues.

```

 Document doc = new Document(getMyDir() + "Extended properties.docx");
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getScaleCrop());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getSharedDocument());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getHyperlinksChanged());
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getSecurity() {#getSecurity}
```
public int getSecurity()
```


Spécifie le niveau de sécurité d'un document sous forme de valeur numérique.

 **Remarks:** 

Utilisez cette propriété à des fins d'information uniquement car Microsoft Word ne définit pas toujours cette propriété. Cette propriété n'est disponible que dans les documents DOC et OOXML.

Pour protéger ou déprotéger un document, utilisez les méthodes **M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** et [Document.unprotect()](../../com.aspose.words/document/\#unprotect).

Aspose.Words met à jour cette propriété avec une valeur correcte avant d'enregistrer un document.

 **Examples:** 

Montre comment utiliser les propriétés du document pour afficher le niveau de sécurité d'un document.

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
int - La valeur int correspondante. La valeur retournée est une combinaison bit à bit des constantes [DocumentSecurity](../../com.aspose.words/documentsecurity/).
### getSharedDocument() {#getSharedDocument}
```
public boolean getSharedDocument()
```


Indique si le document est un document partagé.

 **Remarks:** 

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment obtenir les propriétés étendues.

```

 Document doc = new Document(getMyDir() + "Extended properties.docx");
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getScaleCrop());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getSharedDocument());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getHyperlinksChanged());
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getSubject() {#getSubject}
```
public String getSubject()
```


Obtient le sujet du document.

 **Examples:** 

Montre comment travailler avec les propriétés de document intégrées dans la catégorie "Description".

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
java.lang.String - Le sujet du document.
### getTemplate() {#getTemplate}
```
public String getTemplate()
```


Obtient le nom informatif du modèle de document.

 **Remarks:** 

Dans Microsoft Word, cette propriété est uniquement à des fins d'information et contient généralement seulement le nom de fichier du modèle sans le chemin.

Une chaîne vide signifie que le document est attaché au modèle Normal.

Pour obtenir ou définir le nom réel du modèle attaché, utilisez la propriété [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String).

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
java.lang.String - Le nom informatif du modèle de document.
### getThumbnail() {#getThumbnail}
```
public byte[] getThumbnail()
```


Obtient ou définit la vignette du document.

**Returns:**
byte[] - La valeur byte[] correspondante.
### getTitle() {#getTitle}
```
public String getTitle()
```


Obtient le titre du document.

 **Examples:** 

Montre comment travailler avec les propriétés de document intégrées dans la catégorie "Description".

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
java.lang.String - Le titre du document.
### getTitlesOfParts() {#getTitlesOfParts}
```
public String[] getTitlesOfParts()
```


Chaque chaîne du tableau spécifie le nom d'une partie du document.

 **Remarks:** 

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre la relation entre les propriétés "HeadingPairs" et "TitlesOfParts".

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
java.lang.String[] - La valeur java.lang.String[] correspondante.
### getTotalEditingTime() {#getTotalEditingTime}
```
public int getTotalEditingTime()
```


Obtient le temps total d'édition en minutes.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
int - Le temps total d'édition en minutes.
### getVersion() {#getVersion}
```
public int getVersion()
```


Représente le numéro de version de l'application qui a créé le document.

 **Remarks:** 

Lorsqu'un document a été créé par Microsoft Word, les 16 bits supérieurs représentent la version majeure et les 16 bits inférieurs le numéro de build.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
int - La valeur int correspondante.
### getWords() {#getWords}
```
public int getWords()
```


Représente une estimation du nombre de mots dans le document.

 **Remarks:** 

Aspose.Words met à jour cette propriété lorsque vous appelez [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Montre comment mettre à jour toutes les étiquettes de listes dans un document.

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

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
int - La valeur int correspondante.
### indexOf(String name) {#indexOf-java.lang.String}
```
public int indexOf(String name)
```


Obtient l'indice d'une propriété par son nom.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

 **Examples:** 

Montre comment travailler avec les propriétés personnalisées d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom de la propriété, insensible à la casse. |

**Returns:**
int - L'index basé sur zéro. Valeur négative si non trouvé.
### iterator() {#iterator}
```
public Iterator iterator()
```


Renvoie un objet itérateur qui peut être utilisé pour parcourir tous les éléments de la collection.

 **Examples:** 

Montre comment travailler avec les propriétés personnalisées d'un document.

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


Supprime une propriété portant le nom spécifié de la collection.

 **Examples:** 

Montre comment travailler avec les propriétés personnalisées d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom de la propriété, insensible à la casse. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Supprime une propriété à l'indice spécifié.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

 **Examples:** 

Montre comment travailler avec les propriétés personnalisées d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index basé sur zéro. |

### setAuthor(String value) {#setAuthor-java.lang.String}
```
public void setAuthor(String value)
```


Définit le nom de l'auteur du document.

 **Examples:** 

Montre comment travailler avec les propriétés de document intégrées dans la catégorie "Description".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le nom de l'auteur du document. |

### setBytes(int value) {#setBytes-int}
```
public void setBytes(int value)
```


Représente une estimation du nombre d'octets dans le document.

 **Remarks:** 

Microsoft Word ne définit pas toujours cette propriété.

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La valeur  int  correspondante. |

### setCategory(String value) {#setCategory-java.lang.String}
```
public void setCategory(String value)
```


Définit la catégorie du document.

 **Examples:** 

Montre comment travailler avec les propriétés de document intégrées dans la catégorie "Description".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La catégorie du document. |

### setCharacters(int value) {#setCharacters-int}
```
public void setCharacters(int value)
```


Représente une estimation du nombre de caractères dans le document.

 **Remarks:** 

Aspose.Words met à jour cette propriété lorsque vous appelez [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Montre comment mettre à jour toutes les étiquettes de listes dans un document.

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

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La valeur  int  correspondante. |

### setCharactersWithSpaces(int value) {#setCharactersWithSpaces-int}
```
public void setCharactersWithSpaces(int value)
```


Représente une estimation du nombre de caractères (espaces inclus) dans le document.

 **Remarks:** 

Aspose.Words met à jour cette propriété lorsque vous appelez [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La valeur  int  correspondante. |

### setComments(String value) {#setComments-java.lang.String}
```
public void setComments(String value)
```


Définit les commentaires du document.

 **Examples:** 

Montre comment travailler avec les propriétés de document intégrées dans la catégorie "Description".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Les commentaires du document. |

### setCompany(String value) {#setCompany-java.lang.String}
```
public void setCompany(String value)
```


Définit la propriété de l'entreprise.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La propriété de l'entreprise. |

### setContentStatus(String value) {#setContentStatus-java.lang.String}
```
public void setContentStatus(String value)
```


Définit le statut du contenu du document.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | L'état du contenu du document. |

### setContentType(String value) {#setContentType-java.lang.String}
```
public void setContentType(String value)
```


Définit le type de contenu du document.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le type de contenu du document. |

### setCreatedTime(Date value) {#setCreatedTime-java.util.Date}
```
public void setCreatedTime(Date value)
```


Définit la date de création du document en UTC.

 **Remarks:** 

Pour les documents provenant du format RTF, cette propriété renvoie l'heure locale de la machine de l'auteur au moment de la création du document.

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.util.Date | Date de création du document en UTC. |

### setHeadingPairs(Object[] value) {#setHeadingPairs-java.lang.Object}
```
public void setHeadingPairs(Object[] value)
```


Spécifie les titres du document et leurs noms.

 **Remarks:** 

Chaque paire d'en-têtes occupe deux éléments dans ce tableau.

Le premier élément de la paire est un java.lang.String et spécifie le nom de l'en-tête. Le deuxième élément de la paire est un int et spécifie le nombre de parties du document pour cet en-tête dans la propriété [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String).

La somme totale des comptes pour toutes les paires d'en-têtes dans cette propriété doit être égale au nombre d'éléments dans la propriété [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String).

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre la relation entre les propriétés "HeadingPairs" et "TitlesOfParts".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.Object[] | La valeur java.lang.Object[] correspondante. |

### setHyperlinkBase(String value) {#setHyperlinkBase-java.lang.String}
```
public void setHyperlinkBase(String value)
```


Spécifie la chaîne de base utilisée pour évaluer les hyperliens relatifs dans ce document.

 **Remarks:** 

Aspose.Words n'utilise pas cette propriété.

 **Examples:** 

Montre comment stocker la partie de base d'un hyperlien dans les propriétés du document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setKeywords(String value) {#setKeywords-java.lang.String}
```
public void setKeywords(String value)
```


Définit les mots-clés du document.

 **Examples:** 

Montre comment travailler avec les propriétés de document intégrées dans la catégorie "Description".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Les mots-clés du document. |

### setLastPrinted(Date value) {#setLastPrinted-java.util.Date}
```
public void setLastPrinted(Date value)
```


Définit la date à laquelle le document a été imprimé pour la dernière fois en UTC.

 **Remarks:** 

Pour les documents provenant du format RTF, cette propriété renvoie l'heure locale de la dernière opération d'impression.

Si le document n'a jamais été imprimé, cette propriété renverra DateTime.MinValue.

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.util.Date | La date à laquelle le document a été imprimé pour la dernière fois en UTC. |

### setLastSavedBy(String value) {#setLastSavedBy-java.lang.String}
```
public void setLastSavedBy(String value)
```


Définit le nom du dernier auteur.

 **Remarks:** 

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le nom du dernier auteur. |

### setLastSavedTime(Date value) {#setLastSavedTime-java.util.Date}
```
public void setLastSavedTime(Date value)
```


Définit l'heure de la dernière sauvegarde en UTC.

 **Remarks:** 

Pour les documents provenant du format RTF, cette propriété renvoie l'heure locale de la dernière opération d'enregistrement.

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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

Montre comment utiliser le champ SAVEDATE pour afficher la date/heure de la dernière opération d'enregistrement du document effectuée avec Microsoft Word.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.util.Date | L'heure de la dernière sauvegarde en UTC. |

### setLines(int value) {#setLines-int}
```
public void setLines(int value)
```


Représente une estimation du nombre de lignes dans le document.

 **Remarks:** 

Aspose.Words met à jour cette propriété lorsque vous appelez [Document.updateWordCount(boolean)](../../com.aspose.words/document/\#updateWordCount-boolean).

 **Examples:** 

Montre comment mettre à jour toutes les étiquettes de listes dans un document.

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

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La valeur  int  correspondante. |

### setLinksUpToDate(boolean value) {#setLinksUpToDate-boolean}
```
public void setLinksUpToDate(boolean value)
```


Indique si les hyperliens dans un document sont à jour.

 **Remarks:** 

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setManager(String value) {#setManager-java.lang.String}
```
public void setManager(String value)
```


Définit la propriété du responsable.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La propriété du gestionnaire. |

### setNameOfApplication(String value) {#setNameOfApplication-java.lang.String}
```
public void setNameOfApplication(String value)
```


Définit le nom de l'application.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le nom de l'application. |

### setPages(int value) {#setPages-int}
```
public void setPages(int value)
```


Représente une estimation du nombre de pages dans le document.

 **Remarks:** 

Aspose.Words met à jour cette propriété lorsque vous appelez [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La valeur  int  correspondante. |

### setParagraphs(int value) {#setParagraphs-int}
```
public void setParagraphs(int value)
```


Représente une estimation du nombre de paragraphes dans le document.

 **Remarks:** 

Aspose.Words met à jour cette propriété lorsque vous appelez [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Montre comment mettre à jour toutes les étiquettes de listes dans un document.

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

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La valeur  int  correspondante. |

### setRevisionNumber(int value) {#setRevisionNumber-int}
```
public void setRevisionNumber(int value)
```


Définit le numéro de révision du document.

 **Remarks:** 

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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

Montre comment travailler avec les champs REVNUM.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le numéro de révision du document. |

### setSecurity(int value) {#setSecurity-int}
```
public void setSecurity(int value)
```


Spécifie le niveau de sécurité d'un document sous forme de valeur numérique.

 **Remarks:** 

Utilisez cette propriété à des fins d'information uniquement car Microsoft Word ne définit pas toujours cette propriété. Cette propriété n'est disponible que dans les documents DOC et OOXML.

Pour protéger ou déprotéger un document, utilisez les méthodes **M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** et [Document.unprotect()](../../com.aspose.words/document/\#unprotect).

Aspose.Words met à jour cette propriété avec une valeur correcte avant d'enregistrer un document.

 **Examples:** 

Montre comment utiliser les propriétés du document pour afficher le niveau de sécurité d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur int correspondante. La valeur doit être une combinaison binaire des constantes [DocumentSecurity](../../com.aspose.words/documentsecurity/). |

### setSubject(String value) {#setSubject-java.lang.String}
```
public void setSubject(String value)
```


Définit le sujet du document.

 **Examples:** 

Montre comment travailler avec les propriétés de document intégrées dans la catégorie "Description".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le sujet du document. |

### setTemplate(String value) {#setTemplate-java.lang.String}
```
public void setTemplate(String value)
```


Définit le nom informatif du modèle de document.

 **Remarks:** 

Dans Microsoft Word, cette propriété est uniquement à des fins d'information et contient généralement seulement le nom de fichier du modèle sans le chemin.

Une chaîne vide signifie que le document est attaché au modèle Normal.

Pour obtenir ou définir le nom réel du modèle attaché, utilisez la propriété [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String).

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le nom informatif du modèle de document. |

### setThumbnail(byte[] value) {#setThumbnail-byte}
```
public void setThumbnail(byte[] value)
```


Obtient ou définit la vignette du document.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | byte[] | La valeur byte[] correspondante. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


Définit le titre du document.

 **Examples:** 

Montre comment travailler avec les propriétés de document intégrées dans la catégorie "Description".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le titre du document. |

### setTitlesOfParts(String[] value) {#setTitlesOfParts-java.lang.String}
```
public void setTitlesOfParts(String[] value)
```


Chaque chaîne du tableau spécifie le nom d'une partie du document.

 **Remarks:** 

Aspose.Words ne met pas à jour cette propriété.

 **Examples:** 

Montre la relation entre les propriétés "HeadingPairs" et "TitlesOfParts".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String[] | La valeur java.lang.String[] correspondante. |

### setTotalEditingTime(int value) {#setTotalEditingTime-int}
```
public void setTotalEditingTime(int value)
```


Définit le temps total d'édition en minutes.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le temps total d'édition en minutes. |

### setVersion(int value) {#setVersion-int}
```
public void setVersion(int value)
```


Représente le numéro de version de l'application qui a créé le document.

 **Remarks:** 

Lorsqu'un document a été créé par Microsoft Word, les 16 bits supérieurs représentent la version majeure et les 16 bits inférieurs le numéro de build.

 **Examples:** 

Montre comment travailler avec les propriétés du document dans la catégorie "Origin".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La valeur  int  correspondante. |

### setWords(int value) {#setWords-int}
```
public void setWords(int value)
```


Représente une estimation du nombre de mots dans le document.

 **Remarks:** 

Aspose.Words met à jour cette propriété lorsque vous appelez [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Montre comment mettre à jour toutes les étiquettes de listes dans un document.

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

Montre comment travailler avec les propriétés du document dans la catégorie "Content".

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La valeur  int  correspondante. |

