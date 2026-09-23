---
title: "NodeChangingAction"
linktitle: "NodeChangingAction"
second_title: "Aspose.Words für Java"
description: "Gibt den Typ der Knotenänderung in Java an."
type: docs
weight: 477
url: /de/java/com.aspose.words/nodechangingaction/
---

**Inheritance:**
java.lang.Object
```
public class NodeChangingAction
```

Gibt den Typ der Knotenänderung an.

 **Examples:** 

Zeigt, wie man einen NodeChangingCallback verwendet, um Änderungen am Dokumentbaum in Echtzeit zu überwachen, während wir ihn bearbeiten.

```

 public void nodeChangingCallback() throws Exception {
     Document doc = new Document();
     doc.setNodeChangingCallback(new NodeChangingPrinter());

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.writeln("Hello world!");
     builder.startTable();
     builder.insertCell();
     builder.write("Cell 1");
     builder.insertCell();
     builder.write("Cell 2");
     builder.endTable();

     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.getCurrentParagraph().getParentNode().removeAllChildren();
 }

 /// 
 /// Prints every node insertion/removal as it takes place in the document.
 /// 
 private static class NodeChangingPrinter implements INodeChangingCallback {
     public void nodeInserting(NodeChangingArgs args) {
         Assert.assertEquals(args.getAction(), NodeChangingAction.INSERT);
         Assert.assertEquals(args.getOldParent(), null);
     }

     public void nodeInserted(NodeChangingArgs args) {
         Assert.assertEquals(args.getAction(), NodeChangingAction.INSERT);
         Assert.assertNotNull(args.getNewParent());

         System.out.println("Inserted node:");
         System.out.println(MessageFormat.format("\tType:\t{0}", args.getNode().getNodeType()));

         if (!"".equals(args.getNode().getText().trim())) {
             System.out.println(MessageFormat.format("\tText:\t\"{0}\"", args.getNode().getText().trim()));
         }

         System.out.println(MessageFormat.format("\tHash:\t{0}", args.getNode().hashCode()));
         System.out.println(MessageFormat.format("\tParent:\t{0} ({1})", args.getNewParent().getNodeType(), args.getNewParent().hashCode()));
     }

     public void nodeRemoving(NodeChangingArgs args) {
         Assert.assertEquals(args.getAction(), NodeChangingAction.REMOVE);
     }

     public void nodeRemoved(NodeChangingArgs args) {
         Assert.assertEquals(args.getAction(), NodeChangingAction.REMOVE);
         Assert.assertNull(args.getNewParent());

         System.out.println(MessageFormat.format("Removed node: {0} ({1})", args.getNode().getNodeType(), args.getNode().hashCode()));
     }
 }
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [INSERT](#INSERT) | Ein Knoten wird in den Baum eingefügt. |
| [REMOVE](#REMOVE) | Ein Knoten wird aus dem Baum entfernt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String nodeChangingActionName)](#fromName-java.lang.String) |  |
| [getName(int nodeChangingAction)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int nodeChangingAction)](#toString-int) |  |
### INSERT {#INSERT}
```
public static int INSERT
```


Ein Knoten wird in den Baum eingefügt.

### REMOVE {#REMOVE}
```
public static int REMOVE
```


Ein Knoten wird aus dem Baum entfernt.

### length {#length}
```
public static int length
```


### fromName(String nodeChangingActionName) {#fromName-java.lang.String}
```
public static int fromName(String nodeChangingActionName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeChangingActionName | java.lang.String |  |

**Returns:**
int
### getName(int nodeChangingAction) {#getName-int}
```
public static String getName(int nodeChangingAction)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeChangingAction | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int nodeChangingAction) {#toString-int}
```
public static String toString(int nodeChangingAction)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeChangingAction | int |  |

**Returns:**
java.lang.String
