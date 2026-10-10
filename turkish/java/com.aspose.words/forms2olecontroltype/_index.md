---
title: "Forms2OleControlType"
linktitle: "Forms2OleControlType"
second_title: "Aspose.Words Java için"
description: "Java'da Forms 2.0 denetim türlerini listeler."
type: docs
weight: 351
url: /tr/java/com.aspose.words/forms2olecontroltype/
---

**Inheritance:**
java.lang.Object
```
public class Forms2OleControlType
```

Forms 2.0 denetimlerinin tiplerini numaralandırır.

 **Examples:** 

CheckBox denetiminin durumunun nasıl değiştirileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 CheckBoxControl checkBoxControl = (CheckBoxControl)shape.getOleFormat().getOleControl();
 checkBoxControl.setChecked(true);

 Assert.assertEquals(true, checkBoxControl.getChecked());
 Assert.assertEquals(Forms2OleControlType.CHECK_BOX, checkBoxControl.getType());
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CHECK_BOX](#CHECK-BOX) | Kullanıcının bir seçeneği işaretlemesine veya işaretini kaldırmasına izin veren bir denetim. |
| [COMBO_BOX](#COMBO-BOX) | Kullanıcının bir listeden öğe seçmesine izin veren bir denetim. |
| [COMMAND_BUTTON](#COMMAND-BUTTON) | Tıklandığında bir eylemi tetikleyen bir düğme. |
| [FORM](#FORM) | Diğer denetimler için bir kapsayıcı. |
| [FRAME](#FRAME) | Diğer denetimleri gruplayan bir denetim. |
| [IMAGE](#IMAGE) | Bir resmi gösteren bir denetim. |
| [LABEL](#LABEL) | Metin gösteren bir denetim. |
| [LIST_BOX](#LIST-BOX) | Öğeler listesini gösteren bir denetim. |
| [MULTI_PAGE](#MULTI-PAGE) | Birden fazla içerik sayfasını gösteren bir denetim. |
| [OPTION_BUTTON](#OPTION-BUTTON) | Radyo düğmesi denetimi. |
| [SCROLL_BAR](#SCROLL-BAR) | Kullanıcının içerik içinde kaydırma yapmasına izin veren bir denetim. |
| [SPIN_BUTTON](#SPIN-BUTTON) | Kullanıcının bir değeri artırıp azaltmasına izin veren bir denetim. |
| [TAB_STRIP](#TAB-STRIP) | Kullanıcının birden fazla içerik sayfası arasında geçiş yapmasına izin veren bir denetim. |
| [TEXTBOX](#TEXTBOX) | Kullanıcının metin girmesine izin veren bir denetim. |
| [TOGGLE_BUTTON](#TOGGLE-BUTTON) | Kullanıcının iki durum arasında geçiş yapmasına izin veren bir denetim. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String forms2OleControlTypeName)](#fromName-java.lang.String) |  |
| [getName(int forms2OleControlType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int forms2OleControlType)](#toString-int) |  |
### CHECK_BOX {#CHECK-BOX}
```
public static int CHECK_BOX
```


Kullanıcının bir seçeneği işaretlemesine veya işaretini kaldırmasına izin veren bir denetim.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


Kullanıcının bir listeden öğe seçmesine izin veren bir denetim.

### COMMAND_BUTTON {#COMMAND-BUTTON}
```
public static int COMMAND_BUTTON
```


Tıklandığında bir eylemi tetikleyen bir düğme.

### FORM {#FORM}
```
public static int FORM
```


Diğer denetimler için bir kapsayıcı.

### FRAME {#FRAME}
```
public static int FRAME
```


Diğer denetimleri gruplayan bir denetim.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Bir resmi gösteren bir denetim.

### LABEL {#LABEL}
```
public static int LABEL
```


Metin gösteren bir denetim.

### LIST_BOX {#LIST-BOX}
```
public static int LIST_BOX
```


Öğeler listesini gösteren bir denetim.

### MULTI_PAGE {#MULTI-PAGE}
```
public static int MULTI_PAGE
```


Birden fazla içerik sayfasını gösteren bir denetim.

### OPTION_BUTTON {#OPTION-BUTTON}
```
public static int OPTION_BUTTON
```


Radyo düğmesi denetimi.

### SCROLL_BAR {#SCROLL-BAR}
```
public static int SCROLL_BAR
```


Kullanıcının içerik içinde kaydırma yapmasına izin veren bir denetim.

### SPIN_BUTTON {#SPIN-BUTTON}
```
public static int SPIN_BUTTON
```


Kullanıcının bir değeri artırıp azaltmasına izin veren bir denetim.

### TAB_STRIP {#TAB-STRIP}
```
public static int TAB_STRIP
```


Kullanıcının birden fazla içerik sayfası arasında geçiş yapmasına izin veren bir denetim.

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


Kullanıcının metin girmesine izin veren bir denetim.

### TOGGLE_BUTTON {#TOGGLE-BUTTON}
```
public static int TOGGLE_BUTTON
```


Kullanıcının iki durum arasında geçiş yapmasına izin veren bir denetim.

### length {#length}
```
public static int length
```


### fromName(String forms2OleControlTypeName) {#fromName-java.lang.String}
```
public static int fromName(String forms2OleControlTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| forms2OleControlTypeName | java.lang.String |  |

**Returns:**
int
### getName(int forms2OleControlType) {#getName-int}
```
public static String getName(int forms2OleControlType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| forms2OleControlType | int |  |

**Returns:**
java.lang.String
