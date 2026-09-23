---
title: "EditorType"
linktitle: "EditorType"
second_title: "Aspose.Words für Java"
description: "Gibt die Menge möglicher Aliase oder Bearbeitungsgruppen an, die als Aliase verwendet werden können, um zu bestimmen, ob dem aktuellen Benutzer das Bearbeiten eines einzelnen, durch einen bearbeitbaren Bereich innerhalb eines Dokuments definierten Bereichs in Java erlaubt ist."
type: docs
weight: 183
url: /de/java/com.aspose.words/editortype/
---

**Inheritance:**
java.lang.Object
```
public class EditorType
```

Gibt die Menge möglicher Aliase (oder Bearbeitungsgruppen) an, die als Aliase verwendet werden können, um zu bestimmen, ob dem aktuellen Benutzer das Bearbeiten eines einzelnen, durch einen bearbeitbaren Bereich definierten Bereichs innerhalb eines Dokuments erlaubt ist.

 **Examples:** 

Zeigt, wie man die Bearbeitungsrechte von bearbeitbaren Bereichen auf eine bestimmte Gruppe/Benutzer beschränkt.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ADMINISTRATORS](#ADMINISTRATORS) | Gibt an, dass Benutzer, die der Gruppe Administrators zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist. |
| [CONTRIBUTORS](#CONTRIBUTORS) | Gibt an, dass Benutzer, die der Gruppe Contributors zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist. |
| [CURRENT](#CURRENT) | Gibt an, dass Benutzer, die der Gruppe Current zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist. |
| [DEFAULT](#DEFAULT) | Same as [UNSPECIFIED](../../com.aspose.words/editortype/\#UNSPECIFIED). |
| [EDITORS](#EDITORS) | Gibt an, dass Benutzer, die der Gruppe Editors zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist. |
| [EVERYONE](#EVERYONE) | Gibt an, dass alle Benutzer, die das Dokument öffnen, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist. |
| [NONE](#NONE) | Gibt an, dass keiner der Benutzer, die das Dokument öffnen, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist. |
| [OWNERS](#OWNERS) | Gibt an, dass Benutzer, die der Gruppe Owners zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist. |
| [UNSPECIFIED](#UNSPECIFIED) | Bedeutet, dass der Editor-Typ nicht angegeben ist. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String editorTypeName)](#fromName-java.lang.String) |  |
| [getName(int editorType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int editorType)](#toString-int) |  |
### ADMINISTRATORS {#ADMINISTRATORS}
```
public static int ADMINISTRATORS
```


Gibt an, dass Benutzer, die der Gruppe Administrators zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist.

### CONTRIBUTORS {#CONTRIBUTORS}
```
public static int CONTRIBUTORS
```


Gibt an, dass Benutzer, die der Gruppe Contributors zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist.

### CURRENT {#CURRENT}
```
public static int CURRENT
```


Gibt an, dass Benutzer, die der Gruppe Current zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Same as [UNSPECIFIED](../../com.aspose.words/editortype/\#UNSPECIFIED).

### EDITORS {#EDITORS}
```
public static int EDITORS
```


Gibt an, dass Benutzer, die der Gruppe Editors zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist.

### EVERYONE {#EVERYONE}
```
public static int EVERYONE
```


Gibt an, dass alle Benutzer, die das Dokument öffnen, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist.

### NONE {#NONE}
```
public static int NONE
```


Gibt an, dass keiner der Benutzer, die das Dokument öffnen, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist.

### OWNERS {#OWNERS}
```
public static int OWNERS
```


Gibt an, dass Benutzer, die der Gruppe Owners zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist.

### UNSPECIFIED {#UNSPECIFIED}
```
public static int UNSPECIFIED
```


Bedeutet, dass der Editor-Typ nicht angegeben ist.

### length {#length}
```
public static int length
```


### fromName(String editorTypeName) {#fromName-java.lang.String}
```
public static int fromName(String editorTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| editorTypeName | java.lang.String |  |

**Returns:**
int
### getName(int editorType) {#getName-int}
```
public static String getName(int editorType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| editorType | int |  |

**Returns:**
java.lang.String
