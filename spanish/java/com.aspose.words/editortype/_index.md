---
title: "EditorType"
linktitle: "EditorType"
second_title: "Aspose.Words para Java"
description: "Especifica el conjunto de alias o grupos de edición posibles que pueden usarse como alias para determinar si al usuario actual se le permitirá editar un rango único definido por un rango editable dentro de un documento en Java."
type: docs
weight: 183
url: /es/java/com.aspose.words/editortype/
---

**Inheritance:**
java.lang.Object
```
public class EditorType
```

Especifica el conjunto de alias posibles (o grupos de edición) que pueden usarse como alias para determinar si al usuario actual se le permite editar un rango único definido por un rango editable dentro de un documento.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [ADMINISTRATORS](#ADMINISTRATORS) | Especifica que los usuarios asociados al grupo Administradores podrán editar rangos editables usando este tipo de edición cuando la protección del documento está habilitada. |
| [CONTRIBUTORS](#CONTRIBUTORS) | Especifica que los usuarios asociados al grupo Contribuyentes podrán editar rangos editables usando este tipo de edición cuando la protección del documento está habilitada. |
| [CURRENT](#CURRENT) | Especifica que los usuarios asociados al grupo Actual podrán editar los rangos editables usando este tipo de edición cuando la protección del documento está habilitada. |
| [DEFAULT](#DEFAULT) | Lo mismo que [UNSPECIFIED](../../com.aspose.words/editortype/\#UNSPECIFIED). |
| [EDITORS](#EDITORS) | Especifica que los usuarios asociados al grupo Editores podrán editar los rangos editables usando este tipo de edición cuando la protección del documento está habilitada. |
| [EVERYONE](#EVERYONE) | Especifica que todos los usuarios que abran el documento podrán editar los rangos editables usando este tipo de edición cuando la protección del documento está habilitada. |
| [NONE](#NONE) | Especifica que ninguno de los usuarios que abran el documento podrá editar los rangos editables usando este tipo de edición cuando la protección del documento está habilitada. |
| [OWNERS](#OWNERS) | Especifica que los usuarios asociados al grupo Propietarios podrán editar los rangos editables usando este tipo de edición cuando la protección del documento está habilitada. |
| [UNSPECIFIED](#UNSPECIFIED) | Indica que el tipo de editor no está especificado. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String editorTypeName)](#fromName-java.lang.String) |  |
| [getName(int editorType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int editorType)](#toString-int) |  |
### ADMINISTRATORS {#ADMINISTRATORS}
```
public static int ADMINISTRATORS
```


Especifica que los usuarios asociados al grupo Administradores podrán editar rangos editables usando este tipo de edición cuando la protección del documento está habilitada.

### CONTRIBUTORS {#CONTRIBUTORS}
```
public static int CONTRIBUTORS
```


Especifica que los usuarios asociados al grupo Contribuyentes podrán editar rangos editables usando este tipo de edición cuando la protección del documento está habilitada.

### CURRENT {#CURRENT}
```
public static int CURRENT
```


Especifica que los usuarios asociados al grupo Actual podrán editar los rangos editables usando este tipo de edición cuando la protección del documento está habilitada.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Lo mismo que [UNSPECIFIED](../../com.aspose.words/editortype/\#UNSPECIFIED).

### EDITORS {#EDITORS}
```
public static int EDITORS
```


Especifica que los usuarios asociados al grupo Editores podrán editar los rangos editables usando este tipo de edición cuando la protección del documento está habilitada.

### EVERYONE {#EVERYONE}
```
public static int EVERYONE
```


Especifica que todos los usuarios que abran el documento podrán editar los rangos editables usando este tipo de edición cuando la protección del documento está habilitada.

### NONE {#NONE}
```
public static int NONE
```


Especifica que ninguno de los usuarios que abran el documento podrá editar los rangos editables usando este tipo de edición cuando la protección del documento está habilitada.

### OWNERS {#OWNERS}
```
public static int OWNERS
```


Especifica que los usuarios asociados al grupo Propietarios podrán editar los rangos editables usando este tipo de edición cuando la protección del documento está habilitada.

### UNSPECIFIED {#UNSPECIFIED}
```
public static int UNSPECIFIED
```


Indica que el tipo de editor no está especificado.

### length {#length}
```
public static int length
```


### fromName(String editorTypeName) {#fromName-java.lang.String}
```
public static int fromName(String editorTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| editorTypeName | java.lang.String |  |

**Returns:**
int
### getName(int editorType) {#getName-int}
```
public static String getName(int editorType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| editorType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int editorType) {#toString-int}
```
public static String toString(int editorType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| editorType | int |  |

**Returns:**
java.lang.String
