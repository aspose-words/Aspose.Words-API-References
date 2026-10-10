---
title: "VisitorAction"
linktitle: "VisitorAction"
second_title: "Aspose.Words Java için"
description: "Ziyaretçinin Java'da düğüm sayımını kontrol etmesine izin verir."
type: docs
weight: 716
url: /tr/java/com.aspose.words/visitoraction/
---

**Inheritance:**
java.lang.Object
```
public class VisitorAction
```

Ziyaretçinin düğümlerin yinelemesini kontrol etmesine izin verir.

 **Examples:** 

Bir belge ziyaretçisiyle mutlak konum sek karakterlerini nasıl işleneceğini gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CONTINUE](#CONTINUE) | Ziyaretçi sayımın devam etmesini ister. |
| [SKIP_THIS_NODE](#SKIP-THIS-NODE) | Ziyaretçi mevcut düğümü atlamasını ve sayımın devam etmesini ister. |
| [STOP](#STOP) | Ziyaretçi düğüm sayımının durmasını ister |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String visitorActionName)](#fromName-java.lang.String) |  |
| [getName(int visitorAction)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int visitorAction)](#toString-int) |  |
### CONTINUE {#CONTINUE}
```
public static int CONTINUE
```


Ziyaretçi sayımın devam etmesini ister.

### SKIP_THIS_NODE {#SKIP-THIS-NODE}
```
public static int SKIP_THIS_NODE
```


Ziyaretçi mevcut düğümü atlamasını ve sayımın devam etmesini ister.

### STOP {#STOP}
```
public static int STOP
```


Ziyaretçi düğüm sayımının durmasını ister

### length {#length}
```
public static int length
```


### fromName(String visitorActionName) {#fromName-java.lang.String}
```
public static int fromName(String visitorActionName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| visitorActionName | java.lang.String |  |

**Returns:**
int
### getName(int visitorAction) {#getName-int}
```
public static String getName(int visitorAction)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| visitorAction | int |  |

**Returns:**
java.lang.String
