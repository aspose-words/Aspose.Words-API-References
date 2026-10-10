---
title: "EditorType"
linktitle: "EditorType"
second_title: "Aspose.Words Java için"
description: "Java'da bir belge içinde düzenlenebilir bir aralık tarafından tanımlanan tek bir aralığı mevcut kullanıcının düzenleyip düzenleyemeyeceğini belirlemek için takma ad olarak kullanılabilecek olası takma adlar veya düzenleme grupları kümesini belirtir."
type: docs
weight: 183
url: /tr/java/com.aspose.words/editortype/
---

**Inheritance:**
java.lang.Object
```
public class EditorType
```

Belge içinde bir düzenlenebilir aralık tarafından tanımlanan tek bir aralığı düzenleme izni verilip verilmeyeceğini belirlemek için takma ad olarak kullanılabilecek olası takma adların (veya düzenleme gruplarının) kümesini belirtir.

 **Examples:** 

Düzenlenebilir aralıkların düzenleme haklarını belirli bir grup/kullanıcıyla sınırlamanın nasıl yapılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ADMINISTRATORS](#ADMINISTRATORS) | Belge koruması etkin olduğunda, Administrators grubuna bağlı kullanıcıların bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemelerine izin verileceğini belirtir. |
| [CONTRIBUTORS](#CONTRIBUTORS) | Belge koruması etkin olduğunda, Contributors grubuna bağlı kullanıcıların bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemelerine izin verileceğini belirtir. |
| [CURRENT](#CURRENT) | Belirtilen, Current grubuna ait kullanıcıların belge koruması etkin olduğunda bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemelerine izin verileceğini belirtir. |
| [DEFAULT](#DEFAULT) | Aynı [UNSPECIFIED](../../com.aspose.words/editortype/\#UNSPECIFIED). |
| [EDITORS](#EDITORS) | Belirtilen, Editors grubuna ait kullanıcıların belge koruması etkin olduğunda bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemelerine izin verileceğini belirtir. |
| [EVERYONE](#EVERYONE) | Belirtilen, belgeyi açan tüm kullanıcıların belge koruması etkin olduğunda bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemelerine izin verileceğini belirtir. |
| [NONE](#NONE) | Belirtilen, belgeyi açan hiçbir kullanıcının belge koruması etkin olduğunda bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemesine izin verilmeyeceğini belirtir. |
| [OWNERS](#OWNERS) | Belirtilen, Owners grubuna ait kullanıcıların belge koruması etkin olduğunda bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemelerine izin verileceğini belirtir. |
| [UNSPECIFIED](#UNSPECIFIED) | Düzenleyici türünün belirtilmediği anlamına gelir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String editorTypeName)](#fromName-java.lang.String) |  |
| [getName(int editorType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int editorType)](#toString-int) |  |
### ADMINISTRATORS {#ADMINISTRATORS}
```
public static int ADMINISTRATORS
```


Belge koruması etkin olduğunda, Administrators grubuna bağlı kullanıcıların bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemelerine izin verileceğini belirtir.

### CONTRIBUTORS {#CONTRIBUTORS}
```
public static int CONTRIBUTORS
```


Belge koruması etkin olduğunda, Contributors grubuna bağlı kullanıcıların bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemelerine izin verileceğini belirtir.

### CURRENT {#CURRENT}
```
public static int CURRENT
```


Belirtilen, Current grubuna ait kullanıcıların belge koruması etkin olduğunda bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemelerine izin verileceğini belirtir.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Aynı [UNSPECIFIED](../../com.aspose.words/editortype/\#UNSPECIFIED).

### EDITORS {#EDITORS}
```
public static int EDITORS
```


Belirtilen, Editors grubuna ait kullanıcıların belge koruması etkin olduğunda bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemelerine izin verileceğini belirtir.

### EVERYONE {#EVERYONE}
```
public static int EVERYONE
```


Belirtilen, belgeyi açan tüm kullanıcıların belge koruması etkin olduğunda bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemelerine izin verileceğini belirtir.

### NONE {#NONE}
```
public static int NONE
```


Belirtilen, belgeyi açan hiçbir kullanıcının belge koruması etkin olduğunda bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemesine izin verilmeyeceğini belirtir.

### OWNERS {#OWNERS}
```
public static int OWNERS
```


Belirtilen, Owners grubuna ait kullanıcıların belge koruması etkin olduğunda bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemelerine izin verileceğini belirtir.

### UNSPECIFIED {#UNSPECIFIED}
```
public static int UNSPECIFIED
```


Düzenleyici türünün belirtilmediği anlamına gelir.

### length {#length}
```
public static int length
```


### fromName(String editorTypeName) {#fromName-java.lang.String}
```
public static int fromName(String editorTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| editorTypeName | java.lang.String |  |

**Returns:**
int
### getName(int editorType) {#getName-int}
```
public static String getName(int editorType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| editorType | int |  |

**Returns:**
java.lang.String
