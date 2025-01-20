---
title: NodeChangingAction
linktitle: NodeChangingAction
second_title: Aspose.Words for Java
description: Specifies the type of node change in Java.
type: docs
weight: 462
url: /java/com.aspose.words/nodechangingaction/
---

**Inheritance:**
java.lang.Object
```
public class NodeChangingAction
```

Specifies the type of node change.

 **Examples:** 

Shows how to use a NodeChangingCallback to monitor changes to the document tree in real-time as we edit it.

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
## Fields

| Field | Description |
| --- | --- |
| [INSERT](#INSERT) | A node is being inserted in the tree. |
| [REMOVE](#REMOVE) | A node is being removed from the tree. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String nodeChangingActionName)](#fromName-java.lang.String) |  |
| [getName(int nodeChangingAction)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int nodeChangingAction)](#toString-int) |  |
### INSERT {#INSERT}
```
public static int INSERT
```


A node is being inserted in the tree.

### REMOVE {#REMOVE}
```
public static int REMOVE
```


A node is being removed from the tree.

### length {#length}
```
public static int length
```


### fromName(String nodeChangingActionName) {#fromName-java.lang.String}
```
public static int fromName(String nodeChangingActionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeChangingActionName | java.lang.String |  |

**Returns:**
int
### getName(int nodeChangingAction) {#getName-int}
```
public static String getName(int nodeChangingAction)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| nodeChangingAction | int |  |

**Returns:**
java.lang.String
