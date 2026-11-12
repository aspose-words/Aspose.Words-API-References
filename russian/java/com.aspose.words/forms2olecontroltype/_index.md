---
title: "Forms2OleControlType"
linktitle: "Forms2OleControlType"
second_title: "Aspose.Words для Java"
description: "Перечисляет типы элементов управления Forms 2.0 в Java."
type: docs
weight: 351
url: /ru/java/com.aspose.words/forms2olecontroltype/
---

**Inheritance:**
java.lang.Object
```
public class Forms2OleControlType
```

Перечисляет типы элементов управления Forms 2.0.

 **Examples:** 

Показывает, как изменить состояние элемента управления CheckBox.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 CheckBoxControl checkBoxControl = (CheckBoxControl)shape.getOleFormat().getOleControl();
 checkBoxControl.setChecked(true);

 Assert.assertEquals(true, checkBoxControl.getChecked());
 Assert.assertEquals(Forms2OleControlType.CHECK_BOX, checkBoxControl.getType());
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [CHECK_BOX](#CHECK-BOX) | Элемент управления, позволяющий пользователю выбрать или снять выбор опции. |
| [COMBO_BOX](#COMBO-BOX) | Элемент управления, позволяющий пользователю выбрать элемент из списка. |
| [COMMAND_BUTTON](#COMMAND-BUTTON) | Кнопка, вызывающая действие при нажатии. |
| [FORM](#FORM) | Контейнер для других элементов управления. |
| [FRAME](#FRAME) | Элемент управления, группирующий другие элементы управления. |
| [IMAGE](#IMAGE) | Элемент управления, отображающий изображение. |
| [LABEL](#LABEL) | Элемент управления, отображающий текст. |
| [LIST_BOX](#LIST-BOX) | Элемент управления, отображающий список элементов. |
| [MULTI_PAGE](#MULTI-PAGE) | Элемент управления, отображающий несколько страниц содержимого. |
| [OPTION_BUTTON](#OPTION-BUTTON) | Элемент управления радиокнопкой. |
| [SCROLL_BAR](#SCROLL-BAR) | Элемент управления, позволяющий пользователю прокручивать содержимое. |
| [SPIN_BUTTON](#SPIN-BUTTON) | Элемент управления, позволяющий пользователю увеличить или уменьшить значение. |
| [TAB_STRIP](#TAB-STRIP) | Элемент управления, позволяющий пользователю переключаться между несколькими страницами содержимого. |
| [TEXTBOX](#TEXTBOX) | Элемент управления, позволяющий пользователю вводить текст. |
| [TOGGLE_BUTTON](#TOGGLE-BUTTON) | Элемент управления, позволяющий пользователю переключаться между двумя состояниями. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String forms2OleControlTypeName)](#fromName-java.lang.String) |  |
| [getName(int forms2OleControlType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int forms2OleControlType)](#toString-int) |  |
### CHECK_BOX {#CHECK-BOX}
```
public static int CHECK_BOX
```


Элемент управления, позволяющий пользователю выбрать или снять выбор опции.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


Элемент управления, позволяющий пользователю выбрать элемент из списка.

### COMMAND_BUTTON {#COMMAND-BUTTON}
```
public static int COMMAND_BUTTON
```


Кнопка, вызывающая действие при нажатии.

### FORM {#FORM}
```
public static int FORM
```


Контейнер для других элементов управления.

### FRAME {#FRAME}
```
public static int FRAME
```


Элемент управления, группирующий другие элементы управления.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Элемент управления, отображающий изображение.

### LABEL {#LABEL}
```
public static int LABEL
```


Элемент управления, отображающий текст.

### LIST_BOX {#LIST-BOX}
```
public static int LIST_BOX
```


Элемент управления, отображающий список элементов.

### MULTI_PAGE {#MULTI-PAGE}
```
public static int MULTI_PAGE
```


Элемент управления, отображающий несколько страниц содержимого.

### OPTION_BUTTON {#OPTION-BUTTON}
```
public static int OPTION_BUTTON
```


Элемент управления радиокнопкой.

### SCROLL_BAR {#SCROLL-BAR}
```
public static int SCROLL_BAR
```


Элемент управления, позволяющий пользователю прокручивать содержимое.

### SPIN_BUTTON {#SPIN-BUTTON}
```
public static int SPIN_BUTTON
```


Элемент управления, позволяющий пользователю увеличить или уменьшить значение.

### TAB_STRIP {#TAB-STRIP}
```
public static int TAB_STRIP
```


Элемент управления, позволяющий пользователю переключаться между несколькими страницами содержимого.

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


Элемент управления, позволяющий пользователю вводить текст.

### TOGGLE_BUTTON {#TOGGLE-BUTTON}
```
public static int TOGGLE_BUTTON
```


Элемент управления, позволяющий пользователю переключаться между двумя состояниями.

### length {#length}
```
public static int length
```


### fromName(String forms2OleControlTypeName) {#fromName-java.lang.String}
```
public static int fromName(String forms2OleControlTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| forms2OleControlTypeName | java.lang.String |  |

**Returns:**
int
### getName(int forms2OleControlType) {#getName-int}
```
public static String getName(int forms2OleControlType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| forms2OleControlType | int |  |

**Returns:**
java.lang.String
