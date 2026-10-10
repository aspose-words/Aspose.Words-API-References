---
title: "NodeChangingAction"
linktitle: "NodeChangingAction"
second_title: "Aspose.Words Java için"
description: "Java'da düğüm değişikliğinin türünü belirtir."
type: docs
weight: 477
url: /tr/java/com.aspose.words/nodechangingaction/
---

**Inheritance:**
java.lang.Object
```
public class NodeChangingAction
```

Düğüm değişikliğinin türünü belirtir.

 **Examples:** 

NodeChangingCallback'i kullanarak belge ağacındaki değişiklikleri gerçek zamanlı olarak izlemeyi, düzenlerken nasıl yapacağımızı gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [INSERT](#INSERT) | Ağaca bir düğüm ekleniyor. |
| [REMOVE](#REMOVE) | Ağacın bir düğümü kaldırılıyor. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String nodeChangingActionName)](#fromName-java.lang.String) |  |
| [getName(int nodeChangingAction)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int nodeChangingAction)](#toString-int) |  |
### INSERT {#INSERT}
```
public static int INSERT
```


Ağaca bir düğüm ekleniyor.

### REMOVE {#REMOVE}
```
public static int REMOVE
```


Ağacın bir düğümü kaldırılıyor.

### length {#length}
```
public static int length
```


### fromName(String nodeChangingActionName) {#fromName-java.lang.String}
```
public static int fromName(String nodeChangingActionName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| nodeChangingActionName | java.lang.String |  |

**Returns:**
int
### getName(int nodeChangingAction) {#getName-int}
```
public static String getName(int nodeChangingAction)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| nodeChangingAction | int |  |

**Returns:**
java.lang.String
