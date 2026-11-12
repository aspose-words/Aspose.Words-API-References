---
title: "NodeImporter"
linktitle: "NodeImporter"
second_title: "Aspose.Words для Java"
description: "Позволяет эффективно выполнять повторный импорт узлов из одного документа в другой в Java."
type: docs
weight: 480
url: /ru/java/com.aspose.words/nodeimporter/
---

**Inheritance:**
java.lang.Object
```
public class NodeImporter
```

Позволяет эффективно выполнять повторный импорт узлов из одного документа в другой.

Чтобы узнать больше, посетите статью документации [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_].

 **Remarks:** 

Aspose.Words предоставляет функциональность для простого копирования и перемещения фрагментов между документами Microsoft Word. Это называется «импортом узлов». Прежде чем вставить фрагмент из одного документа в другой, его необходимо «импортировать». Импорт создаёт глубокую копию оригинального узла, готовую к вставке в целевой документ.

Самый простой способ импортировать узел — использовать метод [DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase/\#importNode-com.aspose.words.Node--boolean), предоставляемый объектом [DocumentBase](../../com.aspose.words/documentbase/).

Однако когда необходимо импортировать узлы из одного документа в другой многократно, лучше использовать класс [NodeImporter](../../com.aspose.words/nodeimporter/). Класс [NodeImporter](../../com.aspose.words/nodeimporter/) позволяет минимизировать количество стилей и списков, создаваемых в целевом документе.

Копирование или перемещение фрагментов из одного документа Microsoft Word в другой представляет ряд технических проблем для Aspose.Words. В документе Word стили и форматирование списков хранятся централизованно, отдельно от текста документа. Параграфы и участки текста лишь ссылаются на стили с помощью внутренних уникальных идентификаторов.

Проблемы возникают из‑за того, что стили и списки различаются в разных документах. Например, чтобы скопировать абзац, отформатированный стилем Heading 1, из одного документа в другой, необходимо учесть несколько факторов: решить, следует ли копировать стиль Heading 1 из исходного документа в целевой, клонировать абзац, обновить клонированный абзац так, чтобы он ссылался на правильный стиль Heading 1 в целевом документе. Если стиль нужно скопировать, следует проанализировать и, при необходимости, также скопировать все стили, на которые он ссылается (на основе стиля и стиля следующего абзаца) и так далее. Аналогичные проблемы возникают при копировании маркированных или нумерованных абзацев, поскольку Microsoft Word хранит определения списков отдельно от текста.

Класс [NodeImporter](../../com.aspose.words/nodeimporter/) похож на контекст, который хранит "таблицы преобразования" во время импорта. Он корректно преобразует стили и списки между исходным и целевым документами.

 **Examples:** 

Показывает, как вставить содержимое одного документа в закладку другого документа.

```

 public void insertAtBookmark() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("InsertionPoint");
     builder.write("We will insert a document here: ");
     builder.endBookmark("InsertionPoint");

     Document docToInsert = new Document();
     builder = new DocumentBuilder(docToInsert);

     builder.write("Hello world!");

     docToInsert.save(getArtifactsDir() + "NodeImporter.InsertAtMergeField.docx");

     Bookmark bookmark = doc.getRange().getBookmarks().get("InsertionPoint");
     insertDocument(bookmark.getBookmarkStart().getParentNode(), docToInsert);

     Assert.assertEquals("We will insert a document here: " +
             "\rHello world!", doc.getText().trim());
 }

 /// 
 /// Inserts the contents of a document after the specified node.
 /// 
 static void insertDocument(Node insertionDestination, Document docToInsert) {
     if (((insertionDestination.getNodeType()) == (NodeType.PARAGRAPH)) || ((insertionDestination.getNodeType()) == (NodeType.TABLE))) {
         CompositeNode destinationParent = insertionDestination.getParentNode();

         NodeImporter importer =
                 new NodeImporter(docToInsert, insertionDestination.getDocument(), ImportFormatMode.KEEP_SOURCE_FORMATTING);

         // Loop through all block-level nodes in the section's body,
         // then clone and insert every node that is not the last empty paragraph of a section.
         for (Section srcSection : docToInsert.getSections())
             for (Node srcNode : srcSection.getBody()) {
                 if (((srcNode.getNodeType()) == (NodeType.PARAGRAPH))) {
                     Paragraph para = (Paragraph) srcNode;
                     if (para.isEndOfSection() && !para.hasChildNodes())
                         continue;
                 }

                 Node newNode = importer.importNode(srcNode, true);

                 destinationParent.insertAfter(newNode, insertionDestination);
                 insertionDestination = newNode;
             }
     } else {
         throw new IllegalArgumentException("The destination node should be either a paragraph or table.");
     }
 }
 
```


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int) | Инициализирует новый экземпляр этого класса. |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean) | Импортирует узел из одного документа в другой. |
### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |

### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


Импортирует узел из одного документа в другой.

 **Remarks:** 

Импорт узла создаёт копию исходного узла, принадлежащего импортирующему документу. Возвращённый узел не имеет родителя. Исходный узел не изменяется и не удаляется из оригинального документа.

Прежде чем узел из другого документа можно будет вставить в текущий документ, его необходимо импортировать. Во время импорта свойства, специфичные для документа, такие как ссылки на стили и списки, преобразуются из оригинального в импортирующий документ. После импорта узел можно вставить в нужное место документа, используя [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) или [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node).

Если исходный узел уже принадлежит целевому документу, то просто создаётся глубокая копия исходного узла.

 **Examples:** 

Показывает, как вставить содержимое одного документа в закладку другого документа.

```

 public void insertAtBookmark() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("InsertionPoint");
     builder.write("We will insert a document here: ");
     builder.endBookmark("InsertionPoint");

     Document docToInsert = new Document();
     builder = new DocumentBuilder(docToInsert);

     builder.write("Hello world!");

     docToInsert.save(getArtifactsDir() + "NodeImporter.InsertAtMergeField.docx");

     Bookmark bookmark = doc.getRange().getBookmarks().get("InsertionPoint");
     insertDocument(bookmark.getBookmarkStart().getParentNode(), docToInsert);

     Assert.assertEquals("We will insert a document here: " +
             "\rHello world!", doc.getText().trim());
 }

 /// 
 /// Inserts the contents of a document after the specified node.
 /// 
 static void insertDocument(Node insertionDestination, Document docToInsert) {
     if (((insertionDestination.getNodeType()) == (NodeType.PARAGRAPH)) || ((insertionDestination.getNodeType()) == (NodeType.TABLE))) {
         CompositeNode destinationParent = insertionDestination.getParentNode();

         NodeImporter importer =
                 new NodeImporter(docToInsert, insertionDestination.getDocument(), ImportFormatMode.KEEP_SOURCE_FORMATTING);

         // Loop through all block-level nodes in the section's body,
         // then clone and insert every node that is not the last empty paragraph of a section.
         for (Section srcSection : docToInsert.getSections())
             for (Node srcNode : srcSection.getBody()) {
                 if (((srcNode.getNodeType()) == (NodeType.PARAGRAPH))) {
                     Paragraph para = (Paragraph) srcNode;
                     if (para.isEndOfSection() && !para.hasChildNodes())
                         continue;
                 }

                 Node newNode = importer.importNode(srcNode, true);

                 destinationParent.insertAfter(newNode, insertionDestination);
                 insertionDestination = newNode;
             }
     } else {
         throw new IllegalArgumentException("The destination node should be either a paragraph or table.");
     }
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node/) | Узел для импорта. |
| isImportChildren | boolean | true  — импортировать все дочерние узлы рекурсивно; иначе,  false . |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned, imported node. The node belongs to the destination document, but has no parent.
