---
title: VisitorAction
linktitle: VisitorAction
second_title: Aspose.Words for Java
description: Allows the visitor to control the enumeration of nodes in Java.
type: docs
weight: 711
url: /java/com.aspose.words/visitoraction/
---

**Inheritance:**
java.lang.Object
```
public class VisitorAction
```

Allows the visitor to control the enumeration of nodes.

 **Examples:** 

Shows how to process absolute position tab characters with a document visitor.

```

 public void documentToTxt() throws Exception {
     Document doc = new Document(getMyDir() + "Absolute position tab.docx");

     // Extract the text contents of our document by accepting this custom document visitor.
     DocTextExtractor myDocTextExtractor = new DocTextExtractor();
     Section fisrtSection = doc.getFirstSection();
     fisrtSection.getBody().accept(myDocTextExtractor);
     // Visit only start of the document body.
     fisrtSection.getBody().acceptStart(myDocTextExtractor);
     // Visit only end of the document body.
     fisrtSection.getBody().acceptEnd(myDocTextExtractor);

     // The absolute position tab, which has no equivalent in string form, has been explicitly converted to a tab character.
     Assert.assertEquals("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.getText());

     // An AbsolutePositionTab can accept a DocumentVisitor by itself too.
     AbsolutePositionTab absPositionTab = (AbsolutePositionTab) doc.getFirstSection().getBody().getFirstParagraph().getChild(NodeType.SPECIAL_CHAR, 0, true);

     myDocTextExtractor = new DocTextExtractor();
     absPositionTab.accept(myDocTextExtractor);

     Assert.assertEquals("\t", myDocTextExtractor.getText());
 }

 /// 
 /// Collects the text contents of all runs in the visited document. Replaces all absolute tab characters with ordinary tabs.
 /// 
 public static class DocTextExtractor extends DocumentVisitor {
     public DocTextExtractor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         appendText(run.getText());
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when an AbsolutePositionTab node is encountered in the document.
     /// 
     public int visitAbsolutePositionTab(final AbsolutePositionTab tab) {
         mBuilder.append("\t");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds text to the current output. Honors the enabled/disabled output flag.
     /// 
     public void appendText(final String text) {
         mBuilder.append(text);
     }

     /// 
     /// Plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```
## Fields

| Field | Description |
| --- | --- |
| [CONTINUE](#CONTINUE) | The visitor requests the enumeration to continue. |
| [SKIP_THIS_NODE](#SKIP-THIS-NODE) | The visitor requests to skip the current node and continue enumeration. |
| [STOP](#STOP) | The visitor requests the enumeration of nodes to stop. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String visitorActionName)](#fromName-java.lang.String) |  |
| [getName(int visitorAction)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int visitorAction)](#toString-int) |  |
### CONTINUE {#CONTINUE}
```
public static int CONTINUE
```


The visitor requests the enumeration to continue.

### SKIP_THIS_NODE {#SKIP-THIS-NODE}
```
public static int SKIP_THIS_NODE
```


The visitor requests to skip the current node and continue enumeration.

### STOP {#STOP}
```
public static int STOP
```


The visitor requests the enumeration of nodes to stop.

### length {#length}
```
public static int length
```


### fromName(String visitorActionName) {#fromName-java.lang.String}
```
public static int fromName(String visitorActionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitorActionName | java.lang.String |  |

**Returns:**
int
### getName(int visitorAction) {#getName-int}
```
public static String getName(int visitorAction)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitorAction | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int visitorAction) {#toString-int}
```
public static String toString(int visitorAction)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitorAction | int |  |

**Returns:**
java.lang.String
