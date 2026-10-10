---
title: "Forms2OleControlType"
linktitle: "Forms2OleControlType"
second_title: "Aspose.Words pour Java"
description: "Énumère les types de contrôles Forms 2.0 en Java."
type: docs
weight: 351
url: /fr/java/com.aspose.words/forms2olecontroltype/
---

**Inheritance:**
java.lang.Object
```
public class Forms2OleControlType
```

Énumère les types de contrôles Forms 2.0.

 **Examples:** 

Montre comment changer l'état du contrôle CheckBox.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 CheckBoxControl checkBoxControl = (CheckBoxControl)shape.getOleFormat().getOleControl();
 checkBoxControl.setChecked(true);

 Assert.assertEquals(true, checkBoxControl.getChecked());
 Assert.assertEquals(Forms2OleControlType.CHECK_BOX, checkBoxControl.getType());
 
```
## Champs

| Champ | Description |
| --- | --- |
| [CHECK_BOX](#CHECK-BOX) | Un contrôle qui permet à l'utilisateur de sélectionner ou désélectionner une option. |
| [COMBO_BOX](#COMBO-BOX) | Un contrôle qui permet à l'utilisateur de sélectionner un élément dans une liste. |
| [COMMAND_BUTTON](#COMMAND-BUTTON) | Un bouton qui déclenche une action lorsqu'il est cliqué. |
| [FORM](#FORM) | Un conteneur pour d'autres contrôles. |
| [FRAME](#FRAME) | Un contrôle qui regroupe d'autres contrôles. |
| [IMAGE](#IMAGE) | Un contrôle qui affiche une image. |
| [LABEL](#LABEL) | Un contrôle qui affiche du texte. |
| [LIST_BOX](#LIST-BOX) | Un contrôle qui affiche une liste d'éléments. |
| [MULTI_PAGE](#MULTI-PAGE) | Un contrôle qui affiche plusieurs pages de contenu. |
| [OPTION_BUTTON](#OPTION-BUTTON) | Un contrôle de bouton radio. |
| [SCROLL_BAR](#SCROLL-BAR) | Un contrôle qui permet à l'utilisateur de faire défiler le contenu. |
| [SPIN_BUTTON](#SPIN-BUTTON) | Un contrôle qui permet à l'utilisateur d'augmenter ou de diminuer une valeur. |
| [TAB_STRIP](#TAB-STRIP) | Un contrôle qui permet à l'utilisateur de basculer entre plusieurs pages de contenu. |
| [TEXTBOX](#TEXTBOX) | Un contrôle qui permet à l'utilisateur de saisir du texte. |
| [TOGGLE_BUTTON](#TOGGLE-BUTTON) | Un contrôle qui permet à l'utilisateur de basculer entre deux états. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String forms2OleControlTypeName)](#fromName-java.lang.String) |  |
| [getName(int forms2OleControlType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int forms2OleControlType)](#toString-int) |  |
### CHECK_BOX {#CHECK-BOX}
```
public static int CHECK_BOX
```


Un contrôle qui permet à l'utilisateur de sélectionner ou désélectionner une option.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


Un contrôle qui permet à l'utilisateur de sélectionner un élément dans une liste.

### COMMAND_BUTTON {#COMMAND-BUTTON}
```
public static int COMMAND_BUTTON
```


Un bouton qui déclenche une action lorsqu'il est cliqué.

### FORM {#FORM}
```
public static int FORM
```


Un conteneur pour d'autres contrôles.

### FRAME {#FRAME}
```
public static int FRAME
```


Un contrôle qui regroupe d'autres contrôles.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Un contrôle qui affiche une image.

### LABEL {#LABEL}
```
public static int LABEL
```


Un contrôle qui affiche du texte.

### LIST_BOX {#LIST-BOX}
```
public static int LIST_BOX
```


Un contrôle qui affiche une liste d'éléments.

### MULTI_PAGE {#MULTI-PAGE}
```
public static int MULTI_PAGE
```


Un contrôle qui affiche plusieurs pages de contenu.

### OPTION_BUTTON {#OPTION-BUTTON}
```
public static int OPTION_BUTTON
```


Un contrôle de bouton radio.

### SCROLL_BAR {#SCROLL-BAR}
```
public static int SCROLL_BAR
```


Un contrôle qui permet à l'utilisateur de faire défiler le contenu.

### SPIN_BUTTON {#SPIN-BUTTON}
```
public static int SPIN_BUTTON
```


Un contrôle qui permet à l'utilisateur d'augmenter ou de diminuer une valeur.

### TAB_STRIP {#TAB-STRIP}
```
public static int TAB_STRIP
```


Un contrôle qui permet à l'utilisateur de basculer entre plusieurs pages de contenu.

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


Un contrôle qui permet à l'utilisateur de saisir du texte.

### TOGGLE_BUTTON {#TOGGLE-BUTTON}
```
public static int TOGGLE_BUTTON
```


Un contrôle qui permet à l'utilisateur de basculer entre deux états.

### length {#length}
```
public static int length
```


### fromName(String forms2OleControlTypeName) {#fromName-java.lang.String}
```
public static int fromName(String forms2OleControlTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| forms2OleControlTypeName | java.lang.String |  |

**Returns:**
int
### getName(int forms2OleControlType) {#getName-int}
```
public static String getName(int forms2OleControlType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| forms2OleControlType | int |  |

**Returns:**
java.lang.String
