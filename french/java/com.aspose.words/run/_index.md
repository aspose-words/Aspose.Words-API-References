---
title: "Run"
linktitle: "Run"
second_title: "Aspose.Words pour Java"
description: "Représente une séquence de caractères avec le même format de police en Java."
type: docs
weight: 593
url: /fr/java/com.aspose.words/run/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/), [com.aspose.words.Inline](../../com.aspose.words/inline/)
```
public class Run extends Inline
```

Représente une séquence de caractères avec la même mise en forme de police.

Pour en savoir plus, consultez l'article de documentation [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

Tout le texte du document est stocké dans des séquences de texte.

[Run](../../com.aspose.words/run/) can only be a child of [Paragraph](../../com.aspose.words/paragraph/) or inline [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/).

 **Examples:** 

Montre comment formater une séquence de texte en utilisant sa propriété de police.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

Montre comment ajouter, mettre à jour et supprimer des nœuds enfants dans la collection d'enfants d'un CompositeNode.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

Montre comment construire manuellement un document Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Constructors

| Constructor | Description |
| --- | --- |
| [Run(DocumentBase doc)](#Run-com.aspose.words.DocumentBase) | Initialise une nouvelle instance de la classe [Run](../../com.aspose.words/run/). |
| [Run(DocumentBase doc, String text)](#Run-com.aspose.words.DocumentBase-java.lang.String) | Initialise une nouvelle instance de la classe **Run**. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Accepte un visiteur. |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Crée un duplicata du nœud. |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int) |  |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Obtient le premier ancêtre du type d'objet spécifié. |
| [getCustomNodeId()](#getCustomNodeId) | Spécifie l'identifiant personnalisé du nœud. |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Obtient le document auquel ce nœud appartient. |
| [getDocument_IInline()](#getDocument-IInline) |  |
| [getFont()](#getFont) | Fournit l'accès au formatage de police de cet objet. |
| [getNextSibling()](#getNextSibling) | Obtient le nœud immédiatement suivant ce nœud. |
| [getNodeType()](#getNodeType) | Renvoie [NodeType.RUN](../../com.aspose.words/nodetype/\#RUN). |
| [getParentNode()](#getParentNode) | Obtient le parent immédiat de ce nœud. |
| [getParentParagraph()](#getParentParagraph) | Récupère le [Paragraph](../../com.aspose.words/paragraph/) parent de ce nœud. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline) |  |
| [getPhoneticGuide()](#getPhoneticGuide) | Obtient un objet [getPhoneticGuide()](../../com.aspose.words/run/\#getPhoneticGuide). |
| [getPreviousSibling()](#getPreviousSibling) | Obtient le nœud immédiatement précédant ce nœud. |
| [getRange()](#getRange) | Renvoie un objet [Range](../../com.aspose.words/range/) qui représente la partie d'un document contenue dans ce nœud. |
| [getText()](#getText) | Obtient le texte de la séquence. |
| [isComposite()](#isComposite) | Renvoie  true  si ce nœud peut contenir d'autres nœuds. |
| [isDeleteRevision()](#isDeleteRevision) | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [isFormatRevision()](#isFormatRevision) | Renvoie true si le formatage de l'objet a été modifié dans Microsoft Word alors que le suivi des modifications était activé. |
| [isInsertRevision()](#isInsertRevision) | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [isMoveFromRevision()](#isMoveFromRevision) | Renvoie  true  si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [isMoveToRevision()](#isMoveToRevision) | Renvoie  true  si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [isPhoneticGuide()](#isPhoneticGuide) | Obtient une valeur booléenne indiquant si la séquence est un guide phonétique. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Obtient le nœud précédent selon l'algorithme de parcours d'arbre en pré-ordre. |
| [remove()](#remove) | Se supprime du parent. |
| [removeMoveRevisions()](#removeMoveRevisions) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Spécifie l'identifiant personnalisé du nœud. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setText(String value)](#setText-java.lang.String) | Définit le texte de la séquence. |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| [toString(int saveFormat)](#toString-int) |  |
### Run(DocumentBase doc) {#Run-com.aspose.words.DocumentBase}
```
public Run(DocumentBase doc)
```


Initialise une nouvelle instance de la classe [Run](../../com.aspose.words/run/).

 **Remarks:** 

Lorsque [Run](../../com.aspose.words/run/) est créé, il appartient au document spécifié, mais n'est pas encore intégré au document et [Node.getParentNode()](../../com.aspose.words/node/\#getParentNode) est null.

Pour ajouter [Run](../../com.aspose.words/run/) au document, utilisez [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node) ou [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) sur le paragraphe où vous souhaitez insérer la séquence.

 **Examples:** 

Montre comment construire manuellement un document Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) | Le document propriétaire. |

### Run(DocumentBase doc, String text) {#Run-com.aspose.words.DocumentBase-java.lang.String}
```
public Run(DocumentBase doc, String text)
```


Initialise une nouvelle instance de la classe **Run**.

 **Remarks:** 

Lorsque [Run](../../com.aspose.words/run/) est créé, il appartient au document spécifié, mais n'est pas encore intégré au document et [Node.getParentNode()](../../com.aspose.words/node/\#getParentNode) est null.

Pour ajouter [Run](../../com.aspose.words/run/) au document, utilisez [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node) ou [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) sur le paragraphe où vous souhaitez insérer la séquence.

 **Examples:** 

Montre comment formater une séquence de texte en utilisant sa propriété de police.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) | Le document propriétaire. |
| text | java.lang.String | Le texte de la séquence. |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Accepte un visiteur.

 **Remarks:** 

Appelle [DocumentVisitor.visitRun(com.aspose.words.Run)](../../com.aspose.words/documentvisitor/\#visitRun-com.aspose.words.Run).

Pour plus d'informations, consultez le motif de conception Visitor.

 **Examples:** 

Montre comment imprimer la structure des nœuds de chaque en-tête et pied de page dans un document.

```

 public void headerFooterToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());

     // An alternative way of accessing a document's header/footers section-by-section is by accessing the collection.
     HeaderFooter[] headerFooters = doc.getFirstSection().getHeadersFooters().toArray();
     Assert.assertEquals(3, headerFooters.length);
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered HeaderFooter nodes and their children.
 /// 
 public static class HeaderFooterStructurePrinter extends DocumentVisitor {
     public HeaderFooterStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideHeaderFooter = false;
     }

     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideHeaderFooter) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a HeaderFooter node is encountered in the document.
     /// 
     public int visitHeaderFooterStart(final HeaderFooter headerFooter) {
         indentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.getHeaderFooterType());
         mDocTraversalDepth++;
         mVisitorIsInsideHeaderFooter = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a HeaderFooter node have been visited.
     /// 
     public int visitHeaderFooterEnd(final HeaderFooter headerFooter) {
         mDocTraversalDepth--;
         indentAndAppendLine("[HeaderFooter end]");
         mVisitorIsInsideHeaderFooter = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideHeaderFooter;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Le visiteur qui visitera le nœud. |

**Returns:**
booléen - false si le visiteur a demandé l'arrêt de l'énumération.
### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean}
```
public Node deepClone(boolean isCloneChildren)
```


Crée un duplicata du nœud.

 **Remarks:** 

Cette méthode sert de constructeur de copie pour les nœuds. Le nœud cloné n'a pas de parent, mais appartient au même document que le nœud original.

Cette méthode effectue toujours une copie profonde du nœud. Le paramètre  isCloneChildren  spécifie s'il faut également copier tous les nœuds enfants.

 **Examples:** 

Montre comment cloner un nœud composite.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();
 para.appendChild(new Run(doc, "Hello world!"));

 // Below are two ways of cloning a composite node.
 // 1 -  Create a clone of a node, and create a clone of each of its child nodes as well.
 Node cloneWithChildren = para.deepClone(true);

 Assert.assertTrue(((CompositeNode) cloneWithChildren).hasChildNodes());
 Assert.assertEquals("Hello world!", cloneWithChildren.getText().trim());

 // 2 -  Create a clone of a node just by itself without any children.
 Node cloneWithoutChildren = para.deepClone(false);

 Assert.assertFalse(((CompositeNode) cloneWithoutChildren).hasChildNodes());
 Assert.assertEquals("", cloneWithoutChildren.getText().trim());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| isCloneChildren | boolean | True pour cloner récursivement le sous-arbre sous le nœud spécifié ; false pour ne cloner que le nœud lui-même. |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned node.
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### getAncestor(int ancestorType) {#getAncestor-int}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class}
```
public CompositeNode getAncestor(Class ancestorType)
```


Obtient le premier ancêtre du type d'objet spécifié.

 **Remarks:** 

Le type d'ancêtre correspond s'il est égal à  ancestorType  ou dérivé de  ancestorType .

 **Examples:** 

Montre comment déterminer si des tables sont imbriquées.

```

 public void calculateDepthOfNestedTables() throws Exception {
     Document doc = new Document(getMyDir() + "Nested tables.docx");
     NodeCollection tables = doc.getChildNodes(NodeType.TABLE, true);
     for (int i = 0; i < tables.getCount(); i++) {
         Table table = (Table) tables.get(i);

         // Find out if any cells in the table have other tables as children.
         int count = getChildTableCount(table);
         System.out.print(MessageFormat.format("Table #{0} has {1} tables directly within its cells", i, count));

         // Find out if the table is nested inside another table, and, if so, at what depth.
         int tableDepth = getNestedDepthOfTable(table);

         if (tableDepth > 0)
             System.out.println(MessageFormat.format("Table #{0} is nested inside another table at depth of {1}", i, tableDepth));
         else
             System.out.println(MessageFormat.format("Table #{0} is a non nested table (is not a child of another table)", i));
     }
 }

 // Calculates what level a table is nested inside other tables.
 //
 // Returns An integer containing the level the table is nested at.
 // 0 = Table is not nested inside any other table
 // 1 = Table is nested within one parent table
 // 2 = Table is nested within two parent tables etc..
 private static int getNestedDepthOfTable(final Table table) {
     int depth = 0;
     Node parent = table.getAncestor(table.getNodeType());

     while (parent != null) {
         depth++;
         parent = parent.getAncestor(Table.class);
     }

     return depth;
 }

 // Determines if a table contains any immediate child table within its cells.
 // Does not recursively traverse through those tables to check for further tables.
 //
 // Returns true if at least one child cell contains a table.
 // Returns false if no cells in the table contains a table.
 private static int getChildTableCount(final Table table) {
     int childTableCount = 0;

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             TableCollection childTables = cell.getTables();

             if (childTables.getCount() > 0) childTableCount++;
         }
     }

     return childTableCount;
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| ancestorType | java.lang.Class | Le type d'objet de l'ancêtre à récupérer. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.
### getCustomNodeId() {#getCustomNodeId}
```
public int getCustomNodeId()
```


Spécifie l'identifiant personnalisé du nœud.

 **Remarks:** 

La valeur par défaut est zéro.

Cet identifiant peut être défini et utilisé arbitrairement. Par exemple, comme clé pour obtenir des données externes.

Note importante, la valeur spécifiée n'est pas enregistrée dans un fichier de sortie et n'existe que pendant la durée de vie du nœud.

 **Examples:** 

Montre comment parcourir la collection de nœuds enfants d'un nœud composite.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```

**Returns:**
int - La valeur int correspondante.
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Obtient le document auquel ce nœud appartient.

 **Remarks:** 

Le nœud appartient toujours à un document même s'il vient d'être créé et n'a pas encore été ajouté à l'arbre, ou s'il a été retiré de l'arbre.

 **Examples:** 

Montre comment créer un nœud et définir son document propriétaire.

```

 Document doc = new Document();
 Paragraph para = new Paragraph(doc);
 para.appendChild(new Run(doc, "Hello world!"));

 // We have not yet appended this paragraph as a child to any composite node.
 Assert.assertNull(para.getParentNode());

 // If a node is an appropriate child node type of another composite node,
 // we can attach it as a child only if both nodes have the same owner document.
 // The owner document is the document we passed to the node's constructor.
 // We have not attached this paragraph to the document, so the document does not contain its text.
 Assert.assertEquals(para.getDocument(), doc);
 Assert.assertEquals("", doc.getText().trim());

 // Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
 para.getParagraphFormat().setStyleName("Heading 1");

 // Add this node to the document, and then verify its contents.
 doc.getFirstSection().getBody().appendChild(para);

 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The document to which this node belongs.
### getDocument_IInline() {#getDocument-IInline}
```
public DocumentBase getDocument_IInline()
```




**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/)
### getFont() {#getFont}
```
public Font getFont()
```


Fournit l'accès au formatage de police de cet objet.

 **Examples:** 

Montre comment construire manuellement un document Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getNextSibling() {#getNextSibling}
```
public Node getNextSibling()
```


Obtient le nœud immédiatement suivant ce nœud.

 **Remarks:** 

S'il n'y a pas de nœud suivant, un  null  est renvoyé.

 **Examples:** 

Montre comment parcourir l'arbre des nœuds enfants d'un nœud composite.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

Montre comment utiliser la propriété NextSibling d'un nœud pour énumérer ses enfants immédiats.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 for (Node node = doc.getFirstSection().getBody().getFirstChild(); node != null; node = node.getNextSibling()) {
     System.out.println(Node.nodeTypeToString(node.getNodeType()));
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately following this node.
### getNodeType() {#getNodeType}
```
public int getNodeType()
```


Renvoie [NodeType.RUN](../../com.aspose.words/nodetype/\#RUN).

 **Examples:** 

Montre comment parcourir l'arbre des nœuds enfants d'un nœud composite.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
int - [NodeType.RUN](../../com.aspose.words/nodetype/\#RUN). La valeur retournée est l'une des constantes [NodeType](../../com.aspose.words/nodetype/).
### getParentNode() {#getParentNode}
```
public CompositeNode getParentNode()
```


Obtient le parent immédiat de ce nœud.

 **Remarks:** 

Si un nœud vient d'être créé et n'a pas encore été ajouté à l'arbre, ou s'il a été retiré de l'arbre, le parent est  null .

 **Examples:** 

Montre comment accéder au nœud parent d'un nœud.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();

 // Append a child Run node to the document's first paragraph.
 Run run = new Run(doc, "Hello world!");
 para.appendChild(run);

 // The paragraph is the parent node of the run node. We can trace this lineage
 // all the way to the document node, which is the root of the document's node tree.
 Assert.assertEquals(para, run.getParentNode());
 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals(doc.getFirstSection(), doc.getFirstSection().getBody().getParentNode());
 Assert.assertEquals(doc, doc.getFirstSection().getParentNode());
 
```

Montre comment créer un nœud et définir son document propriétaire.

```

 Document doc = new Document();
 Paragraph para = new Paragraph(doc);
 para.appendChild(new Run(doc, "Hello world!"));

 // We have not yet appended this paragraph as a child to any composite node.
 Assert.assertNull(para.getParentNode());

 // If a node is an appropriate child node type of another composite node,
 // we can attach it as a child only if both nodes have the same owner document.
 // The owner document is the document we passed to the node's constructor.
 // We have not attached this paragraph to the document, so the document does not contain its text.
 Assert.assertEquals(para.getDocument(), doc);
 Assert.assertEquals("", doc.getText().trim());

 // Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
 para.getParagraphFormat().setStyleName("Heading 1");

 // Add this node to the document, and then verify its contents.
 doc.getFirstSection().getBody().appendChild(para);

 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The immediate parent of this node.
### getParentParagraph() {#getParentParagraph}
```
public Paragraph getParentParagraph()
```


Récupère le [Paragraph](../../com.aspose.words/paragraph/) parent de ce nœud.

 **Examples:** 

Montre comment déterminer le type de révision d'un nœud inline.

```

 Document doc = new Document(getMyDir() + "Revision runs.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to change the proposed change effectively.
 Assert.assertEquals(6, doc.getRevisions().getCount());

 // The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
 Run run = (Run) doc.getRevisions().get(0).getParentNode();

 Paragraph firstParagraph = run.getParentParagraph();
 RunCollection runs = firstParagraph.getRuns();

 Assert.assertEquals(runs.getCount(), 6);

 // Below are five types of revisions that can flag an Inline node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Assert.assertTrue(runs.get(2).isInsertRevision());

 // 2 -  A "format" revision:
 // This revision occurs when we change the formatting of text while tracking changes.
 Assert.assertTrue(runs.get(2).isFormatRevision());

 // 3 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 Assert.assertTrue(runs.get(4).isMoveFromRevision());

 // 4 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 Assert.assertTrue(runs.get(1).isMoveToRevision());

 // 5 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 Assert.assertTrue(runs.get(5).isDeleteRevision());
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The corresponding [Paragraph](../../com.aspose.words/paragraph/) value.
### getParentParagraph_IInline() {#getParentParagraph-IInline}
```
public Paragraph getParentParagraph_IInline()
```




**Returns:**
[Paragraph](../../com.aspose.words/paragraph/)
### getPhoneticGuide() {#getPhoneticGuide}
```
public PhoneticGuide getPhoneticGuide()
```


Obtient un objet [getPhoneticGuide()](../../com.aspose.words/run/\#getPhoneticGuide).

 **Examples:** 

Montre comment obtenir les propriétés du guide phonétique.

```

 Document doc = new Document(getMyDir() + "Phonetic guide.docx");

 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();
 // Use phonetic guide in the Asian text.
 Assert.assertEquals(true, runs.get(0).isPhoneticGuide());

 PhoneticGuide phoneticGuide = runs.get(0).getPhoneticGuide();
 Assert.assertEquals("base", phoneticGuide.getBaseText());
 Assert.assertEquals("ruby", phoneticGuide.getRubyText());
 
```

**Returns:**
[PhoneticGuide](../../com.aspose.words/phoneticguide/) - A [getPhoneticGuide()](../../com.aspose.words/run/\#getPhoneticGuide) object.
### getPreviousSibling() {#getPreviousSibling}
```
public Node getPreviousSibling()
```


Obtient le nœud immédiatement précédant ce nœud.

 **Remarks:** 

S'il n'y a pas de nœud précédent, un  null  est renvoyé.

 **Examples:** 

Montre comment utiliser les méthodes de Node et CompositeNode pour supprimer une section avant la dernière section du document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately preceding this node.
### getRange() {#getRange}
```
public Range getRange()
```


Renvoie un objet [Range](../../com.aspose.words/range/) qui représente la partie d'un document contenue dans ce nœud.

 **Examples:** 

Montre comment supprimer tous les nœuds d'une plage.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text to the first section in the document, and then add another section.
 builder.write("Section 1. ");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.write("Section 2.");

 Assert.assertEquals("Section 1. \fSection 2.", doc.getText().trim());

 // Remove the first section entirely by removing all the nodes
 // within its range, including the section itself.
 doc.getSections().get(0).getRange().delete();

 Assert.assertEquals(1, doc.getSections().getCount());
 Assert.assertEquals("Section 2.", doc.getText().trim());
 
```

**Returns:**
[Range](../../com.aspose.words/range/) - A [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.
### getText() {#getText}
```
public String getText()
```


Obtient le texte de la séquence.

 **Examples:** 

Montre comment construire manuellement un document Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
java.lang.String - Le texte du run.
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Renvoie  true  si ce nœud peut contenir d'autres nœuds. (197141,6)

 **Examples:** 

Montre comment parcourir l'arbre des nœuds enfants d'un nœud composite.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
boolean -  true  si ce nœud peut contenir d'autres nœuds.
### isDeleteRevision() {#isDeleteRevision}
```
public boolean isDeleteRevision()
```


Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé.

 **Examples:** 

Montre comment déterminer le type de révision d'un nœud inline.

```

 Document doc = new Document(getMyDir() + "Revision runs.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to change the proposed change effectively.
 Assert.assertEquals(6, doc.getRevisions().getCount());

 // The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
 Run run = (Run) doc.getRevisions().get(0).getParentNode();

 Paragraph firstParagraph = run.getParentParagraph();
 RunCollection runs = firstParagraph.getRuns();

 Assert.assertEquals(runs.getCount(), 6);

 // Below are five types of revisions that can flag an Inline node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Assert.assertTrue(runs.get(2).isInsertRevision());

 // 2 -  A "format" revision:
 // This revision occurs when we change the formatting of text while tracking changes.
 Assert.assertTrue(runs.get(2).isFormatRevision());

 // 3 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 Assert.assertTrue(runs.get(4).isMoveFromRevision());

 // 4 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 Assert.assertTrue(runs.get(1).isMoveToRevision());

 // 5 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 Assert.assertTrue(runs.get(5).isDeleteRevision());
 
```

**Returns:**
boolean - True si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé.
### isFormatRevision() {#isFormatRevision}
```
public boolean isFormatRevision()
```


Renvoie true si le formatage de l'objet a été modifié dans Microsoft Word alors que le suivi des modifications était activé.

 **Examples:** 

Montre comment déterminer le type de révision d'un nœud inline.

```

 Document doc = new Document(getMyDir() + "Revision runs.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to change the proposed change effectively.
 Assert.assertEquals(6, doc.getRevisions().getCount());

 // The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
 Run run = (Run) doc.getRevisions().get(0).getParentNode();

 Paragraph firstParagraph = run.getParentParagraph();
 RunCollection runs = firstParagraph.getRuns();

 Assert.assertEquals(runs.getCount(), 6);

 // Below are five types of revisions that can flag an Inline node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Assert.assertTrue(runs.get(2).isInsertRevision());

 // 2 -  A "format" revision:
 // This revision occurs when we change the formatting of text while tracking changes.
 Assert.assertTrue(runs.get(2).isFormatRevision());

 // 3 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 Assert.assertTrue(runs.get(4).isMoveFromRevision());

 // 4 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 Assert.assertTrue(runs.get(1).isMoveToRevision());

 // 5 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 Assert.assertTrue(runs.get(5).isDeleteRevision());
 
```

**Returns:**
boolean - True si le formatage de l'objet a été modifié dans Microsoft Word alors que le suivi des modifications était activé.
### isInsertRevision() {#isInsertRevision}
```
public boolean isInsertRevision()
```


Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé.

 **Examples:** 

Montre comment déterminer le type de révision d'un nœud inline.

```

 Document doc = new Document(getMyDir() + "Revision runs.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to change the proposed change effectively.
 Assert.assertEquals(6, doc.getRevisions().getCount());

 // The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
 Run run = (Run) doc.getRevisions().get(0).getParentNode();

 Paragraph firstParagraph = run.getParentParagraph();
 RunCollection runs = firstParagraph.getRuns();

 Assert.assertEquals(runs.getCount(), 6);

 // Below are five types of revisions that can flag an Inline node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Assert.assertTrue(runs.get(2).isInsertRevision());

 // 2 -  A "format" revision:
 // This revision occurs when we change the formatting of text while tracking changes.
 Assert.assertTrue(runs.get(2).isFormatRevision());

 // 3 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 Assert.assertTrue(runs.get(4).isMoveFromRevision());

 // 4 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 Assert.assertTrue(runs.get(1).isMoveToRevision());

 // 5 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 Assert.assertTrue(runs.get(5).isDeleteRevision());
 
```

**Returns:**
boolean - True si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé.
### isMoveFromRevision() {#isMoveFromRevision}
```
public boolean isMoveFromRevision()
```


Renvoie  true  si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé.

 **Examples:** 

Montre comment déterminer le type de révision d'un nœud inline.

```

 Document doc = new Document(getMyDir() + "Revision runs.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to change the proposed change effectively.
 Assert.assertEquals(6, doc.getRevisions().getCount());

 // The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
 Run run = (Run) doc.getRevisions().get(0).getParentNode();

 Paragraph firstParagraph = run.getParentParagraph();
 RunCollection runs = firstParagraph.getRuns();

 Assert.assertEquals(runs.getCount(), 6);

 // Below are five types of revisions that can flag an Inline node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Assert.assertTrue(runs.get(2).isInsertRevision());

 // 2 -  A "format" revision:
 // This revision occurs when we change the formatting of text while tracking changes.
 Assert.assertTrue(runs.get(2).isFormatRevision());

 // 3 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 Assert.assertTrue(runs.get(4).isMoveFromRevision());

 // 4 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 Assert.assertTrue(runs.get(1).isMoveToRevision());

 // 5 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 Assert.assertTrue(runs.get(5).isDeleteRevision());
 
```

**Returns:**
boolean -  true  si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé.
### isMoveToRevision() {#isMoveToRevision}
```
public boolean isMoveToRevision()
```


Renvoie  true  si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé.

 **Examples:** 

Montre comment déterminer le type de révision d'un nœud inline.

```

 Document doc = new Document(getMyDir() + "Revision runs.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to change the proposed change effectively.
 Assert.assertEquals(6, doc.getRevisions().getCount());

 // The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
 Run run = (Run) doc.getRevisions().get(0).getParentNode();

 Paragraph firstParagraph = run.getParentParagraph();
 RunCollection runs = firstParagraph.getRuns();

 Assert.assertEquals(runs.getCount(), 6);

 // Below are five types of revisions that can flag an Inline node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Assert.assertTrue(runs.get(2).isInsertRevision());

 // 2 -  A "format" revision:
 // This revision occurs when we change the formatting of text while tracking changes.
 Assert.assertTrue(runs.get(2).isFormatRevision());

 // 3 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 Assert.assertTrue(runs.get(4).isMoveFromRevision());

 // 4 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 Assert.assertTrue(runs.get(1).isMoveToRevision());

 // 5 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 Assert.assertTrue(runs.get(5).isDeleteRevision());
 
```

**Returns:**
boolean -  true  si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé.
### isPhoneticGuide() {#isPhoneticGuide}
```
public boolean isPhoneticGuide()
```


Obtient une valeur booléenne indiquant si la séquence est un guide phonétique.

 **Examples:** 

Montre comment obtenir les propriétés du guide phonétique.

```

 Document doc = new Document(getMyDir() + "Phonetic guide.docx");

 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();
 // Use phonetic guide in the Asian text.
 Assert.assertEquals(true, runs.get(0).isPhoneticGuide());

 PhoneticGuide phoneticGuide = runs.get(0).getPhoneticGuide();
 Assert.assertEquals("base", phoneticGuide.getBaseText());
 Assert.assertEquals("ruby", phoneticGuide.getRubyText());
 
```

**Returns:**
boolean - Une valeur booléenne indiquant que le run est un guide phonétique.
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre.

 **Examples:** 

Montre comment parcourir l'arbre des nœuds du document en utilisant l'algorithme de parcours pré-ordre, et supprimer toute forme rencontrée contenant une image.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | Le nœud supérieur (limite) du parcours. |

**Returns:**
[Node](../../com.aspose.words/node/) - Next node in pre-order order. Null if reached the  rootNode .
### nodeTypeToString(int nodeType) {#nodeTypeToString-int}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Obtient le nœud précédent selon l'algorithme de parcours d'arbre en pré-ordre.

 **Examples:** 

Montre comment parcourir l'arbre des nœuds du document en utilisant l'algorithme de parcours pré-ordre, et supprimer toute forme rencontrée contenant une image.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | Le nœud supérieur (limite) du parcours. |

**Returns:**
[Node](../../com.aspose.words/node/) - Previous node in pre-order order. Null if reached the  rootNode .
### remove() {#remove}
```
public void remove()
```


Se supprime du parent.

 **Examples:** 

Montre comment supprimer toutes les formes avec images d'un document.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 for (Shape shape : shapes)
     if (shape.hasImage())
         shape.remove();

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

Montre comment retirer tous les nœuds enfants d'un type spécifique d'un nœud composite.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Assert.assertEquals(2, doc.getChildNodes(NodeType.TABLE, true).getCount());

 Node curNode = doc.getFirstSection().getBody().getFirstChild();

 while (curNode != null) {
     // Save the next sibling node as a variable in case we want to move to it after deleting this node.
     Node nextNode = curNode.getNextSibling();

     // A section body can contain Paragraph and Table nodes.
     // If the node is a Table, remove it from the parent.
     if (curNode.getNodeType() == NodeType.TABLE) {
         curNode.remove();
     }

     curNode = nextNode;
 }

 Assert.assertEquals(0, doc.getChildNodes(NodeType.TABLE, true).getCount());
 
```

### removeMoveRevisions() {#removeMoveRevisions}
```
public void removeMoveRevisions()
```




### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

### setCustomNodeId(int value) {#setCustomNodeId-int}
```
public void setCustomNodeId(int value)
```


Spécifie l'identifiant personnalisé du nœud.

 **Remarks:** 

La valeur par défaut est zéro.

Cet identifiant peut être défini et utilisé arbitrairement. Par exemple, comme clé pour obtenir des données externes.

Note importante, la valeur spécifiée n'est pas enregistrée dans un fichier de sortie et n'existe que pendant la durée de vie du nœud.

 **Examples:** 

Montre comment parcourir la collection de nœuds enfants d'un nœud composite.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La valeur  int  correspondante. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| valeur | java.lang.Object |  |

### setText(String value) {#setText-java.lang.String}
```
public void setText(String value)
```


Définit le texte de la séquence.

 **Examples:** 

Montre comment construire manuellement un document Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le texte de la séquence. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions}
```
public String toString(SaveOptions saveOptions)
```


Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées.

 **Examples:** 

Exporte le contenu d'un nœud vers une String au format HTML.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Node node = doc.getLastSection().getBody().getLastParagraph();

 // When we call the ToString method using the html SaveFormat overload,
 // it converts the node's contents to their raw html representation.
 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(SaveFormat.HTML));

 // We can also modify the result of this conversion using a SaveOptions object.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setExportRelativeFontSize(true);

 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(saveOptions));
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Spécifie les options qui contrôlent la façon dont le nœud est enregistré. |

**Returns:**
java.lang.String - Le contenu du nœud dans le format spécifié.
### toString(int saveFormat) {#toString-int}
```
public String toString(int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
