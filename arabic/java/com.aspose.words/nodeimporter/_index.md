---
title: "NodeImporter"
linktitle: "NodeImporter"
second_title: "Aspose.Words لـ Java"
description: "يسمح بأداء استيراد متكرر للعقد من مستند إلى آخر في Java بكفاءة."
type: docs
weight: 480
url: /ar/java/com.aspose.words/nodeimporter/
---

**Inheritance:**
java.lang.Object
```
public class NodeImporter
```

يسمح بأداء استيراد متكرر للعقد من مستند إلى آخر بكفاءة.

لمزيد من المعلومات، قم بزيارة مقالة وثائق [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_]

 **Remarks:** 

توفر Aspose.Words وظيفة لنسخ ونقل المقاطع بسهولة بين مستندات Microsoft Word. يُعرف هذا باسم "استيراد العقد". قبل أن تتمكن من إدراج مقطع من مستند إلى آخر، تحتاج إلى "استيراده". يُنشئ الاستيراد نسخة مستنسخة عميقة من العقدة الأصلية، جاهزة للإدراج في المستند الوجهة.

أسهل طريقة لاستيراد عقدة هي استخدام الطريقة [DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase/\#importNode-com.aspose.words.Node--boolean) التي يوفرها كائن [DocumentBase](../../com.aspose.words/documentbase/).

مع ذلك، عندما تحتاج إلى استيراد عقد من مستند إلى آخر عدة مرات، من الأفضل استخدام الفئة [NodeImporter](../../com.aspose.words/nodeimporter/). تسمح الفئة [NodeImporter](../../com.aspose.words/nodeimporter/) بتقليل عدد الأنماط والقوائم التي تُنشأ في المستند الوجهة.

إن نسخ أو نقل أجزاء من مستند Microsoft Word إلى آخر يطرح عددًا من التحديات التقنية لـ Aspose.Words. في مستند Word، يتم تخزين الأنماط وتنسيق القوائم مركزيًا، منفصلًا عن نص المستند. الفقرات ومقاطع النص تشير إلى الأنماط فقط عبر معرّفات فريدة داخلية.

تنشأ التحديات من حقيقة أن الأنماط والقوائم تختلف بين المستندات. على سبيل المثال، لنسخ فقرة مُنسقة بنمط Heading 1 من مستند إلى آخر، يجب مراعاة عدة أمور: تحديد ما إذا كان يجب نسخ نمط Heading 1 من المستند المصدر إلى المستند الوجهة، استنساخ الفقرة، وتحديث الفقرة المستنسخة لتشير إلى نمط Heading 1 الصحيح في المستند الوجهة. إذا كان يجب نسخ النمط، يجب تحليل جميع الأنماط التي يشير إليها (استنادًا إلى النمط ونمط الفقرة التالية) وربما نسخها أيضًا وهكذا. توجد مشكلات مماثلة عند نسخ الفقرات ذات النقاط أو الأرقام لأن Microsoft Word يخزن تعريفات القوائم بشكل منفصل عن النص.

الفئة [NodeImporter](../../com.aspose.words/nodeimporter/) تشبه السياق الذي يحتفظ بـ "translation tables" أثناء الاستيراد. إنها تترجم بشكل صحيح بين الأنماط والقوائم في المستندات المصدر والوجهة.

 **Examples:** 

يوضح كيفية إدراج محتويات مستند واحد إلى إشارة مرجعية في مستند آخر.

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
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean) | يستورد عقدة من مستند إلى آخر. |
### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |

### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


يستورد عقدة من مستند إلى آخر.

 **Remarks:** 

إن استيراد عقدة ينشئ نسخة من العقدة المصدر التي تنتمي إلى المستند المستورد. العقدة المرتجعة لا تحتوي على أصل. العقدة المصدر لا تُعدل أو تُحذف من المستند الأصلي.

قبل أن يتم إدراج عقدة من مستند آخر في هذا المستند، يجب استيرادها. أثناء الاستيراد، تُترجم خصائص المستند الخاصة مثل الإشارات إلى الأنماط والقوائم من الأصل إلى المستند المستورد. بعد استيراد العقدة، يمكن إدراجها في المكان المناسب داخل المستند باستخدام [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) أو [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node).

إذا كانت العقدة المصدر تنتمي بالفعل إلى المستند الوجهة، فسيتم ببساطة إنشاء نسخة عميقة من العقدة المصدر.

 **Examples:** 

يوضح كيفية إدراج محتويات مستند واحد إلى إشارة مرجعية في مستند آخر.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node/) | العقدة المراد استيرادها. |
| isImportChildren | boolean | true لاستيراد جميع العقد الفرعية بشكل متكرر؛ وإلا، false. |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned, imported node. The node belongs to the destination document, but has no parent.
