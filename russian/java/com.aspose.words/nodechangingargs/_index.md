---
title: "NodeChangingArgs"
linktitle: "NodeChangingArgs"
second_title: "Aspose.Words для Java"
description: "Предоставляет данные для методов интерфейса INodeChangingCallback в Java."
type: docs
weight: 478
url: /ru/java/com.aspose.words/nodechangingargs/
---

**Inheritance:**
java.lang.Object
```
public class NodeChangingArgs
```

Предоставляет данные для методов интерфейса [INodeChangingCallback](../../com.aspose.words/inodechangingcallback/).

Чтобы узнать больше, посетите статью документации [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_].

 **Examples:** 

Показывает, как настроить изменение узлов с помощью обратного вызова.

```

 public void fontChangeViaCallback() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Set the node changing callback to custom implementation,
     // then add/remove nodes to get it to generate a log.
     HandleNodeChangingFontChanger callback = new HandleNodeChangingFontChanger();
     doc.setNodeChangingCallback(callback);

     builder.writeln("Hello world!");
     builder.writeln("Hello again!");
     builder.insertField(" HYPERLINK \"https://www.google.com/\" ");
     builder.insertShape(ShapeType.RECTANGLE, 300.0, 300.0);

     doc.getRange().getFields().get(0).remove();

     System.out.println(callback.getLog());
 }

 /// 
 /// Logs the date and time of each node insertion and removal.
 /// Sets a custom font name/size for the text contents of Run nodes.
 /// 
 public static class HandleNodeChangingFontChanger implements INodeChangingCallback {
     public void nodeInserted(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\tType:\t{0}", args.getNode().getNodeType()));
         mLog.append(MessageFormat.format("\tHash:\t{0}", args.getNode().hashCode()));

         if (args.getNode().getNodeType() == NodeType.RUN) {
             Font font = ((Run) args.getNode()).getFont();
             mLog.append(MessageFormat.format("\tFont:\tChanged from \"{0}\" {1}pt", font.getName(), font.getSize()));

             font.setSize(24.0);
             font.setName("Arial");

             mLog.append(MessageFormat.format(" to \"{0}\" {1}pt", font.getName(), font.getSize()));
             mLog.append(MessageFormat.format("\tContents:\n\t\t\"{0}\"", args.getNode().getText()));
         }
     }

     public void nodeInserting(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\n{0}\tNode insertion:", new Date()));
     }

     public void nodeRemoved(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\tType:\t{0}", args.getNode().getNodeType()));
         mLog.append(MessageFormat.format("\tHash code:\t{0}", args.getNode().hashCode()));
     }

     public void nodeRemoving(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\n{0}\tNode removal:", new Date()));
     }

     public String getLog() {
         return mLog.toString();
     }

     private final StringBuilder mLog = new StringBuilder();
 }
 
```


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Методы

| Метод | Описание |
| --- | --- |
| [getAction()](#getAction) | Получает значение, указывающее, какой тип события изменения узла происходит. |
| [getNewParent()](#getNewParent) | Получает родительский узел, который будет установлен после завершения операции. |
| [getNode()](#getNode) | Получает [getNode()](../../com.aspose.words/nodechangingargs/\\#getNode), который добавляется или удаляется. |
| [getOldParent()](#getOldParent) | Получает родительский узел до начала операции. |
### getAction() {#getAction}
```
public int getAction()
```


Получает значение, указывающее, какой тип события изменения узла происходит.

 **Examples:** 

Показывает, как использовать NodeChangingCallback для мониторинга изменений дерева документа в реальном времени во время редактирования.

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

**Returns:**
int - Значение, указывающее, какой тип события изменения узла происходит. Возвращаемое значение является одной из констант [NodeChangingAction](../../com.aspose.words/nodechangingaction/).
### getNewParent() {#getNewParent}
```
public Node getNewParent()
```


Получает родительский узел, который будет установлен после завершения операции.

 **Examples:** 

Показывает, как использовать NodeChangingCallback для мониторинга изменений дерева документа в реальном времени во время редактирования.

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

**Returns:**
[Node](../../com.aspose.words/node/) - The node's parent that will be set after the operation completes.
### getNode() {#getNode}
```
public Node getNode()
```


Получает [getNode()](../../com.aspose.words/nodechangingargs/\\#getNode), который добавляется или удаляется.

 **Examples:** 

Показывает, как настроить изменение узлов с помощью обратного вызова.

```

 public void fontChangeViaCallback() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Set the node changing callback to custom implementation,
     // then add/remove nodes to get it to generate a log.
     HandleNodeChangingFontChanger callback = new HandleNodeChangingFontChanger();
     doc.setNodeChangingCallback(callback);

     builder.writeln("Hello world!");
     builder.writeln("Hello again!");
     builder.insertField(" HYPERLINK \"https://www.google.com/\" ");
     builder.insertShape(ShapeType.RECTANGLE, 300.0, 300.0);

     doc.getRange().getFields().get(0).remove();

     System.out.println(callback.getLog());
 }

 /// 
 /// Logs the date and time of each node insertion and removal.
 /// Sets a custom font name/size for the text contents of Run nodes.
 /// 
 public static class HandleNodeChangingFontChanger implements INodeChangingCallback {
     public void nodeInserted(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\tType:\t{0}", args.getNode().getNodeType()));
         mLog.append(MessageFormat.format("\tHash:\t{0}", args.getNode().hashCode()));

         if (args.getNode().getNodeType() == NodeType.RUN) {
             Font font = ((Run) args.getNode()).getFont();
             mLog.append(MessageFormat.format("\tFont:\tChanged from \"{0}\" {1}pt", font.getName(), font.getSize()));

             font.setSize(24.0);
             font.setName("Arial");

             mLog.append(MessageFormat.format(" to \"{0}\" {1}pt", font.getName(), font.getSize()));
             mLog.append(MessageFormat.format("\tContents:\n\t\t\"{0}\"", args.getNode().getText()));
         }
     }

     public void nodeInserting(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\n{0}\tNode insertion:", new Date()));
     }

     public void nodeRemoved(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\tType:\t{0}", args.getNode().getNodeType()));
         mLog.append(MessageFormat.format("\tHash code:\t{0}", args.getNode().hashCode()));
     }

     public void nodeRemoving(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\n{0}\tNode removal:", new Date()));
     }

     public String getLog() {
         return mLog.toString();
     }

     private final StringBuilder mLog = new StringBuilder();
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The [getNode()](../../com.aspose.words/nodechangingargs/\#getNode) that is being added or removed.
### getOldParent() {#getOldParent}
```
public Node getOldParent()
```


Получает родительский узел до начала операции.

 **Examples:** 

Показывает, как использовать NodeChangingCallback для мониторинга изменений дерева документа в реальном времени во время редактирования.

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

**Returns:**
[Node](../../com.aspose.words/node/) - The node's parent before the operation began.
