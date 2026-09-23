---
title: "Forms2OleControlType"
linktitle: "Forms2OleControlType"
second_title: "Aspose.Words per Java"
description: "Enumera i tipi di controlli Forms 2.0 in Java."
type: docs
weight: 351
url: /it/java/com.aspose.words/forms2olecontroltype/
---

**Inheritance:**
java.lang.Object
```
public class Forms2OleControlType
```

Enumera i tipi di controlli Forms 2.0.

 **Examples:** 

Mostra come cambiare lo stato del controllo CheckBox.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 CheckBoxControl checkBoxControl = (CheckBoxControl)shape.getOleFormat().getOleControl();
 checkBoxControl.setChecked(true);

 Assert.assertEquals(true, checkBoxControl.getChecked());
 Assert.assertEquals(Forms2OleControlType.CHECK_BOX, checkBoxControl.getType());
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [CHECK_BOX](#CHECK-BOX) | Un controllo che consente all'utente di selezionare o deselezionare un'opzione. |
| [COMBO_BOX](#COMBO-BOX) | Un controllo che consente all'utente di selezionare un elemento da un elenco. |
| [COMMAND_BUTTON](#COMMAND-BUTTON) | Un pulsante che avvia un'azione quando viene cliccato. |
| [FORM](#FORM) | Un contenitore per altri controlli. |
| [FRAME](#FRAME) | Un controllo che raggruppa altri controlli. |
| [IMAGE](#IMAGE) | Un controllo che visualizza un'immagine. |
| [LABEL](#LABEL) | Un controllo che visualizza testo. |
| [LIST_BOX](#LIST-BOX) | Un controllo che visualizza un elenco di elementi. |
| [MULTI_PAGE](#MULTI-PAGE) | Un controllo che visualizza più pagine di contenuto. |
| [OPTION_BUTTON](#OPTION-BUTTON) | Un controllo pulsante di opzione. |
| [SCROLL_BAR](#SCROLL-BAR) | Un controllo che consente all'utente di scorrere il contenuto. |
| [SPIN_BUTTON](#SPIN-BUTTON) | Un controllo che consente all'utente di aumentare o diminuire un valore. |
| [TAB_STRIP](#TAB-STRIP) | Un controllo che consente all'utente di passare tra più pagine di contenuto. |
| [TEXTBOX](#TEXTBOX) | Un controllo che consente all'utente di inserire testo. |
| [TOGGLE_BUTTON](#TOGGLE-BUTTON) | Un controllo che consente all'utente di alternare tra due stati. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String forms2OleControlTypeName)](#fromName-java.lang.String) |  |
| [getName(int forms2OleControlType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int forms2OleControlType)](#toString-int) |  |
### CHECK_BOX {#CHECK-BOX}
```
public static int CHECK_BOX
```


Un controllo che consente all'utente di selezionare o deselezionare un'opzione.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


Un controllo che consente all'utente di selezionare un elemento da un elenco.

### COMMAND_BUTTON {#COMMAND-BUTTON}
```
public static int COMMAND_BUTTON
```


Un pulsante che avvia un'azione quando viene cliccato.

### FORM {#FORM}
```
public static int FORM
```


Un contenitore per altri controlli.

### FRAME {#FRAME}
```
public static int FRAME
```


Un controllo che raggruppa altri controlli.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Un controllo che visualizza un'immagine.

### LABEL {#LABEL}
```
public static int LABEL
```


Un controllo che visualizza testo.

### LIST_BOX {#LIST-BOX}
```
public static int LIST_BOX
```


Un controllo che visualizza un elenco di elementi.

### MULTI_PAGE {#MULTI-PAGE}
```
public static int MULTI_PAGE
```


Un controllo che visualizza più pagine di contenuto.

### OPTION_BUTTON {#OPTION-BUTTON}
```
public static int OPTION_BUTTON
```


Un controllo pulsante di opzione.

### SCROLL_BAR {#SCROLL-BAR}
```
public static int SCROLL_BAR
```


Un controllo che consente all'utente di scorrere il contenuto.

### SPIN_BUTTON {#SPIN-BUTTON}
```
public static int SPIN_BUTTON
```


Un controllo che consente all'utente di aumentare o diminuire un valore.

### TAB_STRIP {#TAB-STRIP}
```
public static int TAB_STRIP
```


Un controllo che consente all'utente di passare tra più pagine di contenuto.

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


Un controllo che consente all'utente di inserire testo.

### TOGGLE_BUTTON {#TOGGLE-BUTTON}
```
public static int TOGGLE_BUTTON
```


Un controllo che consente all'utente di alternare tra due stati.

### length {#length}
```
public static int length
```


### fromName(String forms2OleControlTypeName) {#fromName-java.lang.String}
```
public static int fromName(String forms2OleControlTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| forms2OleControlTypeName | java.lang.String |  |

**Returns:**
int
### getName(int forms2OleControlType) {#getName-int}
```
public static String getName(int forms2OleControlType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| forms2OleControlType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int forms2OleControlType) {#toString-int}
```
public static String toString(int forms2OleControlType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| forms2OleControlType | int |  |

**Returns:**
java.lang.String
