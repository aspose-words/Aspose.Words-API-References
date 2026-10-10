---
title: "INodeChangingCallback"
linktitle: "INodeChangingCallback"
second_title: "Aspose.Words für Java"
description: "Implementieren Sie dieses Interface, wenn Sie Benachrichtigungen erhalten möchten, wenn Knoten im Dokument in Java eingefügt oder entfernt werden."
type: docs
weight: 778
url: /de/java/com.aspose.words/inodechangingcallback/
---
```
public interface INodeChangingCallback
```

Implementieren Sie dieses Interface, wenn Sie Benachrichtigungen erhalten möchten, wenn Knoten im Dokument eingefügt oder entfernt werden.

 **Examples:** 

Zeigt, wie man das Ändern von Knoten mit einem Callback anpasst.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [nodeInserted(NodeChangingArgs args)](#nodeInserted-com.aspose.words.NodeChangingArgs) | Wird aufgerufen, wenn ein zu diesem Dokument gehörender Knoten in einen anderen Knoten eingefügt wurde. |
| [nodeInserting(NodeChangingArgs args)](#nodeInserting-com.aspose.words.NodeChangingArgs) | Wird kurz bevor ein zu diesem Dokument gehörender Knoten in einen anderen Knoten eingefügt werden soll, aufgerufen. |
| [nodeRemoved(NodeChangingArgs args)](#nodeRemoved-com.aspose.words.NodeChangingArgs) | Wird aufgerufen, wenn ein zu diesem Dokument gehörender Knoten von seinem übergeordneten Element entfernt wurde. |
| [nodeRemoving(NodeChangingArgs args)](#nodeRemoving-com.aspose.words.NodeChangingArgs) | Wird kurz bevor ein zu diesem Dokument gehörender Knoten aus dem Dokument entfernt werden soll, aufgerufen. |
### nodeInserted(NodeChangingArgs args) {#nodeInserted-com.aspose.words.NodeChangingArgs}
```
public abstract void nodeInserted(NodeChangingArgs args)
```


Wird aufgerufen, wenn ein zu diesem Dokument gehörender Knoten in einen anderen Knoten eingefügt wurde.

 **Examples:** 

Zeigt, wie man das Ändern von Knoten mit einem Callback anpasst.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs/) |  |

### nodeInserting(NodeChangingArgs args) {#nodeInserting-com.aspose.words.NodeChangingArgs}
```
public abstract void nodeInserting(NodeChangingArgs args)
```


Wird kurz bevor ein zu diesem Dokument gehörender Knoten in einen anderen Knoten eingefügt werden soll, aufgerufen.

 **Examples:** 

Zeigt, wie man das Ändern von Knoten mit einem Callback anpasst.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs/) |  |

### nodeRemoved(NodeChangingArgs args) {#nodeRemoved-com.aspose.words.NodeChangingArgs}
```
public abstract void nodeRemoved(NodeChangingArgs args)
```


Wird aufgerufen, wenn ein zu diesem Dokument gehörender Knoten von seinem übergeordneten Element entfernt wurde.

 **Examples:** 

Zeigt, wie man das Ändern von Knoten mit einem Callback anpasst.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs/) |  |

### nodeRemoving(NodeChangingArgs args) {#nodeRemoving-com.aspose.words.NodeChangingArgs}
```
public abstract void nodeRemoving(NodeChangingArgs args)
```


Wird kurz bevor ein zu diesem Dokument gehörender Knoten aus dem Dokument entfernt werden soll, aufgerufen.

 **Examples:** 

Zeigt, wie man das Ändern von Knoten mit einem Callback anpasst.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs/) |  |

