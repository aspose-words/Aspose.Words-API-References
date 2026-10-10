---
title: "ReplaceAction"
linktitle: "ReplaceAction"
second_title: "Aspose.Words لـ Java"
description: "يسمح للمستخدم بتحديد ما يحدث للمطابقة الحالية أثناء عملية الاستبدال في Java."
type: docs
weight: 565
url: /ar/java/com.aspose.words/replaceaction/
---

**Inheritance:**
java.lang.Object
```
public class ReplaceAction
```

يسمح للمستخدم بتحديد ما يحدث للمطابقة الحالية أثناء عملية الاستبدال.

 **Examples:** 

يعرض كيفية إدراج محتويات مستند كامل كبديل لمطابقة في عملية البحث والاستبدال.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [REPLACE](#REPLACE) | استبدال المطابقة الحالية. |
| [SKIP](#SKIP) | تخطي المطابقة الحالية. |
| [STOP](#STOP) | إنهاء عملية الاستبدال. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String replaceActionName)](#fromName-java.lang.String) |  |
| [getName(int replaceAction)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int replaceAction)](#toString-int) |  |
### REPLACE {#REPLACE}
```
public static int REPLACE
```


استبدال المطابقة الحالية.

### SKIP {#SKIP}
```
public static int SKIP
```


تخطي المطابقة الحالية.

### STOP {#STOP}
```
public static int STOP
```


إنهاء عملية الاستبدال.

### length {#length}
```
public static int length
```


### fromName(String replaceActionName) {#fromName-java.lang.String}
```
public static int fromName(String replaceActionName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| replaceActionName | java.lang.String |  |

**Returns:**
int
### getName(int replaceAction) {#getName-int}
```
public static String getName(int replaceAction)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| replaceAction | int |  |

**Returns:**
java.lang.String
