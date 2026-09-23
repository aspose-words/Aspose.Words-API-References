---
title: "EditorType"
linktitle: "EditorType"
second_title: "Aspose.Words per Java"
description: "Specifica l'insieme di possibili alias o gruppi di modifica che possono essere usati come alias per determinare se all'utente corrente è consentito modificare un singolo intervallo definito da un intervallo modificabile all'interno di un documento in Java."
type: docs
weight: 183
url: /it/java/com.aspose.words/editortype/
---

**Inheritance:**
java.lang.Object
```
public class EditorType
```

Specifica l'insieme di alias possibili (o gruppi di modifica) che possono essere usati come alias per determinare se l'utente corrente può modificare un singolo intervallo definito da un intervallo modificabile all'interno di un documento.

 **Examples:** 

Mostra come limitare i diritti di modifica degli intervalli modificabili a un gruppo/utente specifico.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [ADMINISTRATORS](#ADMINISTRATORS) | Specifica che gli utenti associati al gruppo Amministratori potranno modificare gli intervalli modificabili usando questo tipo di modifica quando la protezione del documento è abilitata. |
| [CONTRIBUTORS](#CONTRIBUTORS) | Specifica che gli utenti associati al gruppo Collaboratori potranno modificare gli intervalli modificabili usando questo tipo di modifica quando la protezione del documento è abilitata. |
| [CURRENT](#CURRENT) | Specifica che gli utenti associati al gruppo Current potranno modificare le aree modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| [DEFAULT](#DEFAULT) | Come [UNSPECIFIED](../../com.aspose.words/editortype/\#UNSPECIFIED). |
| [EDITORS](#EDITORS) | Specifica che gli utenti associati al gruppo Editors potranno modificare le aree modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| [EVERYONE](#EVERYONE) | Specifica che tutti gli utenti che aprono il documento potranno modificare le aree modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| [NONE](#NONE) | Specifica che nessuno degli utenti che aprono il documento potrà modificare le aree modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| [OWNERS](#OWNERS) | Specifica che gli utenti associati al gruppo Owners potranno modificare le aree modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| [UNSPECIFIED](#UNSPECIFIED) | Indica che il tipo di editor non è specificato. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String editorTypeName)](#fromName-java.lang.String) |  |
| [getName(int editorType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int editorType)](#toString-int) |  |
### ADMINISTRATORS {#ADMINISTRATORS}
```
public static int ADMINISTRATORS
```


Specifica che gli utenti associati al gruppo Amministratori potranno modificare gli intervalli modificabili usando questo tipo di modifica quando la protezione del documento è abilitata.

### CONTRIBUTORS {#CONTRIBUTORS}
```
public static int CONTRIBUTORS
```


Specifica che gli utenti associati al gruppo Collaboratori potranno modificare gli intervalli modificabili usando questo tipo di modifica quando la protezione del documento è abilitata.

### CURRENT {#CURRENT}
```
public static int CURRENT
```


Specifica che gli utenti associati al gruppo Current potranno modificare le aree modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Come [UNSPECIFIED](../../com.aspose.words/editortype/\#UNSPECIFIED).

### EDITORS {#EDITORS}
```
public static int EDITORS
```


Specifica che gli utenti associati al gruppo Editors potranno modificare le aree modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata.

### EVERYONE {#EVERYONE}
```
public static int EVERYONE
```


Specifica che tutti gli utenti che aprono il documento potranno modificare le aree modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata.

### NONE {#NONE}
```
public static int NONE
```


Specifica che nessuno degli utenti che aprono il documento potrà modificare le aree modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata.

### OWNERS {#OWNERS}
```
public static int OWNERS
```


Specifica che gli utenti associati al gruppo Owners potranno modificare le aree modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata.

### UNSPECIFIED {#UNSPECIFIED}
```
public static int UNSPECIFIED
```


Indica che il tipo di editor non è specificato.

### length {#length}
```
public static int length
```


### fromName(String editorTypeName) {#fromName-java.lang.String}
```
public static int fromName(String editorTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| editorTypeName | java.lang.String |  |

**Returns:**
int
### getName(int editorType) {#getName-int}
```
public static String getName(int editorType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| editorType | int |  |

**Returns:**
java.lang.String
