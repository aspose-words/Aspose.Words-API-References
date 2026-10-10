---
title: "OptionButtonControl"
linktitle: "OptionButtonControl"
second_title: "Aspose.Words для Java"
description: "Элемент управления OptionButton позволяет сделать единственный выбор из ограниченного набора взаимно исключающих вариантов в Java."
type: docs
weight: 506
url: /ru/java/com.aspose.words/optionbuttoncontrol/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.OleControl](../../com.aspose.words/olecontrol/), [com.aspose.words.Forms2OleControl](../../com.aspose.words/forms2olecontrol/), [com.aspose.words.MorphDataControl](../../com.aspose.words/morphdatacontrol/)
```
public class OptionButtonControl extends MorphDataControl
```

Элемент управления OptionButton позволяет сделать единственный выбор из ограниченного набора взаимно исключающих вариантов.

 **Examples:** 

Показывает, как выбрать переключатель.

```

 Document doc = new Document(getMyDir() + "Radio buttons.docx");

 Shape shape1 = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 OptionButtonControl optionButton1 = (OptionButtonControl)shape1.getOleFormat().getOleControl();
 // Deselect selected first item.
 optionButton1.setSelected(false);

 Shape shape2 = (Shape)doc.getChild(NodeType.SHAPE, 1, true);
 OptionButtonControl optionButton2 = (OptionButtonControl)shape2.getOleFormat().getOleControl();
 // Select second option button.
 optionButton2.setSelected(true);

 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton1.getType());
 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton2.getType());

 doc.save(getArtifactsDir() + "Shape.SelectRadioControl.docx");
 
```
## Методы

| Метод | Описание |
| --- | --- |
| [getBackColor()](#getBackColor) | Получает цвет фона элемента управления. |
| [getCaption()](#getCaption) | Получает свойство Caption элемента управления. |
| [getChildNodes()](#getChildNodes) | Получает коллекцию непосредственных дочерних элементов управления. |
| [getClsidInternal()](#getClsidInternal) |  |
| [getEnabled()](#getEnabled) | Возвращает  true  если элемент управления находится в включённом состоянии. |
| [getExtensionForUser(String progId)](#getExtensionForUser-java.lang.String) |  |
| [getFileNameForUser()](#getFileNameForUser) |  |
| [getForeColor()](#getForeColor) | Получает цвет переднего плана элемента управления. |
| [getGroupName()](#getGroupName) | Получает строку, указывающую группу взаимно исключающих друг друга элементов управления. |
| [getHeight()](#getHeight) | Получает высоту элемента управления в пунктах. |
| [getId()](#getId) |  |
| [getName()](#getName) | Получает имя ActiveX‑элемента управления. |
| [getSelected()](#getSelected) | Получает логическое значение, указывающее, выбран ли данный [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) или нет. |
| [getType()](#getType) | Получает тип элемента управления Forms 2.0. |
| [getValue()](#getValue) | Получает базовое свойство Value, которое часто представляет состояние элемента управления. |
| [getWidth()](#getWidth) | Получает ширину элемента управления в пунктах. |
| [isEmpty()](#isEmpty) |  |
| [isForms2OleControl()](#isForms2OleControl) | Возвращает  true  если элемент управления является [Forms2OleControl](../../com.aspose.words/forms2olecontrol/). |
| [isForms2OleControlInternal()](#isForms2OleControlInternal) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Устанавливает цвет фона элемента управления. |
| [setCaption(String value)](#setCaption-java.lang.String) | Устанавливает свойство Caption элемента управления. |
| [setForeColor(Color value)](#setForeColor-java.awt.Color) | Устанавливает цвет переднего плана элемента управления. |
| [setGroupName(String value)](#setGroupName-java.lang.String) | Устанавливает строку, определяющую группу взаимно исключающих элементов управления. |
| [setHeight(double value)](#setHeight-double) | Устанавливает высоту элемента управления в пунктах. |
| [setId(int value)](#setId-int) |  |
| [setName(String value)](#setName-java.lang.String) | Устанавливает имя ActiveX‑элемента управления. |
| [setSelected(boolean value)](#setSelected-boolean) | Устанавливает логическое значение, указывающее, выбран ли данный [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) или нет. |
| [setWidth(double value)](#setWidth-double) | Устанавливает ширину элемента управления в пунктах. |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Получает цвет фона элемента управления. Значение по умолчанию зависит от типа элемента управления.

 **Examples:** 

Показывает, как установить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Returns:**
java.awt.Color — Цвет фона элемента управления.
### getCaption() {#getCaption}
```
public String getCaption()
```


Получает свойство Caption элемента управления. Значение по умолчанию — пустая строка.

 **Examples:** 

Показывает, как проверить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

Показывает, как установить подпись для ActiveX‑элемента управления.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl(); { button1.setCaption("Button caption"); }
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals("Button caption", button1.getCaption());
 
```

**Returns:**
java.lang.String — Свойство Caption элемента управления.
### getChildNodes() {#getChildNodes}
```
public Forms2OleControlCollection getChildNodes()
```


Получает коллекцию непосредственных дочерних элементов управления.

 **Remarks:** 

Возвращает  null  если этот элемент управления не может иметь дочерних элементов.

 **Examples:** 

Показывает, как проверить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Returns:**
[Forms2OleControlCollection](../../com.aspose.words/forms2olecontrolcollection/) - Collection of immediate child controls.
### getClsidInternal() {#getClsidInternal}
```
public String getClsidInternal()
```




**Returns:**
java.lang.String
### getEnabled() {#getEnabled}
```
public boolean getEnabled()
```


Возвращает  true  если элемент управления находится в включённом состоянии.

 **Examples:** 

Показывает, как проверить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Returns:**
boolean —  true  если элемент управления находится в включённом состоянии.
### getExtensionForUser(String progId) {#getExtensionForUser-java.lang.String}
```
public String getExtensionForUser(String progId)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| progId | java.lang.String |  |

**Returns:**
java.lang.String
### getFileNameForUser() {#getFileNameForUser}
```
public String getFileNameForUser()
```




**Returns:**
java.lang.String
### getForeColor() {#getForeColor}
```
public Color getForeColor()
```


Получает цвет переднего плана элемента управления. Значение по умолчанию зависит от типа элемента управления.

 **Examples:** 

Показывает, как установить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Returns:**
java.awt.Color — Цвет переднего плана элемента управления.
### getGroupName() {#getGroupName}
```
public String getGroupName()
```


Получает строку, определяющую группу взаимно исключающих элементов управления. Значение по умолчанию — пустая строка.

 **Examples:** 

Показывает, как проверить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Returns:**
java.lang.String — Строка, определяющая группу взаимно исключающих элементов управления.
### getHeight() {#getHeight}
```
public double getHeight()
```


Получает высоту элемента управления в пунктах.

 **Examples:** 

Показывает, как установить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Returns:**
double — Высота элемента управления в пунктах.
### getId() {#getId}
```
public int getId()
```




**Returns:**
int
### getName() {#getName}
```
public String getName()
```


Получает имя ActiveX‑элемента управления.

 **Examples:** 

Показывает, как проверить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Returns:**
java.lang.String — Имя ActiveX‑элемента управления.
### getSelected() {#getSelected}
```
public boolean getSelected()
```


Получает логическое значение, указывающее, выбран ли данный [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) или нет.

 **Remarks:** 

Примечание: это свойство позволяет выбирать несколько элементов в группе [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) с одинаковым [Forms2OleControl.getGroupName()](../../com.aspose.words/forms2olecontrol/\#getGroupName) / [Forms2OleControl.setGroupName(java.lang.String)](../../com.aspose.words/forms2olecontrol/\#setGroupName-java.lang.String). Вам необходимо самостоятельно обеспечить снятие выбора с ранее выбранного элемента при выборе данного [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/).

 **Examples:** 

Показывает, как выбрать переключатель.

```

 Document doc = new Document(getMyDir() + "Radio buttons.docx");

 Shape shape1 = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 OptionButtonControl optionButton1 = (OptionButtonControl)shape1.getOleFormat().getOleControl();
 // Deselect selected first item.
 optionButton1.setSelected(false);

 Shape shape2 = (Shape)doc.getChild(NodeType.SHAPE, 1, true);
 OptionButtonControl optionButton2 = (OptionButtonControl)shape2.getOleFormat().getOleControl();
 // Select second option button.
 optionButton2.setSelected(true);

 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton1.getType());
 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton2.getType());

 doc.save(getArtifactsDir() + "Shape.SelectRadioControl.docx");
 
```

**Returns:**
boolean — логическое значение, указывающее, выбран ли данный [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) или нет.
### getType() {#getType}
```
public int getType()
```


Получает тип элемента управления Forms 2.0.

 **Examples:** 

Показывает, как выбрать переключатель.

```

 Document doc = new Document(getMyDir() + "Radio buttons.docx");

 Shape shape1 = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 OptionButtonControl optionButton1 = (OptionButtonControl)shape1.getOleFormat().getOleControl();
 // Deselect selected first item.
 optionButton1.setSelected(false);

 Shape shape2 = (Shape)doc.getChild(NodeType.SHAPE, 1, true);
 OptionButtonControl optionButton2 = (OptionButtonControl)shape2.getOleFormat().getOleControl();
 // Select second option button.
 optionButton2.setSelected(true);

 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton1.getType());
 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton2.getType());

 doc.save(getArtifactsDir() + "Shape.SelectRadioControl.docx");
 
```

**Returns:**
int — Тип элемента управления Forms 2.0. Возвращаемое значение является одной из констант [Forms2OleControlType](../../com.aspose.words/forms2olecontroltype/).
### getValue() {#getValue}
```
public String getValue()
```


Получает базовое свойство Value, которое часто представляет состояние элемента управления. Например, у отмеченной переключающей кнопки значение '1', а у неотмеченной — '0'. Значение по умолчанию — пустая строка.

 **Examples:** 

Показывает, как проверить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Returns:**
java.lang.String — базовое свойство Value, которое часто представляет состояние элемента управления.
### getWidth() {#getWidth}
```
public double getWidth()
```


Получает ширину элемента управления в пунктах.

 **Examples:** 

Показывает, как установить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Returns:**
double — ширина элемента управления в пунктах.
### isEmpty() {#isEmpty}
```
public boolean isEmpty()
```




**Returns:**
boolean
### isForms2OleControl() {#isForms2OleControl}
```
public boolean isForms2OleControl()
```


Возвращает  true  если элемент управления является [Forms2OleControl](../../com.aspose.words/forms2olecontrol/).

 **Examples:** 

Показывает, как проверить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Returns:**
boolean —  true  если элемент управления является [Forms2OleControl](../../com.aspose.words/forms2olecontrol/).
### isForms2OleControlInternal() {#isForms2OleControlInternal}
```
public boolean isForms2OleControlInternal()
```




**Returns:**
boolean
### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


Устанавливает цвет фона элемента управления. Значение по умолчанию зависит от типа элемента управления.

 **Examples:** 

Показывает, как установить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color | Цвет фона элемента управления. |

### setCaption(String value) {#setCaption-java.lang.String}
```
public void setCaption(String value)
```


Устанавливает свойство Caption элемента управления. Значение по умолчанию — пустая строка.

 **Examples:** 

Показывает, как проверить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

Показывает, как установить подпись для ActiveX‑элемента управления.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl(); { button1.setCaption("Button caption"); }
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals("Button caption", button1.getCaption());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Свойство Caption элемента управления. |

### setForeColor(Color value) {#setForeColor-java.awt.Color}
```
public void setForeColor(Color value)
```


Устанавливает цвет переднего плана элемента управления. Значение по умолчанию зависит от типа элемента управления.

 **Examples:** 

Показывает, как установить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color | Цвет переднего плана элемента управления. |

### setGroupName(String value) {#setGroupName-java.lang.String}
```
public void setGroupName(String value)
```


Устанавливает строку, определяющую группу взаимно исключающих друг друга элементов управления. Значение по умолчанию — пустая строка.

 **Examples:** 

Показывает, как проверить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Строка, определяющая группу взаимно исключающих друг друга элементов управления. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


Устанавливает высоту элемента управления в пунктах.

 **Examples:** 

Показывает, как установить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Высота элемента управления в пунктах. |

### setId(int value) {#setId-int}
```
public void setId(int value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int |  |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Устанавливает имя ActiveX‑элемента управления.

 **Examples:** 

Показывает, как проверить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя ActiveX‑элемента управления. |

### setSelected(boolean value) {#setSelected-boolean}
```
public void setSelected(boolean value)
```


Устанавливает логическое значение, указывающее, выбран ли данный [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) или нет.

 **Remarks:** 

Примечание: это свойство позволяет выбирать несколько элементов в группе [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) с одинаковым [Forms2OleControl.getGroupName()](../../com.aspose.words/forms2olecontrol/\#getGroupName) / [Forms2OleControl.setGroupName(java.lang.String)](../../com.aspose.words/forms2olecontrol/\#setGroupName-java.lang.String). Вам необходимо самостоятельно обеспечить снятие выбора с ранее выбранного элемента при выборе данного [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/).

 **Examples:** 

Показывает, как выбрать переключатель.

```

 Document doc = new Document(getMyDir() + "Radio buttons.docx");

 Shape shape1 = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 OptionButtonControl optionButton1 = (OptionButtonControl)shape1.getOleFormat().getOleControl();
 // Deselect selected first item.
 optionButton1.setSelected(false);

 Shape shape2 = (Shape)doc.getChild(NodeType.SHAPE, 1, true);
 OptionButtonControl optionButton2 = (OptionButtonControl)shape2.getOleFormat().getOleControl();
 // Select second option button.
 optionButton2.setSelected(true);

 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton1.getType());
 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton2.getType());

 doc.save(getArtifactsDir() + "Shape.SelectRadioControl.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее, выбран ли данный [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) или нет. |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


Устанавливает ширину элемента управления в пунктах.

 **Examples:** 

Показывает, как установить свойства ActiveX‑элемента управления.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Ширина элемента управления в пунктах. |

