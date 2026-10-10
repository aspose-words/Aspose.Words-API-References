---
title: "EditorType"
linktitle: "EditorType"
second_title: "Aspose.Words для Java"
description: "Указывает набор возможных псевдонимов или групп редактирования, которые могут использоваться как псевдонимы для определения, разрешено ли текущему пользователю редактировать отдельный диапазон, определённый редактируемым диапазоном внутри документа в Java."
type: docs
weight: 183
url: /ru/java/com.aspose.words/editortype/
---

**Inheritance:**
java.lang.Object
```
public class EditorType
```

Указывает набор возможных псевдонимов (или групп редактирования), которые могут использоваться в качестве псевдонимов для определения, разрешено ли текущему пользователю редактировать отдельный диапазон, определённый редактируемым диапазоном в документе.

 **Examples:** 

Показывает, как ограничить права редактирования редактируемых диапазонов конкретной группой/пользователем.

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
## Поля

| Поле | Описание |
| --- | --- |
| [ADMINISTRATORS](#ADMINISTRATORS) | Указывает, что пользователи, связанные с группой Administrators, будут иметь право редактировать редактируемые диапазоны с использованием этого типа редактирования, когда защита документа включена. |
| [CONTRIBUTORS](#CONTRIBUTORS) | Указывает, что пользователи, связанные с группой Contributors, будут иметь право редактировать редактируемые диапазоны с использованием этого типа редактирования, когда защита документа включена. |
| [CURRENT](#CURRENT) | Указывает, что пользователи, связанные с текущей группой, будут иметь разрешение редактировать редактируемые диапазоны, используя этот тип редактирования, когда защита документа включена. |
| [DEFAULT](#DEFAULT) | То же, что и [UNSPECIFIED](../../com.aspose.words/editortype/\#UNSPECIFIED). |
| [EDITORS](#EDITORS) | Указывает, что пользователи, связанные с группой Editors, будут иметь разрешение редактировать редактируемые диапазоны, используя этот тип редактирования, когда защита документа включена. |
| [EVERYONE](#EVERYONE) | Указывает, что все пользователи, открывающие документ, будут иметь разрешение редактировать редактируемые диапазоны, используя этот тип редактирования, когда защита документа включена. |
| [NONE](#NONE) | Указывает, что ни один из пользователей, открывающих документ, не будет иметь разрешения редактировать редактируемые диапазоны, используя этот тип редактирования, когда защита документа включена. |
| [OWNERS](#OWNERS) | Указывает, что пользователи, связанные с группой Owners, будут иметь разрешение редактировать редактируемые диапазоны, используя этот тип редактирования, когда защита документа включена. |
| [UNSPECIFIED](#UNSPECIFIED) | Означает, что тип редактора не указан. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String editorTypeName)](#fromName-java.lang.String) |  |
| [getName(int editorType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int editorType)](#toString-int) |  |
### ADMINISTRATORS {#ADMINISTRATORS}
```
public static int ADMINISTRATORS
```


Указывает, что пользователи, связанные с группой Administrators, будут иметь право редактировать редактируемые диапазоны с использованием этого типа редактирования, когда защита документа включена.

### CONTRIBUTORS {#CONTRIBUTORS}
```
public static int CONTRIBUTORS
```


Указывает, что пользователи, связанные с группой Contributors, будут иметь право редактировать редактируемые диапазоны с использованием этого типа редактирования, когда защита документа включена.

### CURRENT {#CURRENT}
```
public static int CURRENT
```


Указывает, что пользователи, связанные с текущей группой, будут иметь разрешение редактировать редактируемые диапазоны, используя этот тип редактирования, когда защита документа включена.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


То же, что и [UNSPECIFIED](../../com.aspose.words/editortype/\#UNSPECIFIED).

### EDITORS {#EDITORS}
```
public static int EDITORS
```


Указывает, что пользователи, связанные с группой Editors, будут иметь разрешение редактировать редактируемые диапазоны, используя этот тип редактирования, когда защита документа включена.

### EVERYONE {#EVERYONE}
```
public static int EVERYONE
```


Указывает, что все пользователи, открывающие документ, будут иметь разрешение редактировать редактируемые диапазоны, используя этот тип редактирования, когда защита документа включена.

### NONE {#NONE}
```
public static int NONE
```


Указывает, что ни один из пользователей, открывающих документ, не будет иметь разрешения редактировать редактируемые диапазоны, используя этот тип редактирования, когда защита документа включена.

### OWNERS {#OWNERS}
```
public static int OWNERS
```


Указывает, что пользователи, связанные с группой Owners, будут иметь разрешение редактировать редактируемые диапазоны, используя этот тип редактирования, когда защита документа включена.

### UNSPECIFIED {#UNSPECIFIED}
```
public static int UNSPECIFIED
```


Означает, что тип редактора не указан.

### length {#length}
```
public static int length
```


### fromName(String editorTypeName) {#fromName-java.lang.String}
```
public static int fromName(String editorTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| editorTypeName | java.lang.String |  |

**Returns:**
int
### getName(int editorType) {#getName-int}
```
public static String getName(int editorType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| editorType | int |  |

**Returns:**
java.lang.String
