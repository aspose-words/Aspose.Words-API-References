---
title: "FormField"
linktitle: "FormField"
second_title: "Aspose.Words für Java"
description: "Stellt ein einzelnes Formularfeld in Java dar."
type: docs
weight: 347
url: /de/java/com.aspose.words/formfield/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/), [com.aspose.words.Inline](../../com.aspose.words/inline/), [com.aspose.words.SpecialChar](../../com.aspose.words/specialchar/)
```
public class FormField extends SpecialChar
```

Stellt ein einzelnes Formularfeld dar.

Weitere Informationen finden Sie im Dokumentationsartikel [ Working with Form Fields ][Working with Form Fields].

 **Remarks:** 

Microsoft Word bietet die folgenden Formularfelder: Kontrollkästchen, Texteingabe und Dropdown (Kombinationsfeld).

[FormField](../../com.aspose.words/formfield/) is an inline-node and can only be a child of [Paragraph](../../com.aspose.words/paragraph/).

[FormField](../../com.aspose.words/formfield/) is represented in a document by a special character and positioned as a character within a line of text.

Ein vollständiges Formularfeld in einem Word-Dokument ist eine komplexe Struktur, die durch mehrere Knoten dargestellt wird: Feldanfang, Feldcode wie FORMTEXT, Formulardaten, Feldtrennzeichen, Feldresultat, Feldende und ein Lesezeichen. Um programmgesteuert Formularfelder in einem Word-Dokument zu erstellen, verwenden Sie [DocumentBuilder.insertCheckBox(java.lang.String, boolean, int)](../../com.aspose.words/documentbuilder/\#insertCheckBox-java.lang.String--boolean--int), **M:Aspose.Words.DocumentBuilder.InsertTextInput(System.String,Aspose.Words.Fields.TextFormFieldType,System.String,System.String,System.Int32)** und [DocumentBuilder.insertComboBox(java.lang.String, java.lang.String[], int)](../../com.aspose.words/documentbuilder/\#insertComboBox-java.lang.String--java.lang.String----int), die sicherstellen, dass alle Knoten des Formularfelds in der richtigen Reihenfolge und in einem geeigneten Zustand erstellt werden.

 **Examples:** 

Zeigt, wie man ein Kombinationsfeld einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Please select a fruit: ");

 // Insert a combo box which will allow a user to choose an option from a collection of strings.
 FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"Apple", "Banana", "Cherry"}, 0);

 Assert.assertEquals("MyComboBox", comboBox.getName());
 Assert.assertEquals(FieldType.FIELD_FORM_DROP_DOWN, comboBox.getType());
 Assert.assertEquals("Apple", comboBox.getResult());

 // The form field will appear in the form of a "select" html tag.
 doc.save(getArtifactsDir() + "FormFields.Create.html");
 
```

Zeigt, wie man das gesamte FormField formatiert, einschließlich des Feldwerts.

```

 Document doc = new Document(getMyDir() + "Form fields.docx");

 FormField formField = doc.getRange().getFormFields().get(0);
 formField.getFont().setBold(true);
 formField.getFont().setSize(24.0);
 formField.getFont().setColor(Color.RED);

 formField.setResult("Aspose.FormField");

 doc = DocumentHelper.saveOpen(doc);

 Run formFieldRun = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(1);

 Assert.assertEquals("Aspose.FormField", formFieldRun.getText());
 Assert.assertEquals(true, formFieldRun.getFont().getBold());
 Assert.assertEquals(24.0, formFieldRun.getFont().getSize());
 Assert.assertEquals(Color.RED.getRGB(), formFieldRun.getFont().getColor().getRGB());
 
```


[Working with Form Fields]: https://docs.aspose.com/words/java/working-with-form-fields/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Akzeptiert einen Besucher. |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Erstellt ein Duplikat des Knotens. |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int) |  |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Ermittelt den ersten Vorfahren des angegebenen Objekttyps. |
| [getCalculateOnExit()](#getCalculateOnExit) | True, wenn Verweise auf das angegebene Formularfeld automatisch aktualisiert werden, sobald das Feld verlassen wird. |
| [getCheckBoxSize()](#getCheckBoxSize) | Ermittelt die Größe des Kontrollkästchens in Punkten. |
| [getChecked()](#getChecked) | Ermittelt den aktivierten Status des Checkbox-Formularfelds. |
| [getCustomNodeId()](#getCustomNodeId) | Gibt eine benutzerdefinierte Knotenkennung an. |
| [getDefault()](#getDefault) | Ermittelt den Standardwert des Checkbox-Formularfelds. |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [getDocument_IInline()](#getDocument-IInline) |  |
| [getDropDownItems()](#getDropDownItems) | Stellt Zugriff auf die Elemente eines Dropdown-Formularfelds bereit. |
| [getDropDownSelectedIndex()](#getDropDownSelectedIndex) | Ermittelt den Index, der das aktuell ausgewählte Element in einem Dropdown-Formularfeld angibt. |
| [getEnabled()](#getEnabled) | True, wenn ein Formularfeld aktiviert ist. |
| [getEntryMacro()](#getEntryMacro) | Ermittelt den Namen eines Eingabe-Makros für das Formularfeld. |
| [getExitMacro()](#getExitMacro) | Ermittelt den Namen eines Beendigungs-Makros für das Formularfeld. |
| [getFont()](#getFont) | Stellt Zugriff auf die Schriftformatierung dieses Objekts bereit. |
| [getHelpText()](#getHelpText) | Ermittelt den Text, der in einer Meldungsbox angezeigt wird, wenn das Formularfeld den Fokus hat und der Benutzer F1 drückt. |
| [getMaxLength()](#getMaxLength) | Maximale Länge für das Textfeld. |
| [getName()](#getName) | Ermittelt den Namen des Formularfelds. |
| [getNextSibling()](#getNextSibling) | Ermittelt den Knoten, der unmittelbar auf diesen Knoten folgt. |
| [getNodeType()](#getNodeType) | Gibt [NodeType.FORM\_FIELD](../../com.aspose.words/nodetype/\#FORM-FIELD) zurück. |
| [getOwnHelp()](#getOwnHelp) | Gibt die Quelle des Textes an, der in einer Meldungsbox angezeigt wird, wenn ein Formularfeld den Fokus hat und der Benutzer F1 drückt. |
| [getOwnStatus()](#getOwnStatus) | Gibt die Quelle des Textes an, der in der Statusleiste angezeigt wird, wenn ein Formularfeld den Fokus hat. |
| [getParentNode()](#getParentNode) | Ermittelt den unmittelbaren übergeordneten Knoten dieses Knotens. |
| [getParentParagraph()](#getParentParagraph) | Ruft das übergeordnete [Paragraph](../../com.aspose.words/paragraph/) dieses Knotens ab. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline) |  |
| [getPreviousSibling()](#getPreviousSibling) | Ermittelt den Knoten, der unmittelbar vor diesem Knoten liegt. |
| [getRange()](#getRange) | Gibt ein [Range](../../com.aspose.words/range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [getResult()](#getResult) | Ermittelt eine Zeichenkette, die das Ergebnis dieses Formularfelds darstellt. |
| [getStatusText()](#getStatusText) | Ermittelt den Text, der in der Statusleiste angezeigt wird, wenn ein Formularfeld den Fokus hat. |
| [getText()](#getText) | Ermittelt das Sonderzeichen, das dieser Knoten darstellt. |
| [getTextInputDefault()](#getTextInputDefault) | Ermittelt die Standardzeichenkette oder einen Berechnungsausdruck eines Textformularfelds. |
| [getTextInputFormat()](#getTextInputFormat) | Ermittelt die Textformatierung für ein Textformularfeld. |
| [getTextInputType()](#getTextInputType) | Ermittelt den Typ eines Textformularfelds. |
| [getType()](#getType) | Gibt den Formularfeldtyp zurück. |
| [isCheckBoxExactSize()](#isCheckBoxExactSize) | Ermittelt den booleschen Wert, der angibt, ob die Größe des Textfelds automatisch oder explizit festgelegt ist. |
| [isCheckBoxExactSize(boolean value)](#isCheckBoxExactSize-boolean) | Setzt den booleschen Wert, der angibt, ob die Größe des Textfelds automatisch oder explizit festgelegt ist. |
| [isComposite()](#isComposite) | Gibt  true  zurück, wenn dieser Knoten andere Knoten enthalten kann. |
| [isDeleteRevision()](#isDeleteRevision) | Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [isFormatRevision()](#isFormatRevision) | Gibt true zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [isInsertRevision()](#isInsertRevision) | Gibt true zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [isMoveFromRevision()](#isMoveFromRevision) | Gibt  true  zurück, wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [isMoveToRevision()](#isMoveToRevision) | Gibt  true  zurück, wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [remove()](#remove) | Entfernt sich selbst vom übergeordneten Element. |
| [removeField()](#removeField) | Entfernt das gesamte Formularfeld, nicht nur das Sonderzeichen des Formularfelds. |
| [removeMoveRevisions()](#removeMoveRevisions) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [setCalculateOnExit(boolean value)](#setCalculateOnExit-boolean) | True, wenn Verweise auf das angegebene Formularfeld automatisch aktualisiert werden, sobald das Feld verlassen wird. |
| [setCheckBoxSize(double value)](#setCheckBoxSize-double) | Setzt die Größe des Kontrollkästchens in Punkten. |
| [setChecked(boolean value)](#setChecked-boolean) | Legt den aktivierten Status des Kontrollkästchen-Formularfelds fest. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Gibt eine benutzerdefinierte Knotenkennung an. |
| [setDefault(boolean value)](#setDefault-boolean) | Legt den Standardwert des Kontrollkästchen-Formularfelds fest. |
| [setDropDownSelectedIndex(int value)](#setDropDownSelectedIndex-int) | Legt den Index fest, der das aktuell ausgewählte Element in einem Dropdown-Formularfeld angibt. |
| [setEnabled(boolean value)](#setEnabled-boolean) | True, wenn ein Formularfeld aktiviert ist. |
| [setEntryMacro(String value)](#setEntryMacro-java.lang.String) | Legt einen Eingabe-Makronamen für das Formularfeld fest. |
| [setExitMacro(String value)](#setExitMacro-java.lang.String) | Legt einen Beendigungs-Makronamen für das Formularfeld fest. |
| [setHelpText(String value)](#setHelpText-java.lang.String) | Legt den Text fest, der in einer Meldungsbox angezeigt wird, wenn das Formularfeld den Fokus hat und der Benutzer F1 drückt. |
| [setMaxLength(int value)](#setMaxLength-int) | Maximale Länge für das Textfeld. |
| [setName(String value)](#setName-java.lang.String) | Legt den Namen des Formularfelds fest. |
| [setOwnHelp(boolean value)](#setOwnHelp-boolean) | Gibt die Quelle des Textes an, der in einer Meldungsbox angezeigt wird, wenn ein Formularfeld den Fokus hat und der Benutzer F1 drückt. |
| [setOwnStatus(boolean value)](#setOwnStatus-boolean) | Gibt die Quelle des Textes an, der in der Statusleiste angezeigt wird, wenn ein Formularfeld den Fokus hat. |
| [setResult(String value)](#setResult-java.lang.String) | Legt eine Zeichenkette fest, die das Ergebnis dieses Formularfelds darstellt. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setStatusText(String value)](#setStatusText-java.lang.String) | Legt den Text fest, der in der Statusleiste angezeigt wird, wenn ein Formularfeld den Fokus hat. |
| [setTextInputDefault(String value)](#setTextInputDefault-java.lang.String) | Legt die Standardzeichenkette oder einen Berechnungsausdruck eines Textformularfelds fest. |
| [setTextInputFormat(String value)](#setTextInputFormat-java.lang.String) | Legt die Textformatierung für ein Textformularfeld fest. |
| [setTextInputType(int value)](#setTextInputType-int) | Legt den Typ eines Textformularfelds fest. |
| [setTextInputValue(Object newValue)](#setTextInputValue-java.lang.Object) | Wendet das in [getTextInputFormat()](../../com.aspose.words/formfield/\#getTextInputFormat) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputFormat-java.lang.String) angegebene Textformat an und speichert den Wert in [getResult()](../../com.aspose.words/formfield/\#getResult) / [setResult(java.lang.String)](../../com.aspose.words/formfield/\#setResult-java.lang.String). |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exportiert den Inhalt des Knotens in einen String unter Verwendung der angegebenen Speicheroptionen. |
| [toString(int saveFormat)](#toString-int) |  |
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Akzeptiert einen Besucher.

 **Remarks:** 

Ruft [DocumentVisitor.visitFormField(com.aspose.words.FormField)](../../com.aspose.words/documentvisitor/\#visitFormField-com.aspose.words.FormField) auf.

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Der Besucher, der den Knoten besuchen wird. |

**Returns:**
boolean – false, falls der Besucher die Aufzählung stoppen möchte.
### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean}
```
public Node deepClone(boolean isCloneChildren)
```


Erstellt ein Duplikat des Knotens.

 **Remarks:** 

Diese Methode dient als Kopierkonstruktor für Knoten. Der geklonte Knoten hat keinen übergeordneten Knoten, gehört jedoch zum selben Dokument wie der ursprüngliche Knoten.

Diese Methode führt immer eine tiefe Kopie des Knotens aus. Der Parameter isCloneChildren gibt an, ob ebenfalls alle Kindknoten kopiert werden sollen.

 **Examples:** 

Zeigt, wie ein zusammengesetzter Knoten geklont wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| isCloneChildren | boolean | True, um den Unterbaum unter dem angegebenen Knoten rekursiv zu klonen; false, um nur den Knoten selbst zu klonen. |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned node.
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### getAncestor(int ancestorType) {#getAncestor-int}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class}
```
public CompositeNode getAncestor(Class ancestorType)
```


Ermittelt den ersten Vorfahren des angegebenen Objekttyps.

 **Remarks:** 

Der Ancestor-Typ stimmt überein, wenn er gleich ancestorType ist oder von ancestorType abgeleitet ist.

 **Examples:** 

Zeigt, wie man herausfindet, ob Tabellen verschachtelt sind.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| ancestorType | java.lang.Class | Der Objekttyp des abzurufenden Ancestors. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.
### getCalculateOnExit() {#getCalculateOnExit}
```
public boolean getCalculateOnExit()
```


True, wenn Verweise auf das angegebene Formularfeld automatisch aktualisiert werden, sobald das Feld verlassen wird.

 **Remarks:** 

Das Festlegen von [getCalculateOnExit()](../../com.aspose.words/formfield/\#getCalculateOnExit) / [setCalculateOnExit(boolean)](../../com.aspose.words/formfield/\#setCalculateOnExit-boolean) wirkt sich nur auf das Verhalten des Formularfelds aus, wenn das Dokument in Microsoft Word geöffnet wird. Aspose.Words aktualisiert niemals Verweise auf das Formularfeld.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getCheckBoxSize() {#getCheckBoxSize}
```
public double getCheckBoxSize()
```


Ermittelt die Größe des Kontrollkästchens in Punkten. Wirkt nur, wenn [isCheckBoxExactSize()](../../com.aspose.words/formfield/\#isCheckBoxExactSize) / [isCheckBoxExactSize(boolean)](../../com.aspose.words/formfield/\#isCheckBoxExactSize-boolean) true ist.

 **Remarks:** 

Nur für ein Kontrollkästchen-Formularfeld anwendbar.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
double - Die Größe des Kontrollkästchens in Punkten.
### getChecked() {#getChecked}
```
public boolean getChecked()
```


Ermittelt den aktivierten Status des Kontrollkästchen-Formularfelds. Der Standardwert für diese Eigenschaft ist false.

 **Remarks:** 

Nur für ein Kontrollkästchen-Formularfeld anwendbar.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
boolean - Der aktivierte Status des Kontrollkästchen-Formularfelds.
### getCustomNodeId() {#getCustomNodeId}
```
public int getCustomNodeId()
```


Gibt eine benutzerdefinierte Knotenkennung an.

 **Remarks:** 

Standardwert ist 0.

Dieser Bezeichner kann beliebig gesetzt und verwendet werden. Zum Beispiel als Schlüssel, um externe Daten abzurufen.

Wichtiger Hinweis: Der angegebene Wert wird nicht in einer Ausgabedatei gespeichert und existiert nur während der Lebensdauer des Knotens.

 **Examples:** 

Zeigt, wie man die Sammlung von Kindknoten eines zusammengesetzten Knotens durchläuft.

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
int - Der entsprechende int-Wert.
### getDefault() {#getDefault}
```
public boolean getDefault()
```


Ermittelt den Standardwert des Kontrollkästchen-Formularfelds. Der Standardwert für diese Eigenschaft ist false.

 **Remarks:** 

Nur für ein Kontrollkästchen-Formularfeld anwendbar.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
boolean - Der Standardwert des Kontrollkästchen-Formularfelds.
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Ermittelt das Dokument, zu dem dieser Knoten gehört.

 **Remarks:** 

Der Knoten gehört immer zu einem Dokument, selbst wenn er gerade erst erstellt wurde und noch nicht zum Baum hinzugefügt wurde oder wenn er aus dem Baum entfernt wurde.

 **Examples:** 

Zeigt, wie man einen Knoten erstellt und sein zugehöriges Dokument festlegt.

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
### getDropDownItems() {#getDropDownItems}
```
public DropDownItemCollection getDropDownItems()
```


Stellt Zugriff auf die Elemente eines Dropdown-Formularfelds bereit.

 **Remarks:** 

Microsoft Word erlaubt maximal 25 Elemente in einem Dropdown-Formularfeld.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
[DropDownItemCollection](../../com.aspose.words/dropdownitemcollection/) - The corresponding [DropDownItemCollection](../../com.aspose.words/dropdownitemcollection/) value.
### getDropDownSelectedIndex() {#getDropDownSelectedIndex}
```
public int getDropDownSelectedIndex()
```


Ermittelt den Index, der das aktuell ausgewählte Element in einem Dropdown-Formularfeld angibt.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
int - Der Index, der das aktuell ausgewählte Element in einem Dropdown-Formularfeld angibt.
### getEnabled() {#getEnabled}
```
public boolean getEnabled()
```


True, wenn ein Formularfeld aktiviert ist.

 **Remarks:** 

Wenn ein Formularfeld aktiviert ist, können seine Inhalte geändert werden, während das Formular ausgefüllt wird.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getEntryMacro() {#getEntryMacro}
```
public String getEntryMacro()
```


Ermittelt den Namen eines Eingabe-Makros für das Formularfeld.

 **Remarks:** 

Das Eingabemakro wird ausgeführt, wenn das Formularfeld in Microsoft Word den Fokus erhält.

Microsoft Word erlaubt Zeichenketten mit höchstens 32 Zeichen.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
java.lang.String - Ein Eingabemakro-Name für das Formularfeld.
### getExitMacro() {#getExitMacro}
```
public String getExitMacro()
```


Ermittelt den Namen eines Beendigungs-Makros für das Formularfeld.

 **Remarks:** 

Das Ausgangsmakro wird ausgeführt, wenn das Formularfeld in Microsoft Word den Fokus verliert.

Microsoft Word erlaubt Zeichenketten mit höchstens 32 Zeichen.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
java.lang.String - Ein Ausgangsmakro-Name für das Formularfeld.
### getFont() {#getFont}
```
public Font getFont()
```


Stellt Zugriff auf die Schriftformatierung dieses Objekts bereit.

 **Examples:** 

Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.

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
### getHelpText() {#getHelpText}
```
public String getHelpText()
```


Ermittelt den Text, der in einer Meldungsbox angezeigt wird, wenn das Formularfeld den Fokus hat und der Benutzer F1 drückt.

 **Remarks:** 

Wenn die [getOwnHelp()](../../com.aspose.words/formfield/\#getOwnHelp) / [setOwnHelp(boolean)](../../com.aspose.words/formfield/\#setOwnHelp-boolean) Eigenschaft auf true gesetzt ist, gibt [getHelpText()](../../com.aspose.words/formfield/\#getHelpText) / [setHelpText(java.lang.String)](../../com.aspose.words/formfield/\#setHelpText-java.lang.String) den Textzeichenkettenwert an. Wenn die [getOwnHelp()](../../com.aspose.words/formfield/\#getOwnHelp) / [setOwnHelp(boolean)](../../com.aspose.words/formfield/\#setOwnHelp-boolean) auf false gesetzt ist, gibt [getHelpText()](../../com.aspose.words/formfield/\#getHelpText) / [setHelpText(java.lang.String)](../../com.aspose.words/formfield/\#setHelpText-java.lang.String) den Namen eines AutoText-Eintrags an, der Hilfetext für das Formularfeld enthält.

Microsoft Word erlaubt Zeichenketten mit höchstens 255 Zeichen.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
java.lang.String - Der Text, der in einer Meldungsbox angezeigt wird, wenn das Formularfeld den Fokus hat und der Benutzer F1 drückt.
### getMaxLength() {#getMaxLength}
```
public int getMaxLength()
```


Maximale Länge für das Textfeld. Null, wenn die Länge nicht begrenzt ist.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
int - Der entsprechende int-Wert.
### getName() {#getName}
```
public String getName()
```


Ermittelt den Namen des Formularfelds.

 **Remarks:** 

Microsoft Word erlaubt Zeichenketten mit höchstens 20 Zeichen.

 **Examples:** 

Zeigt, wie man ein Kombinationsfeld einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Please select a fruit: ");

 // Insert a combo box which will allow a user to choose an option from a collection of strings.
 FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"Apple", "Banana", "Cherry"}, 0);

 Assert.assertEquals("MyComboBox", comboBox.getName());
 Assert.assertEquals(FieldType.FIELD_FORM_DROP_DOWN, comboBox.getType());
 Assert.assertEquals("Apple", comboBox.getResult());

 // The form field will appear in the form of a "select" html tag.
 doc.save(getArtifactsDir() + "FormFields.Create.html");
 
```

**Returns:**
java.lang.String - Der Name des Formularfeldes.
### getNextSibling() {#getNextSibling}
```
public Node getNextSibling()
```


Ermittelt den Knoten, der unmittelbar auf diesen Knoten folgt.

 **Remarks:** 

Wenn es keinen nächsten Knoten gibt, wird ein  null  zurückgegeben.

 **Examples:** 

Zeigt, wie man den Baum von Kindknoten eines zusammengesetzten Knotens durchläuft.

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

Zeigt, wie man die Eigenschaft NextSibling eines Knotens verwendet, um seine unmittelbaren Kinder zu enumerieren.

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


Gibt [NodeType.FORM\_FIELD](../../com.aspose.words/nodetype/\#FORM-FIELD) zurück.

 **Examples:** 

Zeigt, wie man den Baum von Kindknoten eines zusammengesetzten Knotens durchläuft.

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
int - [NodeType.FORM\_FIELD](../../com.aspose.words/nodetype/\#FORM-FIELD). Der zurückgegebene Wert ist einer der [NodeType](../../com.aspose.words/nodetype/) Konstanten.
### getOwnHelp() {#getOwnHelp}
```
public boolean getOwnHelp()
```


Gibt die Quelle des Textes an, der in einer Meldungsbox angezeigt wird, wenn ein Formularfeld den Fokus hat und der Benutzer F1 drückt.

 **Remarks:** 

Wenn true, wird der Text angezeigt, der durch die [getHelpText()](../../com.aspose.words/formfield/\#getHelpText) / [setHelpText(java.lang.String)](../../com.aspose.words/formfield/\#setHelpText-java.lang.String) Eigenschaft angegeben wird. Wenn false, wird der Text im AutoText-Eintrag angezeigt, der durch die [getHelpText()](../../com.aspose.words/formfield/\#getHelpText) / [setHelpText(java.lang.String)](../../com.aspose.words/formfield/\#setHelpText-java.lang.String) Eigenschaft angegeben wird.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getOwnStatus() {#getOwnStatus}
```
public boolean getOwnStatus()
```


Gibt die Quelle des Textes an, der in der Statusleiste angezeigt wird, wenn ein Formularfeld den Fokus hat.

 **Remarks:** 

Wenn true, wird der Text angezeigt, der durch die [getStatusText()](../../com.aspose.words/formfield/\#getStatusText) / [setStatusText(java.lang.String)](../../com.aspose.words/formfield/\#setStatusText-java.lang.String) Eigenschaft angegeben wird. Wenn false, wird der Text des AutoText-Eintrags angezeigt, der durch die [getStatusText()](../../com.aspose.words/formfield/\#getStatusText) / [setStatusText(java.lang.String)](../../com.aspose.words/formfield/\#setStatusText-java.lang.String) Eigenschaft angegeben wird.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getParentNode() {#getParentNode}
```
public CompositeNode getParentNode()
```


Ermittelt den unmittelbaren übergeordneten Knoten dieses Knotens.

 **Remarks:** 

Wenn ein Knoten gerade erstellt wurde und noch nicht zum Baum hinzugefügt wurde, oder wenn er aus dem Baum entfernt wurde, ist der übergeordnete Knoten  null .

 **Examples:** 

Zeigt, wie man auf den übergeordneten Knoten eines Knotens zugreift.

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

Zeigt, wie man einen Knoten erstellt und sein zugehöriges Dokument festlegt.

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


Ruft das übergeordnete [Paragraph](../../com.aspose.words/paragraph/) dieses Knotens ab.

 **Examples:** 

Zeigt, wie der Revisionstyp eines Inline‑Knotens ermittelt wird.

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
### getPreviousSibling() {#getPreviousSibling}
```
public Node getPreviousSibling()
```


Ermittelt den Knoten, der unmittelbar vor diesem Knoten liegt.

 **Remarks:** 

Wenn es keinen vorhergehenden Knoten gibt, wird ein  null  zurückgegeben.

 **Examples:** 

Zeigt, wie man Methoden von Node und CompositeNode verwendet, um einen Abschnitt vor dem letzten Abschnitt im Dokument zu entfernen.

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


Gibt ein [Range](../../com.aspose.words/range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist.

 **Examples:** 

Zeigt, wie man alle Knoten aus einem Bereich löscht.

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
### getResult() {#getResult}
```
public String getResult()
```


Ermittelt eine Zeichenkette, die das Ergebnis dieses Formularfelds darstellt.

 **Remarks:** 

Für ein Textformularfeld ist das Ergebnis der Text, der im Feld steht.

Für ein Kontrollkästchen-Formularfeld kann das Ergebnis "1" oder "0" sein, um geprüft bzw. ungeprüft anzuzeigen.

Für ein Dropdown-Formularfeld ist das Ergebnis die im Dropdown ausgewählte Zeichenkette.

Das Festlegen von [getResult()](../../com.aspose.words/formfield/\#getResult) / [setResult(java.lang.String)](../../com.aspose.words/formfield/\#setResult-java.lang.String) für ein Textformularfeld wendet das in [getTextInputFormat()](../../com.aspose.words/formfield/\#getTextInputFormat) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputFormat-java.lang.String) angegebene Textformat nicht an. Wenn Sie einen Wert festlegen und das Format anwenden möchten, verwenden Sie die Methode [setTextInputValue(java.lang.Object)](../../com.aspose.words/formfield/\#setTextInputValue-java.lang.Object).

Für ein Textformularfeld wird der Wert von [getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String) angewendet, wenn der Wert null ist.

 **Examples:** 

Zeigt, wie man ein Kombinationsfeld einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Please select a fruit: ");

 // Insert a combo box which will allow a user to choose an option from a collection of strings.
 FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"Apple", "Banana", "Cherry"}, 0);

 Assert.assertEquals("MyComboBox", comboBox.getName());
 Assert.assertEquals(FieldType.FIELD_FORM_DROP_DOWN, comboBox.getType());
 Assert.assertEquals("Apple", comboBox.getResult());

 // The form field will appear in the form of a "select" html tag.
 doc.save(getArtifactsDir() + "FormFields.Create.html");
 
```

**Returns:**
java.lang.String - Eine Zeichenkette, die das Ergebnis dieses Formularfeldes darstellt.
### getStatusText() {#getStatusText}
```
public String getStatusText()
```


Ermittelt den Text, der in der Statusleiste angezeigt wird, wenn ein Formularfeld den Fokus hat.

 **Remarks:** 

Wenn die Eigenschaft [getOwnStatus()](../../com.aspose.words/formfield/\#getOwnStatus) / [setOwnStatus(boolean)](../../com.aspose.words/formfield/\#setOwnStatus-boolean) auf true gesetzt ist, gibt die Eigenschaft [getStatusText()](../../com.aspose.words/formfield/\#getStatusText) / [setStatusText(java.lang.String)](../../com.aspose.words/formfield/\#setStatusText-java.lang.String) den Text für die Statusleiste an. Wenn die Eigenschaft [getOwnStatus()](../../com.aspose.words/formfield/\#getOwnStatus) / [setOwnStatus(boolean)](../../com.aspose.words/formfield/\#setOwnStatus-boolean) auf false gesetzt ist, gibt die Eigenschaft [getStatusText()](../../com.aspose.words/formfield/\#getStatusText) / [setStatusText(java.lang.String)](../../com.aspose.words/formfield/\#setStatusText-java.lang.String) den Namen eines AutoText‑Eintrags an, der den Statusleisten‑Text für das Formularfeld enthält.

Microsoft Word erlaubt Zeichenketten mit höchstens 138 Zeichen.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
java.lang.String - Der Text, der in der Statusleiste angezeigt wird, wenn ein Formularfeld den Fokus hat.
### getText() {#getText}
```
public String getText()
```


Ermittelt das Sonderzeichen, das dieser Knoten darstellt.

 **Examples:** 

Zeigt, wie man eine DocumentVisitor‑Implementierung verwendet, um allen versteckten Inhalt aus einem Dokument zu entfernen.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Returns:**
java.lang.String - Die Zeichenkette, die das Zeichen enthält, das dieser Knoten darstellt.
### getTextInputDefault() {#getTextInputDefault}
```
public String getTextInputDefault()
```


Ermittelt die Standardzeichenkette oder einen Berechnungsausdruck eines Textformularfelds.

 **Remarks:** 

Die Bedeutung dieser Eigenschaft hängt vom Wert der Eigenschaft [getTextInputType()](../../com.aspose.words/formfield/\#getTextInputType) / [setTextInputType(int)](../../com.aspose.words/formfield/\#setTextInputType-int) ab.

Wenn [getTextInputType()](../../com.aspose.words/formfield/\#getTextInputType) / [setTextInputType(int)](../../com.aspose.words/formfield/\#setTextInputType-int) [TextFormFieldType.REGULAR](../../com.aspose.words/textformfieldtype/\#REGULAR) oder [TextFormFieldType.NUMBER](../../com.aspose.words/textformfieldtype/\#NUMBER) ist, gibt diese Zeichenkette die Standardzeichenkette für das Textformularfeld an. Diese Zeichenkette ist der Inhalt, den Microsoft Word im Dokument anzeigt, wenn das Formularfeld leer ist.

When [getTextInputType()](../../com.aspose.words/formfield/\#getTextInputType) / [setTextInputType(int)](../../com.aspose.words/formfield/\#setTextInputType-int) is [TextFormFieldType.CALCULATED](../../com.aspose.words/textformfieldtype/\#CALCULATED), then this string holds the expression to be calculated. The expression needs to be a formula valid according to Microsoft Word formula field requirements. When you set a new expression using this property, Aspose.Words calculates the formula result automatically and inserts it into the form field.

Microsoft Word erlaubt Zeichenketten mit höchstens 255 Zeichen.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
java.lang.String - Die Standardzeichenkette oder ein Berechnungsausdruck eines Textformularfelds.
### getTextInputFormat() {#getTextInputFormat}
```
public String getTextInputFormat()
```


Ermittelt die Textformatierung für ein Textformularfeld.

 **Remarks:** 

Wenn das Textformularfeld regulären Text enthält, sind gültige Formatzeichenketten "", "UPPERCASE", "LOWERCASE", "FIRST CAPITAL" und "TITLE CASE". Die Zeichenketten sind nicht case‑sensitiv.

Wenn das Textformularfeld eine Zahl oder einen Datum/Uhrzeit‑Wert enthält, sind gültige Formatzeichenketten Zahlen‑ bzw. Datum‑ und Zeitformatzeichenketten.

Microsoft Word erlaubt Zeichenketten mit höchstens 64 Zeichen.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
java.lang.String - Die Textformatierung für ein Textformularfeld.
### getTextInputType() {#getTextInputType}
```
public int getTextInputType()
```


Ermittelt den Typ eines Textformularfelds.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
int - Der Typ eines Textformularfelds. Der zurückgegebene Wert ist einer der Konstanten von [TextFormFieldType](../../com.aspose.words/textformfieldtype/).
### getType() {#getType}
```
public int getType()
```


Gibt den Formularfeldtyp zurück.

 **Examples:** 

Zeigt, wie man ein Kombinationsfeld einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Please select a fruit: ");

 // Insert a combo box which will allow a user to choose an option from a collection of strings.
 FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"Apple", "Banana", "Cherry"}, 0);

 Assert.assertEquals("MyComboBox", comboBox.getName());
 Assert.assertEquals(FieldType.FIELD_FORM_DROP_DOWN, comboBox.getType());
 Assert.assertEquals("Apple", comboBox.getResult());

 // The form field will appear in the form of a "select" html tag.
 doc.save(getArtifactsDir() + "FormFields.Create.html");
 
```

**Returns:**
int - Der Formularfeldtyp. Der zurückgegebene Wert ist einer der Konstanten von [FieldType](../../com.aspose.words/fieldtype/).
### isCheckBoxExactSize() {#isCheckBoxExactSize}
```
public boolean isCheckBoxExactSize()
```


Ermittelt den booleschen Wert, der angibt, ob die Größe des Textfelds automatisch oder explizit festgelegt ist.

 **Remarks:** 

Nur für ein Kontrollkästchen-Formularfeld anwendbar.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
boolean - Der boolesche Wert, der angibt, ob die Größe des Textfeldes automatisch oder explizit festgelegt ist.
### isCheckBoxExactSize(boolean value) {#isCheckBoxExactSize-boolean}
```
public void isCheckBoxExactSize(boolean value)
```


Setzt den booleschen Wert, der angibt, ob die Größe des Textfelds automatisch oder explizit festgelegt ist.

 **Remarks:** 

Nur für ein Kontrollkästchen-Formularfeld anwendbar.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der boolesche Wert, der angibt, ob die Größe des Textfeldes automatisch oder explizit festgelegt ist. |

### isComposite() {#isComposite}
```
public boolean isComposite()
```


Gibt  true  zurück, wenn dieser Knoten andere Knoten enthalten kann. (197141,6)

 **Examples:** 

Zeigt, wie man den Baum von Kindknoten eines zusammengesetzten Knotens durchläuft.

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
boolean -  true  wenn dieser Knoten andere Knoten enthalten kann.
### isDeleteRevision() {#isDeleteRevision}
```
public boolean isDeleteRevision()
```


Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war.

 **Examples:** 

Zeigt, wie der Revisionstyp eines Inline‑Knotens ermittelt wird.

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
boolean - True, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war.
### isFormatRevision() {#isFormatRevision}
```
public boolean isFormatRevision()
```


Gibt true zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war.

 **Examples:** 

Zeigt, wie der Revisionstyp eines Inline‑Knotens ermittelt wird.

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
boolean - True, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war.
### isInsertRevision() {#isInsertRevision}
```
public boolean isInsertRevision()
```


Gibt true zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war.

 **Examples:** 

Zeigt, wie der Revisionstyp eines Inline‑Knotens ermittelt wird.

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
boolean - True, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war.
### isMoveFromRevision() {#isMoveFromRevision}
```
public boolean isMoveFromRevision()
```


Gibt  true  zurück, wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war.

 **Examples:** 

Zeigt, wie der Revisionstyp eines Inline‑Knotens ermittelt wird.

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
boolean -  true  wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war.
### isMoveToRevision() {#isMoveToRevision}
```
public boolean isMoveToRevision()
```


Gibt  true  zurück, wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war.

 **Examples:** 

Zeigt, wie der Revisionstyp eines Inline‑Knotens ermittelt wird.

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
boolean -  true  wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war.
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus.

 **Examples:** 

Zeigt, wie man den Knotbaum des Dokuments mit dem Preorder‑Durchlaufalgorithmus durchläuft und jede gefundene Form mit einem Bild löscht.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | Der oberste Knoten (Grenze) des Durchlaufs. |

**Returns:**
[Node](../../com.aspose.words/node/) - Next node in pre-order order. Null if reached the  rootNode .
### nodeTypeToString(int nodeType) {#nodeTypeToString-int}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus.

 **Examples:** 

Zeigt, wie man den Knotbaum des Dokuments mit dem Preorder‑Durchlaufalgorithmus durchläuft und jede gefundene Form mit einem Bild löscht.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | Der oberste Knoten (Grenze) des Durchlaufs. |

**Returns:**
[Node](../../com.aspose.words/node/) - Previous node in pre-order order. Null if reached the  rootNode .
### remove() {#remove}
```
public void remove()
```


Entfernt sich selbst vom übergeordneten Element.

 **Examples:** 

Zeigt, wie man alle Formen mit Bildern aus einem Dokument löscht.

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

Zeigt, wie man alle Kindknoten eines bestimmten Typs aus einem zusammengesetzten Knoten entfernt.

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

### removeField() {#removeField}
```
public void removeField()
```


Entfernt das gesamte Formularfeld, nicht nur das Sonderzeichen des Formularfelds.

 **Remarks:** 

Wenn ein Lesezeichen mit dem Formularfeld verknüpft ist, wird das Lesezeichen nicht entfernt.

 **Examples:** 

Zeigt, wie ein Formularfeld gelöscht wird.

```

 Document doc = new Document(getMyDir() + "Form fields.docx");

 FormField formField = doc.getRange().getFormFields().get(3);
 formField.removeField();
 
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

### setCalculateOnExit(boolean value) {#setCalculateOnExit-boolean}
```
public void setCalculateOnExit(boolean value)
```


True, wenn Verweise auf das angegebene Formularfeld automatisch aktualisiert werden, sobald das Feld verlassen wird.

 **Remarks:** 

Das Festlegen von [getCalculateOnExit()](../../com.aspose.words/formfield/\#getCalculateOnExit) / [setCalculateOnExit(boolean)](../../com.aspose.words/formfield/\#setCalculateOnExit-boolean) wirkt sich nur auf das Verhalten des Formularfelds aus, wenn das Dokument in Microsoft Word geöffnet wird. Aspose.Words aktualisiert niemals Verweise auf das Formularfeld.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setCheckBoxSize(double value) {#setCheckBoxSize-double}
```
public void setCheckBoxSize(double value)
```


Legt die Größe des Kontrollkästchens in Punkten fest. Wirkt nur, wenn [isCheckBoxExactSize()](../../com.aspose.words/formfield/\#isCheckBoxExactSize) / [isCheckBoxExactSize(boolean)](../../com.aspose.words/formfield/\#isCheckBoxExactSize-boolean) true ist.

 **Remarks:** 

Nur für ein Kontrollkästchen-Formularfeld anwendbar.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Die Größe des Kontrollkästchens in Punkten. |

### setChecked(boolean value) {#setChecked-boolean}
```
public void setChecked(boolean value)
```


Legt den aktivierten Status des Kontrollkästchen‑Formularfelds fest. Der Standardwert für diese Eigenschaft ist false.

 **Remarks:** 

Nur für ein Kontrollkästchen-Formularfeld anwendbar.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der aktivierte Status des Kontrollkästchen‑Formularfelds. |

### setCustomNodeId(int value) {#setCustomNodeId-int}
```
public void setCustomNodeId(int value)
```


Gibt eine benutzerdefinierte Knotenkennung an.

 **Remarks:** 

Standardwert ist 0.

Dieser Bezeichner kann beliebig gesetzt und verwendet werden. Zum Beispiel als Schlüssel, um externe Daten abzurufen.

Wichtiger Hinweis: Der angegebene Wert wird nicht in einer Ausgabedatei gespeichert und existiert nur während der Lebensdauer des Knotens.

 **Examples:** 

Zeigt, wie man die Sammlung von Kindknoten eines zusammengesetzten Knotens durchläuft.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setDefault(boolean value) {#setDefault-boolean}
```
public void setDefault(boolean value)
```


Legt den Standardwert des Kontrollkästchen‑Formularfelds fest. Der Standardwert für diese Eigenschaft ist false.

 **Remarks:** 

Nur für ein Kontrollkästchen-Formularfeld anwendbar.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der Standardwert des Kontrollkästchen‑Formularfelds. |

### setDropDownSelectedIndex(int value) {#setDropDownSelectedIndex-int}
```
public void setDropDownSelectedIndex(int value)
```


Legt den Index fest, der das aktuell ausgewählte Element in einem Dropdown-Formularfeld angibt.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der Index, der das aktuell ausgewählte Element in einem Dropdown‑Formularfeld angibt. |

### setEnabled(boolean value) {#setEnabled-boolean}
```
public void setEnabled(boolean value)
```


True, wenn ein Formularfeld aktiviert ist.

 **Remarks:** 

Wenn ein Formularfeld aktiviert ist, können seine Inhalte geändert werden, während das Formular ausgefüllt wird.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setEntryMacro(String value) {#setEntryMacro-java.lang.String}
```
public void setEntryMacro(String value)
```


Legt einen Eingabe-Makronamen für das Formularfeld fest.

 **Remarks:** 

Das Eingabemakro wird ausgeführt, wenn das Formularfeld in Microsoft Word den Fokus erhält.

Microsoft Word erlaubt Zeichenketten mit höchstens 32 Zeichen.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Ein Eintritt‑Makroname für das Formularfeld. |

### setExitMacro(String value) {#setExitMacro-java.lang.String}
```
public void setExitMacro(String value)
```


Legt einen Beendigungs-Makronamen für das Formularfeld fest.

 **Remarks:** 

Das Ausgangsmakro wird ausgeführt, wenn das Formularfeld in Microsoft Word den Fokus verliert.

Microsoft Word erlaubt Zeichenketten mit höchstens 32 Zeichen.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Ein Austritts‑Makroname für das Formularfeld. |

### setHelpText(String value) {#setHelpText-java.lang.String}
```
public void setHelpText(String value)
```


Legt den Text fest, der in einer Meldungsbox angezeigt wird, wenn das Formularfeld den Fokus hat und der Benutzer F1 drückt.

 **Remarks:** 

Wenn die [getOwnHelp()](../../com.aspose.words/formfield/\#getOwnHelp) / [setOwnHelp(boolean)](../../com.aspose.words/formfield/\#setOwnHelp-boolean) Eigenschaft auf true gesetzt ist, gibt [getHelpText()](../../com.aspose.words/formfield/\#getHelpText) / [setHelpText(java.lang.String)](../../com.aspose.words/formfield/\#setHelpText-java.lang.String) den Textzeichenkettenwert an. Wenn die [getOwnHelp()](../../com.aspose.words/formfield/\#getOwnHelp) / [setOwnHelp(boolean)](../../com.aspose.words/formfield/\#setOwnHelp-boolean) auf false gesetzt ist, gibt [getHelpText()](../../com.aspose.words/formfield/\#getHelpText) / [setHelpText(java.lang.String)](../../com.aspose.words/formfield/\#setHelpText-java.lang.String) den Namen eines AutoText-Eintrags an, der Hilfetext für das Formularfeld enthält.

Microsoft Word erlaubt Zeichenketten mit höchstens 255 Zeichen.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Text, der in einer Meldungsbox angezeigt wird, wenn das Formularfeld den Fokus hat und der Benutzer F1 drückt. |

### setMaxLength(int value) {#setMaxLength-int}
```
public void setMaxLength(int value)
```


Maximale Länge für das Textfeld. Null, wenn die Länge nicht begrenzt ist.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Legt den Namen des Formularfelds fest.

 **Remarks:** 

Microsoft Word erlaubt Zeichenketten mit höchstens 20 Zeichen.

 **Examples:** 

Zeigt, wie man ein Kombinationsfeld einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Please select a fruit: ");

 // Insert a combo box which will allow a user to choose an option from a collection of strings.
 FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"Apple", "Banana", "Cherry"}, 0);

 Assert.assertEquals("MyComboBox", comboBox.getName());
 Assert.assertEquals(FieldType.FIELD_FORM_DROP_DOWN, comboBox.getType());
 Assert.assertEquals("Apple", comboBox.getResult());

 // The form field will appear in the form of a "select" html tag.
 doc.save(getArtifactsDir() + "FormFields.Create.html");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Name des Formularfelds. |

### setOwnHelp(boolean value) {#setOwnHelp-boolean}
```
public void setOwnHelp(boolean value)
```


Gibt die Quelle des Textes an, der in einer Meldungsbox angezeigt wird, wenn ein Formularfeld den Fokus hat und der Benutzer F1 drückt.

 **Remarks:** 

Wenn true, wird der Text angezeigt, der durch die [getHelpText()](../../com.aspose.words/formfield/\#getHelpText) / [setHelpText(java.lang.String)](../../com.aspose.words/formfield/\#setHelpText-java.lang.String) Eigenschaft angegeben wird. Wenn false, wird der Text im AutoText-Eintrag angezeigt, der durch die [getHelpText()](../../com.aspose.words/formfield/\#getHelpText) / [setHelpText(java.lang.String)](../../com.aspose.words/formfield/\#setHelpText-java.lang.String) Eigenschaft angegeben wird.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setOwnStatus(boolean value) {#setOwnStatus-boolean}
```
public void setOwnStatus(boolean value)
```


Gibt die Quelle des Textes an, der in der Statusleiste angezeigt wird, wenn ein Formularfeld den Fokus hat.

 **Remarks:** 

Wenn true, wird der Text angezeigt, der durch die [getStatusText()](../../com.aspose.words/formfield/\#getStatusText) / [setStatusText(java.lang.String)](../../com.aspose.words/formfield/\#setStatusText-java.lang.String) Eigenschaft angegeben wird. Wenn false, wird der Text des AutoText-Eintrags angezeigt, der durch die [getStatusText()](../../com.aspose.words/formfield/\#getStatusText) / [setStatusText(java.lang.String)](../../com.aspose.words/formfield/\#setStatusText-java.lang.String) Eigenschaft angegeben wird.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Legt eine Zeichenkette fest, die das Ergebnis dieses Formularfelds darstellt.

 **Remarks:** 

Für ein Textformularfeld ist das Ergebnis der Text, der im Feld steht.

Für ein Kontrollkästchen-Formularfeld kann das Ergebnis "1" oder "0" sein, um geprüft bzw. ungeprüft anzuzeigen.

Für ein Dropdown-Formularfeld ist das Ergebnis die im Dropdown ausgewählte Zeichenkette.

Das Festlegen von [getResult()](../../com.aspose.words/formfield/\#getResult) / [setResult(java.lang.String)](../../com.aspose.words/formfield/\#setResult-java.lang.String) für ein Textformularfeld wendet das in [getTextInputFormat()](../../com.aspose.words/formfield/\#getTextInputFormat) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputFormat-java.lang.String) angegebene Textformat nicht an. Wenn Sie einen Wert festlegen und das Format anwenden möchten, verwenden Sie die Methode [setTextInputValue(java.lang.Object)](../../com.aspose.words/formfield/\#setTextInputValue-java.lang.Object).

Für ein Textformularfeld wird der Wert von [getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String) angewendet, wenn der Wert null ist.

 **Examples:** 

Zeigt, wie man ein Kombinationsfeld einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Please select a fruit: ");

 // Insert a combo box which will allow a user to choose an option from a collection of strings.
 FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"Apple", "Banana", "Cherry"}, 0);

 Assert.assertEquals("MyComboBox", comboBox.getName());
 Assert.assertEquals(FieldType.FIELD_FORM_DROP_DOWN, comboBox.getType());
 Assert.assertEquals("Apple", comboBox.getResult());

 // The form field will appear in the form of a "select" html tag.
 doc.save(getArtifactsDir() + "FormFields.Create.html");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Eine Zeichenkette, die das Ergebnis dieses Formularfelds darstellt. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| Wert | java.lang.Object |  |

### setStatusText(String value) {#setStatusText-java.lang.String}
```
public void setStatusText(String value)
```


Legt den Text fest, der in der Statusleiste angezeigt wird, wenn ein Formularfeld den Fokus hat.

 **Remarks:** 

Wenn die Eigenschaft [getOwnStatus()](../../com.aspose.words/formfield/\#getOwnStatus) / [setOwnStatus(boolean)](../../com.aspose.words/formfield/\#setOwnStatus-boolean) auf true gesetzt ist, gibt die Eigenschaft [getStatusText()](../../com.aspose.words/formfield/\#getStatusText) / [setStatusText(java.lang.String)](../../com.aspose.words/formfield/\#setStatusText-java.lang.String) den Text für die Statusleiste an. Wenn die Eigenschaft [getOwnStatus()](../../com.aspose.words/formfield/\#getOwnStatus) / [setOwnStatus(boolean)](../../com.aspose.words/formfield/\#setOwnStatus-boolean) auf false gesetzt ist, gibt die Eigenschaft [getStatusText()](../../com.aspose.words/formfield/\#getStatusText) / [setStatusText(java.lang.String)](../../com.aspose.words/formfield/\#setStatusText-java.lang.String) den Namen eines AutoText‑Eintrags an, der den Statusleisten‑Text für das Formularfeld enthält.

Microsoft Word erlaubt Zeichenketten mit höchstens 138 Zeichen.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Text, der in der Statusleiste angezeigt wird, wenn ein Formularfeld den Fokus hat. |

### setTextInputDefault(String value) {#setTextInputDefault-java.lang.String}
```
public void setTextInputDefault(String value)
```


Legt die Standardzeichenkette oder einen Berechnungsausdruck eines Textformularfelds fest.

 **Remarks:** 

Die Bedeutung dieser Eigenschaft hängt vom Wert der Eigenschaft [getTextInputType()](../../com.aspose.words/formfield/\#getTextInputType) / [setTextInputType(int)](../../com.aspose.words/formfield/\#setTextInputType-int) ab.

Wenn [getTextInputType()](../../com.aspose.words/formfield/\#getTextInputType) / [setTextInputType(int)](../../com.aspose.words/formfield/\#setTextInputType-int) [TextFormFieldType.REGULAR](../../com.aspose.words/textformfieldtype/\#REGULAR) oder [TextFormFieldType.NUMBER](../../com.aspose.words/textformfieldtype/\#NUMBER) ist, gibt diese Zeichenkette die Standardzeichenkette für das Textformularfeld an. Diese Zeichenkette ist der Inhalt, den Microsoft Word im Dokument anzeigt, wenn das Formularfeld leer ist.

When [getTextInputType()](../../com.aspose.words/formfield/\#getTextInputType) / [setTextInputType(int)](../../com.aspose.words/formfield/\#setTextInputType-int) is [TextFormFieldType.CALCULATED](../../com.aspose.words/textformfieldtype/\#CALCULATED), then this string holds the expression to be calculated. The expression needs to be a formula valid according to Microsoft Word formula field requirements. When you set a new expression using this property, Aspose.Words calculates the formula result automatically and inserts it into the form field.

Microsoft Word erlaubt Zeichenketten mit höchstens 255 Zeichen.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Die Standardzeichenfolge oder ein Berechnungsausdruck eines Textformularfelds. |

### setTextInputFormat(String value) {#setTextInputFormat-java.lang.String}
```
public void setTextInputFormat(String value)
```


Legt die Textformatierung für ein Textformularfeld fest.

 **Remarks:** 

Wenn das Textformularfeld regulären Text enthält, sind gültige Formatzeichenketten "", "UPPERCASE", "LOWERCASE", "FIRST CAPITAL" und "TITLE CASE". Die Zeichenketten sind nicht case‑sensitiv.

Wenn das Textformularfeld eine Zahl oder einen Datum/Uhrzeit‑Wert enthält, sind gültige Formatzeichenketten Zahlen‑ bzw. Datum‑ und Zeitformatzeichenketten.

Microsoft Word erlaubt Zeichenketten mit höchstens 64 Zeichen.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Die Textformatierung für ein Textformularfeld. |

### setTextInputType(int value) {#setTextInputType-int}
```
public void setTextInputType(int value)
```


Legt den Typ eines Textformularfelds fest.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der Typ eines Textformularfelds. Der Wert muss einer der [TextFormFieldType](../../com.aspose.words/textformfieldtype/) Konstanten sein. |

### setTextInputValue(Object newValue) {#setTextInputValue-java.lang.Object}
```
public void setTextInputValue(Object newValue)
```


Wendet das in [getTextInputFormat()](../../com.aspose.words/formfield/\#getTextInputFormat) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputFormat-java.lang.String) angegebene Textformat an und speichert den Wert in [getResult()](../../com.aspose.words/formfield/\#getResult) / [setResult(java.lang.String)](../../com.aspose.words/formfield/\#setResult-java.lang.String).

 **Remarks:** 

Der [getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String) Wert wird angewendet, wenn  newValue  null ist.

 **Examples:** 

Zeigt, wie verschiedene Arten von Formularfeldern in ein Dokument eingefügt und mit einer DocumentVisitor-Implementierung verarbeitet werden.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| newValue | java.lang.Object | Kann eine Zeichenfolge, eine Zahl oder ein **DateTime** Objekt sein. |

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


Exportiert den Inhalt des Knotens in einen String unter Verwendung der angegebenen Speicheroptionen.

 **Examples:** 

Exportiert den Inhalt eines Knotens als String im HTML-Format.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Gibt die Optionen an, die steuern, wie der Knoten gespeichert wird. |

**Returns:**
java.lang.String - Der Inhalt des Knotens im angegebenen Format.
### toString(int saveFormat) {#toString-int}
```
public String toString(int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
