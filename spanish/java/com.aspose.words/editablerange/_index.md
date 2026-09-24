---
title: "EditableRange"
linktitle: "EditableRange"
second_title: "Aspose.Words para Java"
description: "Representa un rango editable único en Java."
type: docs
weight: 179
url: /es/java/com.aspose.words/editablerange/
---

**Inheritance:**
java.lang.Object
```
public class EditableRange
```

Representa un rango editable único.

Para obtener más información, visite el artículo de documentación [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_].

 **Remarks:** 

[EditableRange](../../com.aspose.words/editablerange/) is a "facade" object that encapsulates two nodes [getEditableRangeStart()](../../com.aspose.words/editablerange/\#getEditableRangeStart) and [getEditableRangeEnd()](../../com.aspose.words/editablerange/\#getEditableRangeEnd) in a document tree and allows to work with an editable range as a single object.

 **Examples:** 

Muestra cómo trabajar con un rango editable.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
         " we cannot edit this paragraph without the password.");

 // Editable ranges allow us to leave parts of protected documents open for editing.
 EditableRangeStart editableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph is inside an editable range, and can be edited.");
 EditableRangeEnd editableRangeEnd = builder.endEditableRange();

 // A well-formed editable range has a start node, and end node.
 // These nodes have matching IDs and encompass editable nodes.
 EditableRange editableRange = editableRangeStart.getEditableRange();

 Assert.assertEquals(editableRangeStart.getId(), editableRange.getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getId());

 // Different parts of the editable range link to each other.
 Assert.assertEquals(editableRangeStart.getId(), editableRange.getEditableRangeStart().getId());
 Assert.assertEquals(editableRangeStart.getId(), editableRangeEnd.getEditableRangeStart().getId());
 Assert.assertEquals(editableRange.getId(), editableRangeStart.getEditableRange().getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getEditableRangeEnd().getId());

 // We can access the node types of each part like this. The editable range itself is not a node,
 // but an entity which consists of a start, an end, and their enclosed contents.
 Assert.assertEquals(NodeType.EDITABLE_RANGE_START, editableRangeStart.getNodeType());
 Assert.assertEquals(NodeType.EDITABLE_RANGE_END, editableRangeEnd.getNodeType());

 builder.writeln("This paragraph is outside the editable range, and cannot be edited.");

 doc.save(getArtifactsDir() + "EditableRange.CreateAndRemove.docx");

 // Remove an editable range. All the nodes that were inside the range will remain intact.
 editableRange.remove();
 
```

Muestra cómo limitar los derechos de edición de los rangos editables a un grupo/usuario específico.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     doc.protect(ProtectionType.READ_ONLY, "MyPassword");

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
             " we cannot edit this paragraph without the password.");

     // When we write-protect documents, editable ranges allow us to pick specific areas that users may edit.
     // There are two mutually exclusive ways to narrow down the list of allowed editors.
     // 1 -  Specify a user:
     EditableRange editableRange = builder.startEditableRange().getEditableRange();
     editableRange.setSingleUser("john.doe@myoffice.com");
     builder.writeln(MessageFormat.format("This paragraph is inside the first editable range, can only be edited by {0}.", editableRange.getSingleUser()));
     builder.endEditableRange();

     Assert.assertEquals(EditorType.UNSPECIFIED, editableRange.getEditorGroup());

     // 2 -  Specify a group that allowed users are associated with:
     editableRange = builder.startEditableRange().getEditableRange();
     editableRange.setEditorGroup(EditorType.ADMINISTRATORS);
     builder.writeln(MessageFormat.format("This paragraph is inside the first editable range, can only be edited by {0}.", editableRange.getEditorGroup()));
     builder.endEditableRange();

     Assert.assertEquals("", editableRange.getSingleUser());

     builder.writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

     // Print details and contents of every editable range in the document.
     EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

     doc.accept(editableRangePrinter);

     System.out.println(editableRangePrinter.toText());
 }

 /// 
 /// Collects properties and contents of visited editable ranges in a string.
 /// 
 public static class EditableRangePrinter extends DocumentVisitor {
     public EditableRangePrinter() {
         mBuilder = new StringBuilder();
     }

     public String toText() {
         return mBuilder.toString();
     }

     public void reset() {
         mBuilder.setLength(0);
         mInsideEditableRange = false;
     }

     /// 
     /// Called when an EditableRangeStart node is encountered in the document.
     /// 
     public int visitEditableRangeStart(EditableRangeStart editableRangeStart) {
         mBuilder.append(" -- Editable range found! -- ");
         mBuilder.append("\tID:\t\t" + editableRangeStart.getId());
         if (editableRangeStart.getEditableRange().getSingleUser().equals(""))
             mBuilder.append("\tGroup:\t" + editableRangeStart.getEditableRange().getEditorGroup());
         else
             mBuilder.append("\tUser:\t" + editableRangeStart.getEditableRange().getSingleUser());
         mBuilder.append("\tContents:");

         mInsideEditableRange = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when an EditableRangeEnd node is encountered in the document.
     /// 
     public int visitEditableRangeEnd(final EditableRangeEnd editableRangeEnd) {
         mBuilder.append(" -- End of editable range -- " + "\r\n");

         mInsideEditableRange = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document. This visitor only records runs that are inside editable ranges.
     /// 
     public int visitRun(final Run run) {
         if (mInsideEditableRange) {
             mBuilder.append("\t\"" + run.getText() + "\"" + "\r\n");
         }

         return VisitorAction.CONTINUE;
     }

     private boolean mInsideEditableRange;
     private final StringBuilder mBuilder;
 }
 
```


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Métodos

| Método | Descripción |
| --- | --- |
| [getEditableRangeEnd()](#getEditableRangeEnd) | Obtiene el nodo que representa el final del rango editable. |
| [getEditableRangeStart()](#getEditableRangeStart) | Obtiene el nodo que representa el inicio del rango editable. |
| [getEditorGroup()](#getEditorGroup) | Obtiene un alias (o grupo de edición) que se utilizará para determinar si el usuario actual tiene permiso para editar este rango editable. |
| [getId()](#getId) | Obtiene el identificador del rango editable. |
| [getSingleUser()](#getSingleUser) | Obtiene el usuario único para el rango editable. |
| [remove()](#remove) | Elimina el rango editable del documento. |
| [setEditorGroup(int value)](#setEditorGroup-int) | Establece un alias (o grupo de edición) que se utilizará para determinar si el usuario actual tiene permiso para editar este rango editable. |
| [setSingleUser(String value)](#setSingleUser-java.lang.String) | Establece el usuario único para el rango editable. |
### getEditableRangeEnd() {#getEditableRangeEnd}
```
public EditableRangeEnd getEditableRangeEnd()
```


Obtiene el nodo que representa el final del rango editable.

 **Examples:** 

Muestra cómo trabajar con un rango editable.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
         " we cannot edit this paragraph without the password.");

 // Editable ranges allow us to leave parts of protected documents open for editing.
 EditableRangeStart editableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph is inside an editable range, and can be edited.");
 EditableRangeEnd editableRangeEnd = builder.endEditableRange();

 // A well-formed editable range has a start node, and end node.
 // These nodes have matching IDs and encompass editable nodes.
 EditableRange editableRange = editableRangeStart.getEditableRange();

 Assert.assertEquals(editableRangeStart.getId(), editableRange.getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getId());

 // Different parts of the editable range link to each other.
 Assert.assertEquals(editableRangeStart.getId(), editableRange.getEditableRangeStart().getId());
 Assert.assertEquals(editableRangeStart.getId(), editableRangeEnd.getEditableRangeStart().getId());
 Assert.assertEquals(editableRange.getId(), editableRangeStart.getEditableRange().getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getEditableRangeEnd().getId());

 // We can access the node types of each part like this. The editable range itself is not a node,
 // but an entity which consists of a start, an end, and their enclosed contents.
 Assert.assertEquals(NodeType.EDITABLE_RANGE_START, editableRangeStart.getNodeType());
 Assert.assertEquals(NodeType.EDITABLE_RANGE_END, editableRangeEnd.getNodeType());

 builder.writeln("This paragraph is outside the editable range, and cannot be edited.");

 doc.save(getArtifactsDir() + "EditableRange.CreateAndRemove.docx");

 // Remove an editable range. All the nodes that were inside the range will remain intact.
 editableRange.remove();
 
```

**Returns:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend/) - The node that represents the end of the editable range.
### getEditableRangeStart() {#getEditableRangeStart}
```
public EditableRangeStart getEditableRangeStart()
```


Obtiene el nodo que representa el inicio del rango editable.

 **Examples:** 

Muestra cómo trabajar con un rango editable.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
         " we cannot edit this paragraph without the password.");

 // Editable ranges allow us to leave parts of protected documents open for editing.
 EditableRangeStart editableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph is inside an editable range, and can be edited.");
 EditableRangeEnd editableRangeEnd = builder.endEditableRange();

 // A well-formed editable range has a start node, and end node.
 // These nodes have matching IDs and encompass editable nodes.
 EditableRange editableRange = editableRangeStart.getEditableRange();

 Assert.assertEquals(editableRangeStart.getId(), editableRange.getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getId());

 // Different parts of the editable range link to each other.
 Assert.assertEquals(editableRangeStart.getId(), editableRange.getEditableRangeStart().getId());
 Assert.assertEquals(editableRangeStart.getId(), editableRangeEnd.getEditableRangeStart().getId());
 Assert.assertEquals(editableRange.getId(), editableRangeStart.getEditableRange().getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getEditableRangeEnd().getId());

 // We can access the node types of each part like this. The editable range itself is not a node,
 // but an entity which consists of a start, an end, and their enclosed contents.
 Assert.assertEquals(NodeType.EDITABLE_RANGE_START, editableRangeStart.getNodeType());
 Assert.assertEquals(NodeType.EDITABLE_RANGE_END, editableRangeEnd.getNodeType());

 builder.writeln("This paragraph is outside the editable range, and cannot be edited.");

 doc.save(getArtifactsDir() + "EditableRange.CreateAndRemove.docx");

 // Remove an editable range. All the nodes that were inside the range will remain intact.
 editableRange.remove();
 
```

**Returns:**
[EditableRangeStart](../../com.aspose.words/editablerangestart/) - The node that represents the start of the editable range.
### getEditorGroup() {#getEditorGroup}
```
public int getEditorGroup()
```


Obtiene un alias (o grupo de edición) que se utilizará para determinar si el usuario actual tiene permiso para editar este rango editable.

 **Remarks:** 

El usuario único y el grupo de editores no pueden establecerse simultáneamente para el rango editable específico; si se establece uno, el otro se borrará.

 **Examples:** 

Muestra cómo crear rangos editables anidados.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only, " +
         "we cannot edit this paragraph without the password.");

 // Create two nested editable ranges.
 EditableRangeStart outerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 EditableRangeStart innerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

 // Currently, the document builder's node insertion cursor is in more than one ongoing editable range.
 // When we want to end an editable range in this situation,
 // we need to specify which of the ranges we wish to end by passing its EditableRangeStart node.
 builder.endEditableRange(innerEditableRangeStart);

 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 builder.endEditableRange(outerEditableRangeStart);

 builder.writeln("This paragraph is outside any editable ranges, and cannot be edited.");

 // If a region of text has two overlapping editable ranges with specified groups,
 // the combined group of users excluded by both groups are prevented from editing it.
 outerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.EVERYONE);
 innerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.CONTRIBUTORS);

 doc.save(getArtifactsDir() + "EditableRange.Nested.docx");
 
```

Muestra cómo limitar los derechos de edición de los rangos editables a un grupo/usuario específico.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     doc.protect(ProtectionType.READ_ONLY, "MyPassword");

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
             " we cannot edit this paragraph without the password.");

     // When we write-protect documents, editable ranges allow us to pick specific areas that users may edit.
     // There are two mutually exclusive ways to narrow down the list of allowed editors.
     // 1 -  Specify a user:
     EditableRange editableRange = builder.startEditableRange().getEditableRange();
     editableRange.setSingleUser("john.doe@myoffice.com");
     builder.writeln(MessageFormat.format("This paragraph is inside the first editable range, can only be edited by {0}.", editableRange.getSingleUser()));
     builder.endEditableRange();

     Assert.assertEquals(EditorType.UNSPECIFIED, editableRange.getEditorGroup());

     // 2 -  Specify a group that allowed users are associated with:
     editableRange = builder.startEditableRange().getEditableRange();
     editableRange.setEditorGroup(EditorType.ADMINISTRATORS);
     builder.writeln(MessageFormat.format("This paragraph is inside the first editable range, can only be edited by {0}.", editableRange.getEditorGroup()));
     builder.endEditableRange();

     Assert.assertEquals("", editableRange.getSingleUser());

     builder.writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

     // Print details and contents of every editable range in the document.
     EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

     doc.accept(editableRangePrinter);

     System.out.println(editableRangePrinter.toText());
 }

 /// 
 /// Collects properties and contents of visited editable ranges in a string.
 /// 
 public static class EditableRangePrinter extends DocumentVisitor {
     public EditableRangePrinter() {
         mBuilder = new StringBuilder();
     }

     public String toText() {
         return mBuilder.toString();
     }

     public void reset() {
         mBuilder.setLength(0);
         mInsideEditableRange = false;
     }

     /// 
     /// Called when an EditableRangeStart node is encountered in the document.
     /// 
     public int visitEditableRangeStart(EditableRangeStart editableRangeStart) {
         mBuilder.append(" -- Editable range found! -- ");
         mBuilder.append("\tID:\t\t" + editableRangeStart.getId());
         if (editableRangeStart.getEditableRange().getSingleUser().equals(""))
             mBuilder.append("\tGroup:\t" + editableRangeStart.getEditableRange().getEditorGroup());
         else
             mBuilder.append("\tUser:\t" + editableRangeStart.getEditableRange().getSingleUser());
         mBuilder.append("\tContents:");

         mInsideEditableRange = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when an EditableRangeEnd node is encountered in the document.
     /// 
     public int visitEditableRangeEnd(final EditableRangeEnd editableRangeEnd) {
         mBuilder.append(" -- End of editable range -- " + "\r\n");

         mInsideEditableRange = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document. This visitor only records runs that are inside editable ranges.
     /// 
     public int visitRun(final Run run) {
         if (mInsideEditableRange) {
             mBuilder.append("\t\"" + run.getText() + "\"" + "\r\n");
         }

         return VisitorAction.CONTINUE;
     }

     private boolean mInsideEditableRange;
     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
int - Un alias (o grupo de edición) que se utilizará para determinar si el usuario actual tiene permiso para editar este rango editable. El valor devuelto es una de las constantes [EditorType](../../com.aspose.words/editortype/).
### getId() {#getId}
```
public int getId()
```


Obtiene el identificador del rango editable.

 **Remarks:** 

La región debe delimitarse usando [getEditableRangeStart()](../../com.aspose.words/editablerange/\#getEditableRangeStart) y [getEditableRangeEnd()](../../com.aspose.words/editablerange/\#getEditableRangeEnd)

Se supone que los identificadores de rangos editables son únicos en todo un documento y Aspose.Words mantiene automáticamente los identificadores de rangos editables al cargar, guardar y combinar documentos.

 **Examples:** 

Muestra cómo trabajar con un rango editable.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
         " we cannot edit this paragraph without the password.");

 // Editable ranges allow us to leave parts of protected documents open for editing.
 EditableRangeStart editableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph is inside an editable range, and can be edited.");
 EditableRangeEnd editableRangeEnd = builder.endEditableRange();

 // A well-formed editable range has a start node, and end node.
 // These nodes have matching IDs and encompass editable nodes.
 EditableRange editableRange = editableRangeStart.getEditableRange();

 Assert.assertEquals(editableRangeStart.getId(), editableRange.getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getId());

 // Different parts of the editable range link to each other.
 Assert.assertEquals(editableRangeStart.getId(), editableRange.getEditableRangeStart().getId());
 Assert.assertEquals(editableRangeStart.getId(), editableRangeEnd.getEditableRangeStart().getId());
 Assert.assertEquals(editableRange.getId(), editableRangeStart.getEditableRange().getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getEditableRangeEnd().getId());

 // We can access the node types of each part like this. The editable range itself is not a node,
 // but an entity which consists of a start, an end, and their enclosed contents.
 Assert.assertEquals(NodeType.EDITABLE_RANGE_START, editableRangeStart.getNodeType());
 Assert.assertEquals(NodeType.EDITABLE_RANGE_END, editableRangeEnd.getNodeType());

 builder.writeln("This paragraph is outside the editable range, and cannot be edited.");

 doc.save(getArtifactsDir() + "EditableRange.CreateAndRemove.docx");

 // Remove an editable range. All the nodes that were inside the range will remain intact.
 editableRange.remove();
 
```

**Returns:**
int - El identificador del rango editable.
### getSingleUser() {#getSingleUser}
```
public String getSingleUser()
```


Obtiene el usuario único para el rango editable.

 **Remarks:** 

Este editor puede almacenarse en una de las siguientes formas:

DOMAIN\\Username - para usuarios cuyo acceso será autenticado usando las credenciales de dominio del usuario actual.

user@domain.com - para usuarios cuyo acceso será autenticado usando la dirección de correo electrónico del usuario como credenciales.

user - para usuarios cuyo acceso será autenticado usando las credenciales de la máquina del usuario actual.

El usuario único y el grupo de editores no pueden establecerse simultáneamente para el rango editable específico; si se establece uno, el otro se borrará.

 **Examples:** 

Muestra cómo limitar los derechos de edición de los rangos editables a un grupo/usuario específico.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     doc.protect(ProtectionType.READ_ONLY, "MyPassword");

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
             " we cannot edit this paragraph without the password.");

     // When we write-protect documents, editable ranges allow us to pick specific areas that users may edit.
     // There are two mutually exclusive ways to narrow down the list of allowed editors.
     // 1 -  Specify a user:
     EditableRange editableRange = builder.startEditableRange().getEditableRange();
     editableRange.setSingleUser("john.doe@myoffice.com");
     builder.writeln(MessageFormat.format("This paragraph is inside the first editable range, can only be edited by {0}.", editableRange.getSingleUser()));
     builder.endEditableRange();

     Assert.assertEquals(EditorType.UNSPECIFIED, editableRange.getEditorGroup());

     // 2 -  Specify a group that allowed users are associated with:
     editableRange = builder.startEditableRange().getEditableRange();
     editableRange.setEditorGroup(EditorType.ADMINISTRATORS);
     builder.writeln(MessageFormat.format("This paragraph is inside the first editable range, can only be edited by {0}.", editableRange.getEditorGroup()));
     builder.endEditableRange();

     Assert.assertEquals("", editableRange.getSingleUser());

     builder.writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

     // Print details and contents of every editable range in the document.
     EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

     doc.accept(editableRangePrinter);

     System.out.println(editableRangePrinter.toText());
 }

 /// 
 /// Collects properties and contents of visited editable ranges in a string.
 /// 
 public static class EditableRangePrinter extends DocumentVisitor {
     public EditableRangePrinter() {
         mBuilder = new StringBuilder();
     }

     public String toText() {
         return mBuilder.toString();
     }

     public void reset() {
         mBuilder.setLength(0);
         mInsideEditableRange = false;
     }

     /// 
     /// Called when an EditableRangeStart node is encountered in the document.
     /// 
     public int visitEditableRangeStart(EditableRangeStart editableRangeStart) {
         mBuilder.append(" -- Editable range found! -- ");
         mBuilder.append("\tID:\t\t" + editableRangeStart.getId());
         if (editableRangeStart.getEditableRange().getSingleUser().equals(""))
             mBuilder.append("\tGroup:\t" + editableRangeStart.getEditableRange().getEditorGroup());
         else
             mBuilder.append("\tUser:\t" + editableRangeStart.getEditableRange().getSingleUser());
         mBuilder.append("\tContents:");

         mInsideEditableRange = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when an EditableRangeEnd node is encountered in the document.
     /// 
     public int visitEditableRangeEnd(final EditableRangeEnd editableRangeEnd) {
         mBuilder.append(" -- End of editable range -- " + "\r\n");

         mInsideEditableRange = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document. This visitor only records runs that are inside editable ranges.
     /// 
     public int visitRun(final Run run) {
         if (mInsideEditableRange) {
             mBuilder.append("\t\"" + run.getText() + "\"" + "\r\n");
         }

         return VisitorAction.CONTINUE;
     }

     private boolean mInsideEditableRange;
     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
java.lang.String - El único usuario para el rango editable.
### remove() {#remove}
```
public void remove()
```


Elimina el rango editable del documento. No elimina el contenido dentro del rango editable.

 **Examples:** 

Muestra cómo trabajar con un rango editable.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
         " we cannot edit this paragraph without the password.");

 // Editable ranges allow us to leave parts of protected documents open for editing.
 EditableRangeStart editableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph is inside an editable range, and can be edited.");
 EditableRangeEnd editableRangeEnd = builder.endEditableRange();

 // A well-formed editable range has a start node, and end node.
 // These nodes have matching IDs and encompass editable nodes.
 EditableRange editableRange = editableRangeStart.getEditableRange();

 Assert.assertEquals(editableRangeStart.getId(), editableRange.getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getId());

 // Different parts of the editable range link to each other.
 Assert.assertEquals(editableRangeStart.getId(), editableRange.getEditableRangeStart().getId());
 Assert.assertEquals(editableRangeStart.getId(), editableRangeEnd.getEditableRangeStart().getId());
 Assert.assertEquals(editableRange.getId(), editableRangeStart.getEditableRange().getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getEditableRangeEnd().getId());

 // We can access the node types of each part like this. The editable range itself is not a node,
 // but an entity which consists of a start, an end, and their enclosed contents.
 Assert.assertEquals(NodeType.EDITABLE_RANGE_START, editableRangeStart.getNodeType());
 Assert.assertEquals(NodeType.EDITABLE_RANGE_END, editableRangeEnd.getNodeType());

 builder.writeln("This paragraph is outside the editable range, and cannot be edited.");

 doc.save(getArtifactsDir() + "EditableRange.CreateAndRemove.docx");

 // Remove an editable range. All the nodes that were inside the range will remain intact.
 editableRange.remove();
 
```

### setEditorGroup(int value) {#setEditorGroup-int}
```
public void setEditorGroup(int value)
```


Establece un alias (o grupo de edición) que se utilizará para determinar si el usuario actual tiene permiso para editar este rango editable.

 **Remarks:** 

El usuario único y el grupo de editores no pueden establecerse simultáneamente para el rango editable específico; si se establece uno, el otro se borrará.

 **Examples:** 

Muestra cómo crear rangos editables anidados.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only, " +
         "we cannot edit this paragraph without the password.");

 // Create two nested editable ranges.
 EditableRangeStart outerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 EditableRangeStart innerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

 // Currently, the document builder's node insertion cursor is in more than one ongoing editable range.
 // When we want to end an editable range in this situation,
 // we need to specify which of the ranges we wish to end by passing its EditableRangeStart node.
 builder.endEditableRange(innerEditableRangeStart);

 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 builder.endEditableRange(outerEditableRangeStart);

 builder.writeln("This paragraph is outside any editable ranges, and cannot be edited.");

 // If a region of text has two overlapping editable ranges with specified groups,
 // the combined group of users excluded by both groups are prevented from editing it.
 outerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.EVERYONE);
 innerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.CONTRIBUTORS);

 doc.save(getArtifactsDir() + "EditableRange.Nested.docx");
 
```

Muestra cómo limitar los derechos de edición de los rangos editables a un grupo/usuario específico.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     doc.protect(ProtectionType.READ_ONLY, "MyPassword");

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
             " we cannot edit this paragraph without the password.");

     // When we write-protect documents, editable ranges allow us to pick specific areas that users may edit.
     // There are two mutually exclusive ways to narrow down the list of allowed editors.
     // 1 -  Specify a user:
     EditableRange editableRange = builder.startEditableRange().getEditableRange();
     editableRange.setSingleUser("john.doe@myoffice.com");
     builder.writeln(MessageFormat.format("This paragraph is inside the first editable range, can only be edited by {0}.", editableRange.getSingleUser()));
     builder.endEditableRange();

     Assert.assertEquals(EditorType.UNSPECIFIED, editableRange.getEditorGroup());

     // 2 -  Specify a group that allowed users are associated with:
     editableRange = builder.startEditableRange().getEditableRange();
     editableRange.setEditorGroup(EditorType.ADMINISTRATORS);
     builder.writeln(MessageFormat.format("This paragraph is inside the first editable range, can only be edited by {0}.", editableRange.getEditorGroup()));
     builder.endEditableRange();

     Assert.assertEquals("", editableRange.getSingleUser());

     builder.writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

     // Print details and contents of every editable range in the document.
     EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

     doc.accept(editableRangePrinter);

     System.out.println(editableRangePrinter.toText());
 }

 /// 
 /// Collects properties and contents of visited editable ranges in a string.
 /// 
 public static class EditableRangePrinter extends DocumentVisitor {
     public EditableRangePrinter() {
         mBuilder = new StringBuilder();
     }

     public String toText() {
         return mBuilder.toString();
     }

     public void reset() {
         mBuilder.setLength(0);
         mInsideEditableRange = false;
     }

     /// 
     /// Called when an EditableRangeStart node is encountered in the document.
     /// 
     public int visitEditableRangeStart(EditableRangeStart editableRangeStart) {
         mBuilder.append(" -- Editable range found! -- ");
         mBuilder.append("\tID:\t\t" + editableRangeStart.getId());
         if (editableRangeStart.getEditableRange().getSingleUser().equals(""))
             mBuilder.append("\tGroup:\t" + editableRangeStart.getEditableRange().getEditorGroup());
         else
             mBuilder.append("\tUser:\t" + editableRangeStart.getEditableRange().getSingleUser());
         mBuilder.append("\tContents:");

         mInsideEditableRange = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when an EditableRangeEnd node is encountered in the document.
     /// 
     public int visitEditableRangeEnd(final EditableRangeEnd editableRangeEnd) {
         mBuilder.append(" -- End of editable range -- " + "\r\n");

         mInsideEditableRange = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document. This visitor only records runs that are inside editable ranges.
     /// 
     public int visitRun(final Run run) {
         if (mInsideEditableRange) {
             mBuilder.append("\t\"" + run.getText() + "\"" + "\r\n");
         }

         return VisitorAction.CONTINUE;
     }

     private boolean mInsideEditableRange;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Un alias (o grupo de edición) que se utilizará para determinar si el usuario actual podrá editar este rango editable. El valor debe ser una de las constantes de [EditorType](../../com.aspose.words/editortype/). |

### setSingleUser(String value) {#setSingleUser-java.lang.String}
```
public void setSingleUser(String value)
```


Establece el usuario único para el rango editable.

 **Remarks:** 

Este editor puede almacenarse en una de las siguientes formas:

DOMAIN\\Username - para usuarios cuyo acceso será autenticado usando las credenciales de dominio del usuario actual.

user@domain.com - para usuarios cuyo acceso será autenticado usando la dirección de correo electrónico del usuario como credenciales.

user - para usuarios cuyo acceso será autenticado usando las credenciales de la máquina del usuario actual.

El usuario único y el grupo de editores no pueden establecerse simultáneamente para el rango editable específico; si se establece uno, el otro se borrará.

 **Examples:** 

Muestra cómo limitar los derechos de edición de los rangos editables a un grupo/usuario específico.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     doc.protect(ProtectionType.READ_ONLY, "MyPassword");

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
             " we cannot edit this paragraph without the password.");

     // When we write-protect documents, editable ranges allow us to pick specific areas that users may edit.
     // There are two mutually exclusive ways to narrow down the list of allowed editors.
     // 1 -  Specify a user:
     EditableRange editableRange = builder.startEditableRange().getEditableRange();
     editableRange.setSingleUser("john.doe@myoffice.com");
     builder.writeln(MessageFormat.format("This paragraph is inside the first editable range, can only be edited by {0}.", editableRange.getSingleUser()));
     builder.endEditableRange();

     Assert.assertEquals(EditorType.UNSPECIFIED, editableRange.getEditorGroup());

     // 2 -  Specify a group that allowed users are associated with:
     editableRange = builder.startEditableRange().getEditableRange();
     editableRange.setEditorGroup(EditorType.ADMINISTRATORS);
     builder.writeln(MessageFormat.format("This paragraph is inside the first editable range, can only be edited by {0}.", editableRange.getEditorGroup()));
     builder.endEditableRange();

     Assert.assertEquals("", editableRange.getSingleUser());

     builder.writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

     // Print details and contents of every editable range in the document.
     EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

     doc.accept(editableRangePrinter);

     System.out.println(editableRangePrinter.toText());
 }

 /// 
 /// Collects properties and contents of visited editable ranges in a string.
 /// 
 public static class EditableRangePrinter extends DocumentVisitor {
     public EditableRangePrinter() {
         mBuilder = new StringBuilder();
     }

     public String toText() {
         return mBuilder.toString();
     }

     public void reset() {
         mBuilder.setLength(0);
         mInsideEditableRange = false;
     }

     /// 
     /// Called when an EditableRangeStart node is encountered in the document.
     /// 
     public int visitEditableRangeStart(EditableRangeStart editableRangeStart) {
         mBuilder.append(" -- Editable range found! -- ");
         mBuilder.append("\tID:\t\t" + editableRangeStart.getId());
         if (editableRangeStart.getEditableRange().getSingleUser().equals(""))
             mBuilder.append("\tGroup:\t" + editableRangeStart.getEditableRange().getEditorGroup());
         else
             mBuilder.append("\tUser:\t" + editableRangeStart.getEditableRange().getSingleUser());
         mBuilder.append("\tContents:");

         mInsideEditableRange = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when an EditableRangeEnd node is encountered in the document.
     /// 
     public int visitEditableRangeEnd(final EditableRangeEnd editableRangeEnd) {
         mBuilder.append(" -- End of editable range -- " + "\r\n");

         mInsideEditableRange = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document. This visitor only records runs that are inside editable ranges.
     /// 
     public int visitRun(final Run run) {
         if (mInsideEditableRange) {
             mBuilder.append("\t\"" + run.getText() + "\"" + "\r\n");
         }

         return VisitorAction.CONTINUE;
     }

     private boolean mInsideEditableRange;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El único usuario para el rango editable. |

