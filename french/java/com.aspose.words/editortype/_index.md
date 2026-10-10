---
title: "EditorType"
linktitle: "EditorType"
second_title: "Aspose.Words pour Java"
description: "Spécifie l’ensemble des alias ou groupes d’édition possibles qui peuvent être utilisés comme alias pour déterminer si l’utilisateur actuel est autorisé à modifier une seule plage définie par une plage modifiable dans un document en Java."
type: docs
weight: 183
url: /fr/java/com.aspose.words/editortype/
---

**Inheritance:**
java.lang.Object
```
public class EditorType
```

Spécifie l'ensemble des alias possibles (ou groupes d'édition) pouvant être utilisés comme alias pour déterminer si l'utilisateur actuel est autorisé à modifier une plage unique définie par une plage modifiable dans un document.

 **Examples:** 

Montre comment limiter les droits de modification des plages éditables à un groupe/utilisateur spécifique.

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
## Champs

| Champ | Description |
| --- | --- |
| [ADMINISTRATORS](#ADMINISTRATORS) | Spécifie que les utilisateurs associés au groupe Administrators sont autorisés à modifier les plages modifiables en utilisant ce type d’édition lorsque la protection du document est activée. |
| [CONTRIBUTORS](#CONTRIBUTORS) | Spécifie que les utilisateurs associés au groupe Contributors sont autorisés à modifier les plages modifiables en utilisant ce type d’édition lorsque la protection du document est activée. |
| [CURRENT](#CURRENT) | Spécifie que les utilisateurs associés au groupe Current sont autorisés à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée. |
| [DEFAULT](#DEFAULT) | Identique à [UNSPECIFIED](../../com.aspose.words/editortype/\#UNSPECIFIED). |
| [EDITORS](#EDITORS) | Spécifie que les utilisateurs associés au groupe Editors sont autorisés à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée. |
| [EVERYONE](#EVERYONE) | Spécifie que tous les utilisateurs qui ouvrent le document sont autorisés à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée. |
| [NONE](#NONE) | Spécifie qu'aucun des utilisateurs qui ouvrent le document n'est autorisé à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée. |
| [OWNERS](#OWNERS) | Spécifie que les utilisateurs associés au groupe Owners sont autorisés à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée. |
| [UNSPECIFIED](#UNSPECIFIED) | Indique que le type d'éditeur n'est pas spécifié. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String editorTypeName)](#fromName-java.lang.String) |  |
| [getName(int editorType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int editorType)](#toString-int) |  |
### ADMINISTRATORS {#ADMINISTRATORS}
```
public static int ADMINISTRATORS
```


Spécifie que les utilisateurs associés au groupe Administrators sont autorisés à modifier les plages modifiables en utilisant ce type d’édition lorsque la protection du document est activée.

### CONTRIBUTORS {#CONTRIBUTORS}
```
public static int CONTRIBUTORS
```


Spécifie que les utilisateurs associés au groupe Contributors sont autorisés à modifier les plages modifiables en utilisant ce type d’édition lorsque la protection du document est activée.

### CURRENT {#CURRENT}
```
public static int CURRENT
```


Spécifie que les utilisateurs associés au groupe Current sont autorisés à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Identique à [UNSPECIFIED](../../com.aspose.words/editortype/\#UNSPECIFIED).

### EDITORS {#EDITORS}
```
public static int EDITORS
```


Spécifie que les utilisateurs associés au groupe Editors sont autorisés à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée.

### EVERYONE {#EVERYONE}
```
public static int EVERYONE
```


Spécifie que tous les utilisateurs qui ouvrent le document sont autorisés à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée.

### NONE {#NONE}
```
public static int NONE
```


Spécifie qu'aucun des utilisateurs qui ouvrent le document n'est autorisé à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée.

### OWNERS {#OWNERS}
```
public static int OWNERS
```


Spécifie que les utilisateurs associés au groupe Owners sont autorisés à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée.

### UNSPECIFIED {#UNSPECIFIED}
```
public static int UNSPECIFIED
```


Indique que le type d'éditeur n'est pas spécifié.

### length {#length}
```
public static int length
```


### fromName(String editorTypeName) {#fromName-java.lang.String}
```
public static int fromName(String editorTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| editorTypeName | java.lang.String |  |

**Returns:**
int
### getName(int editorType) {#getName-int}
```
public static String getName(int editorType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| editorType | int |  |

**Returns:**
java.lang.String
