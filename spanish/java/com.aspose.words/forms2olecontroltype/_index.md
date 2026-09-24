---
title: "Forms2OleControlType"
linktitle: "Forms2OleControlType"
second_title: "Aspose.Words para Java"
description: "Enumera los tipos de controles de Forms 2.0 en Java."
type: docs
weight: 351
url: /es/java/com.aspose.words/forms2olecontroltype/
---

**Inheritance:**
java.lang.Object
```
public class Forms2OleControlType
```

Enumera los tipos de controles de Forms 2.0.

 **Examples:** 

Muestra cómo cambiar el estado del control CheckBox.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 CheckBoxControl checkBoxControl = (CheckBoxControl)shape.getOleFormat().getOleControl();
 checkBoxControl.setChecked(true);

 Assert.assertEquals(true, checkBoxControl.getChecked());
 Assert.assertEquals(Forms2OleControlType.CHECK_BOX, checkBoxControl.getType());
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [CHECK_BOX](#CHECK-BOX) | Un control que permite al usuario seleccionar o deseleccionar una opción. |
| [COMBO_BOX](#COMBO-BOX) | Un control que permite al usuario seleccionar un elemento de una lista. |
| [COMMAND_BUTTON](#COMMAND-BUTTON) | Un botón que desencadena una acción al hacer clic. |
| [FORM](#FORM) | Un contenedor para otros controles. |
| [FRAME](#FRAME) | Un control que agrupa otros controles. |
| [IMAGE](#IMAGE) | Un control que muestra una imagen. |
| [LABEL](#LABEL) | Un control que muestra texto. |
| [LIST_BOX](#LIST-BOX) | Un control que muestra una lista de elementos. |
| [MULTI_PAGE](#MULTI-PAGE) | Un control que muestra múltiples páginas de contenido. |
| [OPTION_BUTTON](#OPTION-BUTTON) | Un control de botón de opción. |
| [SCROLL_BAR](#SCROLL-BAR) | Un control que permite al usuario desplazarse por el contenido. |
| [SPIN_BUTTON](#SPIN-BUTTON) | Un control que permite al usuario aumentar o disminuir un valor. |
| [TAB_STRIP](#TAB-STRIP) | Un control que permite al usuario cambiar entre múltiples páginas de contenido. |
| [TEXTBOX](#TEXTBOX) | Un control que permite al usuario ingresar texto. |
| [TOGGLE_BUTTON](#TOGGLE-BUTTON) | Un control que permite al usuario alternar entre dos estados. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String forms2OleControlTypeName)](#fromName-java.lang.String) |  |
| [getName(int forms2OleControlType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int forms2OleControlType)](#toString-int) |  |
### CHECK_BOX {#CHECK-BOX}
```
public static int CHECK_BOX
```


Un control que permite al usuario seleccionar o deseleccionar una opción.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


Un control que permite al usuario seleccionar un elemento de una lista.

### COMMAND_BUTTON {#COMMAND-BUTTON}
```
public static int COMMAND_BUTTON
```


Un botón que desencadena una acción al hacer clic.

### FORM {#FORM}
```
public static int FORM
```


Un contenedor para otros controles.

### FRAME {#FRAME}
```
public static int FRAME
```


Un control que agrupa otros controles.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Un control que muestra una imagen.

### LABEL {#LABEL}
```
public static int LABEL
```


Un control que muestra texto.

### LIST_BOX {#LIST-BOX}
```
public static int LIST_BOX
```


Un control que muestra una lista de elementos.

### MULTI_PAGE {#MULTI-PAGE}
```
public static int MULTI_PAGE
```


Un control que muestra múltiples páginas de contenido.

### OPTION_BUTTON {#OPTION-BUTTON}
```
public static int OPTION_BUTTON
```


Un control de botón de opción.

### SCROLL_BAR {#SCROLL-BAR}
```
public static int SCROLL_BAR
```


Un control que permite al usuario desplazarse por el contenido.

### SPIN_BUTTON {#SPIN-BUTTON}
```
public static int SPIN_BUTTON
```


Un control que permite al usuario aumentar o disminuir un valor.

### TAB_STRIP {#TAB-STRIP}
```
public static int TAB_STRIP
```


Un control que permite al usuario cambiar entre múltiples páginas de contenido.

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


Un control que permite al usuario ingresar texto.

### TOGGLE_BUTTON {#TOGGLE-BUTTON}
```
public static int TOGGLE_BUTTON
```


Un control que permite al usuario alternar entre dos estados.

### length {#length}
```
public static int length
```


### fromName(String forms2OleControlTypeName) {#fromName-java.lang.String}
```
public static int fromName(String forms2OleControlTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| forms2OleControlTypeName | java.lang.String |  |

**Returns:**
int
### getName(int forms2OleControlType) {#getName-int}
```
public static String getName(int forms2OleControlType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| forms2OleControlType | int |  |

**Returns:**
java.lang.String
