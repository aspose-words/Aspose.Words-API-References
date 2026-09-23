---
title: "Forms2OleControlType"
linktitle: "Forms2OleControlType"
second_title: "Aspose.Words für Java"
description: "Enumeriert die Typen von Forms 2.0‑Steuerelementen in Java."
type: docs
weight: 351
url: /de/java/com.aspose.words/forms2olecontroltype/
---

**Inheritance:**
java.lang.Object
```
public class Forms2OleControlType
```

Enumeriert die Typen von Forms 2.0-Steuerelementen.

 **Examples:** 

Zeigt, wie der Zustand des CheckBox‑Steuerelements geändert wird.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 CheckBoxControl checkBoxControl = (CheckBoxControl)shape.getOleFormat().getOleControl();
 checkBoxControl.setChecked(true);

 Assert.assertEquals(true, checkBoxControl.getChecked());
 Assert.assertEquals(Forms2OleControlType.CHECK_BOX, checkBoxControl.getType());
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CHECK_BOX](#CHECK-BOX) | Ein Steuerelement, das dem Benutzer ermöglicht, eine Option auszuwählen oder abzuwählen. |
| [COMBO_BOX](#COMBO-BOX) | Ein Steuerelement, das dem Benutzer ermöglicht, ein Element aus einer Liste auszuwählen. |
| [COMMAND_BUTTON](#COMMAND-BUTTON) | Ein Button, der eine Aktion auslöst, wenn er angeklickt wird. |
| [FORM](#FORM) | Ein Container für andere Steuerelemente. |
| [FRAME](#FRAME) | Ein Steuerelement, das andere Steuerelemente gruppiert. |
| [IMAGE](#IMAGE) | Ein Steuerelement, das ein Bild anzeigt. |
| [LABEL](#LABEL) | Ein Steuerelement, das Text anzeigt. |
| [LIST_BOX](#LIST-BOX) | Ein Steuerelement, das eine Liste von Elementen anzeigt. |
| [MULTI_PAGE](#MULTI-PAGE) | Ein Steuerelement, das mehrere Seiten Inhalt anzeigt. |
| [OPTION_BUTTON](#OPTION-BUTTON) | Ein Radio‑Button‑Steuerelement. |
| [SCROLL_BAR](#SCROLL-BAR) | Ein Steuerelement, das dem Benutzer ermöglicht, durch Inhalt zu scrollen. |
| [SPIN_BUTTON](#SPIN-BUTTON) | Ein Steuerelement, das dem Benutzer ermöglicht, einen Wert zu erhöhen oder zu verringern. |
| [TAB_STRIP](#TAB-STRIP) | Ein Steuerelement, das dem Benutzer ermöglicht, zwischen mehreren Inhaltsseiten zu wechseln. |
| [TEXTBOX](#TEXTBOX) | Ein Steuerelement, das dem Benutzer das Eingeben von Text ermöglicht. |
| [TOGGLE_BUTTON](#TOGGLE-BUTTON) | Ein Steuerelement, das dem Benutzer das Umschalten zwischen zwei Zuständen ermöglicht. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String forms2OleControlTypeName)](#fromName-java.lang.String) |  |
| [getName(int forms2OleControlType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int forms2OleControlType)](#toString-int) |  |
### CHECK_BOX {#CHECK-BOX}
```
public static int CHECK_BOX
```


Ein Steuerelement, das dem Benutzer ermöglicht, eine Option auszuwählen oder abzuwählen.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


Ein Steuerelement, das dem Benutzer ermöglicht, ein Element aus einer Liste auszuwählen.

### COMMAND_BUTTON {#COMMAND-BUTTON}
```
public static int COMMAND_BUTTON
```


Ein Button, der eine Aktion auslöst, wenn er angeklickt wird.

### FORM {#FORM}
```
public static int FORM
```


Ein Container für andere Steuerelemente.

### FRAME {#FRAME}
```
public static int FRAME
```


Ein Steuerelement, das andere Steuerelemente gruppiert.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Ein Steuerelement, das ein Bild anzeigt.

### LABEL {#LABEL}
```
public static int LABEL
```


Ein Steuerelement, das Text anzeigt.

### LIST_BOX {#LIST-BOX}
```
public static int LIST_BOX
```


Ein Steuerelement, das eine Liste von Elementen anzeigt.

### MULTI_PAGE {#MULTI-PAGE}
```
public static int MULTI_PAGE
```


Ein Steuerelement, das mehrere Seiten Inhalt anzeigt.

### OPTION_BUTTON {#OPTION-BUTTON}
```
public static int OPTION_BUTTON
```


Ein Radio‑Button‑Steuerelement.

### SCROLL_BAR {#SCROLL-BAR}
```
public static int SCROLL_BAR
```


Ein Steuerelement, das dem Benutzer ermöglicht, durch Inhalt zu scrollen.

### SPIN_BUTTON {#SPIN-BUTTON}
```
public static int SPIN_BUTTON
```


Ein Steuerelement, das dem Benutzer ermöglicht, einen Wert zu erhöhen oder zu verringern.

### TAB_STRIP {#TAB-STRIP}
```
public static int TAB_STRIP
```


Ein Steuerelement, das dem Benutzer ermöglicht, zwischen mehreren Inhaltsseiten zu wechseln.

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


Ein Steuerelement, das dem Benutzer das Eingeben von Text ermöglicht.

### TOGGLE_BUTTON {#TOGGLE-BUTTON}
```
public static int TOGGLE_BUTTON
```


Ein Steuerelement, das dem Benutzer das Umschalten zwischen zwei Zuständen ermöglicht.

### length {#length}
```
public static int length
```


### fromName(String forms2OleControlTypeName) {#fromName-java.lang.String}
```
public static int fromName(String forms2OleControlTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| forms2OleControlTypeName | java.lang.String |  |

**Returns:**
int
### getName(int forms2OleControlType) {#getName-int}
```
public static String getName(int forms2OleControlType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| forms2OleControlType | int |  |

**Returns:**
java.lang.String
