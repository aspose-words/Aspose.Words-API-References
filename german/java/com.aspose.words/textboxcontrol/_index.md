---
title: "TextBoxControl"
linktitle: "TextBoxControl"
second_title: "Aspose.Words für Java"
description: "Das TextBox-Steuerelement zeigt Text aus einem organisierten Datensatz oder Benutzereingaben in Java an."
type: docs
weight: 668
url: /de/java/com.aspose.words/textboxcontrol/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.OleControl](../../com.aspose.words/olecontrol/), [com.aspose.words.Forms2OleControl](../../com.aspose.words/forms2olecontrol/), [com.aspose.words.MorphDataControl](../../com.aspose.words/morphdatacontrol/)
```
public class TextBoxControl extends MorphDataControl
```

Das TextBox‑Steuerelement zeigt Text aus einem organisierten Datensatz oder Benutzereingaben an.

 **Examples:** 

Zeigt, wie der Text des TextBox OLE-Steuerelements geändert wird.

```

 Document doc = new Document(getMyDir() + "Textbox control.docm");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 TextBoxControl textBoxControl = (TextBoxControl)shape.getOleFormat().getOleControl();
 Assert.assertEquals(textBoxControl.getText(), "Aspose.Words test");

 textBoxControl.setText("Updated text");
 Assert.assertEquals(textBoxControl.getText(), "Updated text");
 
```
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getBackColor()](#getBackColor) | Liefert die Hintergrundfarbe des Steuerelements. |
| [getCaption()](#getCaption) | Liefert die Caption‑Eigenschaft des Steuerelements. |
| [getChildNodes()](#getChildNodes) | Liefert die Sammlung unmittelbarer untergeordneter Steuerelemente. |
| [getClsidInternal()](#getClsidInternal) |  |
| [getEnabled()](#getEnabled) | Gibt  true  zurück, wenn das Steuerelement im aktivierten Zustand ist. |
| [getExtensionForUser(String progId)](#getExtensionForUser-java.lang.String) |  |
| [getFileNameForUser()](#getFileNameForUser) |  |
| [getForeColor()](#getForeColor) | Liefert die Vordergrundfarbe des Steuerelements. |
| [getGroupName()](#getGroupName) | Liefert eine Zeichenkette, die eine Gruppe gegenseitig ausschließender Steuerelemente angibt. |
| [getHeight()](#getHeight) | Liefert die Höhe des Steuerelements in Punkten. |
| [getId()](#getId) |  |
| [getName()](#getName) | Liefert den Namen des ActiveX‑Steuerelements. |
| [getText()](#getText) | Liest den Text des Steuerelements. |
| [getType()](#getType) | Liefert den Typ des Forms‑2.0‑Steuerelements. |
| [getValue()](#getValue) | Liefert die zugrunde liegende Value‑Eigenschaft, die häufig den Zustand des Steuerelements darstellt. |
| [getWidth()](#getWidth) | Ermittelt die Breite des Steuerelements in Punkten. |
| [isEmpty()](#isEmpty) |  |
| [isForms2OleControl()](#isForms2OleControl) | Gibt  true  zurück, wenn das Steuerelement ein [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) ist. |
| [isForms2OleControlInternal()](#isForms2OleControlInternal) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Legt eine Hintergrundfarbe des Steuerelements fest. |
| [setCaption(String value)](#setCaption-java.lang.String) | Legt die Caption-Eigenschaft des Steuerelements fest. |
| [setForeColor(Color value)](#setForeColor-java.awt.Color) | Legt eine Vordergrundfarbe des Steuerelements fest. |
| [setGroupName(String value)](#setGroupName-java.lang.String) | Legt eine Zeichenkette fest, die eine Gruppe von gegenseitig ausschließenden Steuerelementen angibt. |
| [setHeight(double value)](#setHeight-double) | Legt die Höhe des Steuerelements in Punkten fest. |
| [setId(int value)](#setId-int) |  |
| [setName(String value)](#setName-java.lang.String) | Legt den Namen des ActiveX-Steuerelements fest. |
| [setText(String value)](#setText-java.lang.String) | Setzt den Text des Steuerelements. |
| [setWidth(double value)](#setWidth-double) | Legt die Breite des Steuerelements in Punkten fest. |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Ermittelt die Hintergrundfarbe des Steuerelements. Der Standardwert hängt vom Typ des Steuerelements ab.

 **Examples:** 

Zeigt, wie Eigenschaften für ein ActiveX-Steuerelement festgelegt werden.

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
java.awt.Color - Eine Hintergrundfarbe des Steuerelements.
### getCaption() {#getCaption}
```
public String getCaption()
```


Ermittelt die Caption-Eigenschaft des Steuerelements. Der Standardwert ist eine leere Zeichenkette.

 **Examples:** 

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

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

Zeigt, wie die Caption für ein ActiveX-Steuerelement festgelegt wird.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl(); { button1.setCaption("Button caption"); }
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals("Button caption", button1.getCaption());
 
```

**Returns:**
java.lang.String - Eine Caption-Eigenschaft des Steuerelements.
### getChildNodes() {#getChildNodes}
```
public Forms2OleControlCollection getChildNodes()
```


Liefert die Sammlung unmittelbarer untergeordneter Steuerelemente.

 **Remarks:** 

Gibt  null  zurück, wenn dieses Steuerelement keine Kinder haben kann.

 **Examples:** 

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

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


Gibt  true  zurück, wenn das Steuerelement im aktivierten Zustand ist.

 **Examples:** 

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

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
boolean -  true  wenn das Steuerelement aktiviert ist.
### getExtensionForUser(String progId) {#getExtensionForUser-java.lang.String}
```
public String getExtensionForUser(String progId)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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


Ermittelt die Vordergrundfarbe des Steuerelements. Der Standardwert hängt vom Typ des Steuerelements ab.

 **Examples:** 

Zeigt, wie Eigenschaften für ein ActiveX-Steuerelement festgelegt werden.

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
java.awt.Color - Eine Vordergrundfarbe des Steuerelements.
### getGroupName() {#getGroupName}
```
public String getGroupName()
```


Ermittelt eine Zeichenkette, die eine Gruppe von gegenseitig ausschließenden Steuerelementen angibt. Der Standardwert ist eine leere Zeichenkette.

 **Examples:** 

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

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
java.lang.String - Eine Zeichenkette, die eine Gruppe von gegenseitig ausschließenden Steuerelementen angibt.
### getHeight() {#getHeight}
```
public double getHeight()
```


Liefert die Höhe des Steuerelements in Punkten.

 **Examples:** 

Zeigt, wie Eigenschaften für ein ActiveX-Steuerelement festgelegt werden.

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
double - Eine Höhe des Steuerelements in Punkten.
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


Liefert den Namen des ActiveX‑Steuerelements.

 **Examples:** 

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

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
java.lang.String - Name des ActiveX-Steuerelements.
### getText() {#getText}
```
public String getText()
```


Liest den Text des Steuerelements.

 **Examples:** 

Zeigt, wie der Text des TextBox OLE-Steuerelements geändert wird.

```

 Document doc = new Document(getMyDir() + "Textbox control.docm");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 TextBoxControl textBoxControl = (TextBoxControl)shape.getOleFormat().getOleControl();
 Assert.assertEquals(textBoxControl.getText(), "Aspose.Words test");

 textBoxControl.setText("Updated text");
 Assert.assertEquals(textBoxControl.getText(), "Updated text");
 
```

**Returns:**
java.lang.String - Ein Text des Steuerelements.
### getType() {#getType}
```
public int getType()
```


Liefert den Typ des Forms‑2.0‑Steuerelements.

 **Examples:** 

Zeigt, wie der Text des TextBox OLE-Steuerelements geändert wird.

```

 Document doc = new Document(getMyDir() + "Textbox control.docm");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 TextBoxControl textBoxControl = (TextBoxControl)shape.getOleFormat().getOleControl();
 Assert.assertEquals(textBoxControl.getText(), "Aspose.Words test");

 textBoxControl.setText("Updated text");
 Assert.assertEquals(textBoxControl.getText(), "Updated text");
 
```

**Returns:**
int - Typ eines Forms 2.0‑Steuerelements. Der zurückgegebene Wert ist einer der Konstanten von [Forms2OleControlType](../../com.aspose.words/forms2olecontroltype/).
### getValue() {#getValue}
```
public String getValue()
```


Liest die zugrunde liegende Value‑Eigenschaft, die häufig den Zustand des Steuerelements darstellt. Beispielsweise hat ein aktiviertes Optionsfeld den Wert '1', während ein deaktiviertes den Wert '0' hat. Der Standardwert ist eine leere Zeichenfolge.

 **Examples:** 

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

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
java.lang.String - Zugrunde liegende Value‑Eigenschaft, die häufig den Zustand des Steuerelements darstellt.
### getWidth() {#getWidth}
```
public double getWidth()
```


Ermittelt die Breite des Steuerelements in Punkten.

 **Examples:** 

Zeigt, wie Eigenschaften für ein ActiveX-Steuerelement festgelegt werden.

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
double - Eine Breite des Steuerelements in Punkten.
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


Gibt  true  zurück, wenn das Steuerelement ein [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) ist.

 **Examples:** 

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

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
boolean -  true  wenn das Steuerelement ein [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) ist.
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


Legt die Hintergrundfarbe des Steuerelements fest. Der Standardwert hängt vom Typ des Steuerelements ab.

 **Examples:** 

Zeigt, wie Eigenschaften für ein ActiveX-Steuerelement festgelegt werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Eine Hintergrundfarbe des Steuerelements. |

### setCaption(String value) {#setCaption-java.lang.String}
```
public void setCaption(String value)
```


Legt die Caption‑Eigenschaft des Steuerelements fest. Der Standardwert ist eine leere Zeichenfolge.

 **Examples:** 

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

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

Zeigt, wie die Caption für ein ActiveX-Steuerelement festgelegt wird.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl(); { button1.setCaption("Button caption"); }
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals("Button caption", button1.getCaption());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Eine Caption‑Eigenschaft des Steuerelements. |

### setForeColor(Color value) {#setForeColor-java.awt.Color}
```
public void setForeColor(Color value)
```


Legt die Vordergrundfarbe des Steuerelements fest. Der Standardwert hängt vom Typ des Steuerelements ab.

 **Examples:** 

Zeigt, wie Eigenschaften für ein ActiveX-Steuerelement festgelegt werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Eine Vordergrundfarbe des Steuerelements. |

### setGroupName(String value) {#setGroupName-java.lang.String}
```
public void setGroupName(String value)
```


Legt eine Zeichenfolge fest, die eine Gruppe von gegenseitig ausschließenden Steuerelementen angibt. Der Standardwert ist eine leere Zeichenfolge.

 **Examples:** 

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Eine Zeichenfolge, die eine Gruppe von gegenseitig ausschließenden Steuerelementen angibt. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


Legt die Höhe des Steuerelements in Punkten fest.

 **Examples:** 

Zeigt, wie Eigenschaften für ein ActiveX-Steuerelement festgelegt werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Eine Höhe des Steuerelements in Punkten. |

### setId(int value) {#setId-int}
```
public void setId(int value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int |  |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Legt den Namen des ActiveX-Steuerelements fest.

 **Examples:** 

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Name des ActiveX‑Steuerelements. |

### setText(String value) {#setText-java.lang.String}
```
public void setText(String value)
```


Setzt den Text des Steuerelements.

 **Examples:** 

Zeigt, wie der Text des TextBox OLE-Steuerelements geändert wird.

```

 Document doc = new Document(getMyDir() + "Textbox control.docm");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 TextBoxControl textBoxControl = (TextBoxControl)shape.getOleFormat().getOleControl();
 Assert.assertEquals(textBoxControl.getText(), "Aspose.Words test");

 textBoxControl.setText("Updated text");
 Assert.assertEquals(textBoxControl.getText(), "Updated text");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Ein Text des Steuerelements. |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


Legt die Breite des Steuerelements in Punkten fest.

 **Examples:** 

Zeigt, wie Eigenschaften für ein ActiveX-Steuerelement festgelegt werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Eine Breite des Steuerelements in Punkten. |

