---
title: "EditorType"
linktitle: "EditorType"
second_title: "Aspose.Words لـ Java"
description: "يحدد مجموعة الأسماء المستعارة أو مجموعات التحرير الممكنة التي يمكن استخدامها كأسماء مستعارة لتحديد ما إذا كان يُسمح للمستخدم الحالي بتحرير نطاق واحد معرف بنطاق قابل للتحرير داخل مستند في Java."
type: docs
weight: 183
url: /ar/java/com.aspose.words/editortype/
---

**Inheritance:**
java.lang.Object
```
public class EditorType
```

يحدد مجموعة الأسماء المستعارة الممكنة (أو مجموعات التحرير) التي يمكن استخدامها كأسماء مستعارة لتحديد ما إذا كان يُسمح للمستخدم الحالي بتحرير نطاق واحد معرف بنطاق قابل للتحرير داخل المستند.

 **Examples:** 

يوضح كيفية تقييد حقوق التحرير للنطاقات القابلة للتحرير لمجموعة/مستخدم معين.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [ADMINISTRATORS](#ADMINISTRATORS) | يحدد أن المستخدمين المرتبطين بمجموعة المسؤولين يُسمح لهم بتحرير النطاقات القابلة للتحرير باستخدام هذا النوع من التحرير عندما تكون حماية المستند مفعلة. |
| [CONTRIBUTORS](#CONTRIBUTORS) | يحدد أن المستخدمين المرتبطين بمجموعة المساهمين يُسمح لهم بتحرير النطاقات القابلة للتحرير باستخدام هذا النوع من التحرير عندما تكون حماية المستند مفعلة. |
| [CURRENT](#CURRENT) | يحدد أن المستخدمين المرتبطين بمجموعة Current سيسمح لهم بتحرير النطاقات القابلة للتحرير باستخدام هذا النوع من التحرير عندما تكون حماية المستند مفعلة. |
| [DEFAULT](#DEFAULT) | نفس [UNSPECIFIED](../../com.aspose.words/editortype/\#UNSPECIFIED). |
| [EDITORS](#EDITORS) | يحدد أن المستخدمين المرتبطين بمجموعة Editors سيسمح لهم بتحرير النطاقات القابلة للتحرير باستخدام هذا النوع من التحرير عندما تكون حماية المستند مفعلة. |
| [EVERYONE](#EVERYONE) | يحدد أن جميع المستخدمين الذين يفتحون المستند سيسمح لهم بتحرير النطاقات القابلة للتحرير باستخدام هذا النوع من التحرير عندما تكون حماية المستند مفعلة. |
| [NONE](#NONE) | يحدد أنه لا يُسمح لأي من المستخدمين الذين يفتحون المستند بتحرير النطاقات القابلة للتحرير باستخدام هذا النوع من التحرير عندما تكون حماية المستند مفعلة. |
| [OWNERS](#OWNERS) | يحدد أن المستخدمين المرتبطين بمجموعة Owners سيسمح لهم بتحرير النطاقات القابلة للتحرير باستخدام هذا النوع من التحرير عندما تكون حماية المستند مفعلة. |
| [UNSPECIFIED](#UNSPECIFIED) | يعني أن نوع المحرر غير محدد. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String editorTypeName)](#fromName-java.lang.String) |  |
| [getName(int editorType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int editorType)](#toString-int) |  |
### ADMINISTRATORS {#ADMINISTRATORS}
```
public static int ADMINISTRATORS
```


يحدد أن المستخدمين المرتبطين بمجموعة المسؤولين يُسمح لهم بتحرير النطاقات القابلة للتحرير باستخدام هذا النوع من التحرير عندما تكون حماية المستند مفعلة.

### CONTRIBUTORS {#CONTRIBUTORS}
```
public static int CONTRIBUTORS
```


يحدد أن المستخدمين المرتبطين بمجموعة المساهمين يُسمح لهم بتحرير النطاقات القابلة للتحرير باستخدام هذا النوع من التحرير عندما تكون حماية المستند مفعلة.

### CURRENT {#CURRENT}
```
public static int CURRENT
```


يحدد أن المستخدمين المرتبطين بمجموعة Current سيسمح لهم بتحرير النطاقات القابلة للتحرير باستخدام هذا النوع من التحرير عندما تكون حماية المستند مفعلة.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


نفس [UNSPECIFIED](../../com.aspose.words/editortype/\#UNSPECIFIED).

### EDITORS {#EDITORS}
```
public static int EDITORS
```


يحدد أن المستخدمين المرتبطين بمجموعة Editors سيسمح لهم بتحرير النطاقات القابلة للتحرير باستخدام هذا النوع من التحرير عندما تكون حماية المستند مفعلة.

### EVERYONE {#EVERYONE}
```
public static int EVERYONE
```


يحدد أن جميع المستخدمين الذين يفتحون المستند سيسمح لهم بتحرير النطاقات القابلة للتحرير باستخدام هذا النوع من التحرير عندما تكون حماية المستند مفعلة.

### NONE {#NONE}
```
public static int NONE
```


يحدد أنه لا يُسمح لأي من المستخدمين الذين يفتحون المستند بتحرير النطاقات القابلة للتحرير باستخدام هذا النوع من التحرير عندما تكون حماية المستند مفعلة.

### OWNERS {#OWNERS}
```
public static int OWNERS
```


يحدد أن المستخدمين المرتبطين بمجموعة Owners سيسمح لهم بتحرير النطاقات القابلة للتحرير باستخدام هذا النوع من التحرير عندما تكون حماية المستند مفعلة.

### UNSPECIFIED {#UNSPECIFIED}
```
public static int UNSPECIFIED
```


يعني أن نوع المحرر غير محدد.

### length {#length}
```
public static int length
```


### fromName(String editorTypeName) {#fromName-java.lang.String}
```
public static int fromName(String editorTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| editorTypeName | java.lang.String |  |

**Returns:**
int
### getName(int editorType) {#getName-int}
```
public static String getName(int editorType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| editorType | int |  |

**Returns:**
java.lang.String
