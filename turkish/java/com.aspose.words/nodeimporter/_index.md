---
title: "NodeImporter"
linktitle: "NodeImporter"
second_title: "Aspose.Words Java için"
description: "Java'da bir belgeden diğerine düğümlerin tekrarlı olarak verimli bir şekilde içe aktarılmasını sağlar."
type: docs
weight: 480
url: /tr/java/com.aspose.words/nodeimporter/
---

**Inheritance:**
java.lang.Object
```
public class NodeImporter
```

Bir belgeden diğerine düğümlerin tekrarlı ithalatını verimli bir şekilde gerçekleştirmeye olanak tanır.

Daha fazla bilgi edinmek için, [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Aspose.Words, Microsoft Word belgeleri arasında parçaları kolayca kopyalama ve taşıma işlevi sağlar. Bu, "düğümleri içe aktarma" olarak bilinir. Bir belgeden başka bir belgeye bir parçayı eklemeden önce, onu "içe aktarmanız" gerekir. İçe aktarma, orijinal düğümün derin bir kopyasını oluşturur ve hedef belgeye eklenmeye hazır hâle getirir.

Bir düğümü içe aktarmanın en basit yolu, [DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase/\#importNode-com.aspose.words.Node--boolean) metodunu sağlayan [DocumentBase](../../com.aspose.words/documentbase/) nesnesini kullanmaktır.

Ancak, bir belgeden başka bir belgeye düğümleri birden çok kez içe aktarmanız gerektiğinde, [NodeImporter](../../com.aspose.words/nodeimporter/) sınıfını kullanmak daha iyidir. [NodeImporter](../../com.aspose.words/nodeimporter/) sınıfı, hedef belgede oluşturulan stil ve liste sayısını en aza indirmeyi sağlar.

Bir Microsoft Word belgesinden diğerine parçaları kopyalamak veya taşımak, Aspose.Words için bir dizi teknik zorluk ortaya çıkarır. Bir Word belgesinde stiller ve liste biçimlendirmesi, belgenin metninden ayrı olarak merkezi bir şekilde depolanır. Paragraflar ve metin akışları yalnızca stillere dahili benzersiz tanımlayıcılar aracılığıyla referans verir.

Zorluklar, stillerin ve listelerin farklı belgelerde farklı olmasından kaynaklanır. Örneğin, bir belgeden diğerine Heading 1 stiliyle biçimlendirilmiş bir paragrafı kopyalamak için dikkate alınması gereken birkaç husus vardır: Heading 1 stilinin kaynak belgeden hedef belgeye kopyalanıp kopyalanmayacağına karar vermek, paragrafı klonlamak, klonlanan paragrafı hedef belgede doğru Heading 1 stiline başvuracak şekilde güncellemek. Stil kopyalanması gerekiyorsa, stilin referans verdiği (stil ve sonraki paragraf stili temelinde) tüm stiller analiz edilmeli ve gerekirse kopyalanmalıdır ve benzeri. Madde işaretli veya numaralı paragrafların kopyalanmasında da benzer sorunlar ortaya çıkar çünkü Microsoft Word, liste tanımlarını metinden ayrı olarak depolar.

Bu [NodeImporter](../../com.aspose.words/nodeimporter/) sınıfı, içe aktarma sırasında "çeviri tablolarını" tutan bir bağlam gibidir. Kaynak ve hedef belgelerdeki stiller ve listeler arasında doğru bir şekilde çeviri yapar.

 **Examples:** 

Bir belgenin içeriğinin başka bir belgedeki bir yer imine nasıl ekleneceğini gösterir.

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
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int) | Bu sınıfın yeni bir örneğini başlatır. |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean) | Bir belgeden diğerine bir düğüm içe aktarır. |
### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |

### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


Bir belgeden diğerine bir düğüm içe aktarır.

 **Remarks:** 

Bir düğümün içe aktarılması, içe aktaran belgeye ait kaynak düğümün bir kopyasını oluşturur. Döndürülen düğümün ebeveyni yoktur. Kaynak düğüm, orijinal belgede değiştirilmez veya kaldırılmaz.

Başka bir belgeden bir düğüm bu belgeye eklenmeden önce içe aktarılmalıdır. İçe aktarma sırasında, stillere ve listelere referans gibi belgeye özgü özellikler orijinalden içe aktaran belgeye çevrilir. Düğüm içe aktarıldıktan sonra, belge içinde uygun konuma [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) veya [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node) kullanılarak eklenebilir.

Kaynak düğüm zaten hedef belgeye aitse, sadece kaynak düğümün derin bir klonu oluşturulur.

 **Examples:** 

Bir belgenin içeriğinin başka bir belgedeki bir yer imine nasıl ekleneceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node/) | İçe aktarılacak düğüm. |
| isImportChildren | boolean | true  tüm alt düğümleri özyinelemeli olarak içe aktarmak için; aksi takdirde,  false . |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned, imported node. The node belongs to the destination document, but has no parent.
