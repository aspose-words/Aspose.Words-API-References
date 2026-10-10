---
title: "ReplaceAction"
linktitle: "ReplaceAction"
second_title: "Aspose.Words per Java"
description: "Consente all'utente di specificare cosa succede alla corrispondenza corrente durante un'operazione di sostituzione in Java."
type: docs
weight: 565
url: /it/java/com.aspose.words/replaceaction/
---

**Inheritance:**
java.lang.Object
```
public class ReplaceAction
```

Consente all'utente di specificare cosa accade alla corrispondenza corrente durante un'operazione di sostituzione.

 **Examples:** 

Mostra come inserire il contenuto di un intero documento come sostituzione di una corrispondenza in un'operazione di trova e sostituisci.

```

 public void insertDocumentAtReplace() throws Exception {
     Document mainDoc = new Document(getMyDir() + "Document insertion destination.docx");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();
     options.setReplacingCallback(new InsertDocumentAtReplaceHandler());

     mainDoc.getRange().replace(Pattern.compile("\[MY_DOCUMENT\]"), "", options);
     mainDoc.save(getArtifactsDir() + "InsertDocument.InsertDocumentAtReplace.docx");

 }

 private static class InsertDocumentAtReplaceHandler implements IReplacingCallback {
     public int replacing(ReplacingArgs args) throws Exception {
         Document subDoc = new Document(getMyDir() + "Document.docx");

         // Insert a document after the paragraph containing the matched text.
         Paragraph para = (Paragraph) args.getMatchNode().getParentNode();
         insertDocument(para, subDoc);

         // Remove the paragraph with the matched text.
         para.remove();

         return ReplaceAction.SKIP;
     }
 }

 /// 
 /// Inserts all the nodes of another document after a paragraph or table.
 /// 
 private static void insertDocument(Node insertionDestination, Document docToInsert) {
     if (((insertionDestination.getNodeType()) == (NodeType.PARAGRAPH)) || ((insertionDestination.getNodeType()) == (NodeType.TABLE))) {
         CompositeNode dstStory = insertionDestination.getParentNode();

         NodeImporter importer =
                 new NodeImporter(docToInsert, insertionDestination.getDocument(), ImportFormatMode.KEEP_SOURCE_FORMATTING);

         for (Section srcSection : docToInsert.getSections())
             for (Node srcNode : srcSection.getBody()) {
                 // Skip the node if it is the last empty paragraph in a section.
                 if (((srcNode.getNodeType()) == (NodeType.PARAGRAPH))) {
                     Paragraph para = (Paragraph) srcNode;
                     if (para.isEndOfSection() && !para.hasChildNodes())
                         continue;
                 }

                 Node newNode = importer.importNode(srcNode, true);

                 dstStory.insertAfter(newNode, insertionDestination);
                 insertionDestination = newNode;
             }
     } else {
         throw new IllegalArgumentException("The destination node must be either a paragraph or table.");
     }
 }
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [REPLACE](#REPLACE) | Sostituisci la corrispondenza corrente. |
| [SKIP](#SKIP) | Salta la corrispondenza corrente. |
| [STOP](#STOP) | Termina l'operazione di sostituzione. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String replaceActionName)](#fromName-java.lang.String) |  |
| [getName(int replaceAction)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int replaceAction)](#toString-int) |  |
### REPLACE {#REPLACE}
```
public static int REPLACE
```


Sostituisci la corrispondenza corrente.

### SKIP {#SKIP}
```
public static int SKIP
```


Salta la corrispondenza corrente.

### STOP {#STOP}
```
public static int STOP
```


Termina l'operazione di sostituzione.

### length {#length}
```
public static int length
```


### fromName(String replaceActionName) {#fromName-java.lang.String}
```
public static int fromName(String replaceActionName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| replaceActionName | java.lang.String |  |

**Returns:**
int
### getName(int replaceAction) {#getName-int}
```
public static String getName(int replaceAction)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| replaceAction | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int replaceAction) {#toString-int}
```
public static String toString(int replaceAction)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| replaceAction | int |  |

**Returns:**
java.lang.String
