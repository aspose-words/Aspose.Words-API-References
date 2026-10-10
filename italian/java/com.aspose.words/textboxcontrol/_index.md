---
title: "TextBoxControl"
linktitle: "TextBoxControl"
second_title: "Aspose.Words per Java"
description: "Il controllo TextBox visualizza il testo da un insieme organizzato di dati o input dell'utente in Java."
type: docs
weight: 668
url: /it/java/com.aspose.words/textboxcontrol/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.OleControl](../../com.aspose.words/olecontrol/), [com.aspose.words.Forms2OleControl](../../com.aspose.words/forms2olecontrol/), [com.aspose.words.MorphDataControl](../../com.aspose.words/morphdatacontrol/)
```
public class TextBoxControl extends MorphDataControl
```

Il controllo TextBox visualizza il testo da un insieme organizzato di dati o input dell'utente.

 **Examples:** 

Mostra come modificare il testo del controllo OLE TextBox.

```

 Document doc = new Document(getMyDir() + "Textbox control.docm");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 TextBoxControl textBoxControl = (TextBoxControl)shape.getOleFormat().getOleControl();
 Assert.assertEquals(textBoxControl.getText(), "Aspose.Words test");

 textBoxControl.setText("Updated text");
 Assert.assertEquals(textBoxControl.getText(), "Updated text");
 
```
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getBackColor()](#getBackColor) | Restituisce un colore di sfondo del controllo. |
| [getCaption()](#getCaption) | Restituisce la proprietà Caption del controllo. |
| [getChildNodes()](#getChildNodes) | Restituisce la collezione dei controlli figli immediati. |
| [getClsidInternal()](#getClsidInternal) |  |
| [getEnabled()](#getEnabled) | Restituisce  true  se il controllo è nello stato abilitato. |
| [getExtensionForUser(String progId)](#getExtensionForUser-java.lang.String) |  |
| [getFileNameForUser()](#getFileNameForUser) |  |
| [getForeColor()](#getForeColor) | Restituisce un colore di primo piano del controllo. |
| [getGroupName()](#getGroupName) | Restituisce una stringa che specifica un gruppo di controlli mutuamente esclusivi. |
| [getHeight()](#getHeight) | Restituisce un'altezza del controllo in punti. |
| [getId()](#getId) |  |
| [getName()](#getName) | Restituisce il nome del controllo ActiveX. |
| [getText()](#getText) | Ottiene il testo del controllo. |
| [getType()](#getType) | Restituisce il tipo del controllo Forms 2.0. |
| [getValue()](#getValue) | Restituisce la proprietà Value sottostante che spesso rappresenta lo stato del controllo. |
| [getWidth()](#getWidth) | Restituisce una larghezza del controllo in punti. |
| [isEmpty()](#isEmpty) |  |
| [isForms2OleControl()](#isForms2OleControl) | Restituisce true se il controllo è un [Forms2OleControl](../../com.aspose.words/forms2olecontrol/). |
| [isForms2OleControlInternal()](#isForms2OleControlInternal) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Imposta un colore di sfondo del controllo. |
| [setCaption(String value)](#setCaption-java.lang.String) | Imposta la proprietà Caption del controllo. |
| [setForeColor(Color value)](#setForeColor-java.awt.Color) | Imposta un colore di primo piano del controllo. |
| [setGroupName(String value)](#setGroupName-java.lang.String) | Imposta una stringa che specifica un gruppo di controlli mutuamente esclusivi. |
| [setHeight(double value)](#setHeight-double) | Imposta un'altezza del controllo in punti. |
| [setId(int value)](#setId-int) |  |
| [setName(String value)](#setName-java.lang.String) | Imposta il nome del controllo ActiveX. |
| [setText(String value)](#setText-java.lang.String) | Imposta il testo del controllo. |
| [setWidth(double value)](#setWidth-double) | Imposta una larghezza del controllo in punti. |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Ottiene il colore di sfondo del controllo. Il valore predefinito dipende dal tipo di controllo.

 **Examples:** 

Mostra come impostare le proprietà per il controllo ActiveX.

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
java.awt.Color - Un colore di sfondo del controllo.
### getCaption() {#getCaption}
```
public String getCaption()
```


Ottiene la proprietà Caption del controllo. Il valore predefinito è una stringa vuota.

 **Examples:** 

Mostra come verificare le proprietà di un controllo ActiveX.

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

Mostra come impostare la didascalia per il controllo ActiveX.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl(); { button1.setCaption("Button caption"); }
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals("Button caption", button1.getCaption());
 
```

**Returns:**
java.lang.String - Una proprietà Caption del controllo.
### getChildNodes() {#getChildNodes}
```
public Forms2OleControlCollection getChildNodes()
```


Restituisce la collezione dei controlli figli immediati.

 **Remarks:** 

Restituisce null se questo controllo non può avere figli.

 **Examples:** 

Mostra come verificare le proprietà di un controllo ActiveX.

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


Restituisce  true  se il controllo è nello stato abilitato.

 **Examples:** 

Mostra come verificare le proprietà di un controllo ActiveX.

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
boolean - true se il controllo è nello stato abilitato.
### getExtensionForUser(String progId) {#getExtensionForUser-java.lang.String}
```
public String getExtensionForUser(String progId)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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


Ottiene il colore di primo piano del controllo. Il valore predefinito dipende dal tipo di controllo.

 **Examples:** 

Mostra come impostare le proprietà per il controllo ActiveX.

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
java.awt.Color - Un colore di primo piano del controllo.
### getGroupName() {#getGroupName}
```
public String getGroupName()
```


Ottiene una stringa che specifica un gruppo di controlli mutuamente esclusivi. Il valore predefinito è una stringa vuota.

 **Examples:** 

Mostra come verificare le proprietà di un controllo ActiveX.

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
java.lang.String - Una stringa che specifica un gruppo di controlli mutuamente esclusivi.
### getHeight() {#getHeight}
```
public double getHeight()
```


Restituisce un'altezza del controllo in punti.

 **Examples:** 

Mostra come impostare le proprietà per il controllo ActiveX.

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
double - Un'altezza del controllo in punti.
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


Restituisce il nome del controllo ActiveX.

 **Examples:** 

Mostra come verificare le proprietà di un controllo ActiveX.

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
java.lang.String - Nome del controllo ActiveX.
### getText() {#getText}
```
public String getText()
```


Ottiene il testo del controllo.

 **Examples:** 

Mostra come modificare il testo del controllo OLE TextBox.

```

 Document doc = new Document(getMyDir() + "Textbox control.docm");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 TextBoxControl textBoxControl = (TextBoxControl)shape.getOleFormat().getOleControl();
 Assert.assertEquals(textBoxControl.getText(), "Aspose.Words test");

 textBoxControl.setText("Updated text");
 Assert.assertEquals(textBoxControl.getText(), "Updated text");
 
```

**Returns:**
java.lang.String - Un testo del controllo.
### getType() {#getType}
```
public int getType()
```


Restituisce il tipo del controllo Forms 2.0.

 **Examples:** 

Mostra come modificare il testo del controllo OLE TextBox.

```

 Document doc = new Document(getMyDir() + "Textbox control.docm");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 TextBoxControl textBoxControl = (TextBoxControl)shape.getOleFormat().getOleControl();
 Assert.assertEquals(textBoxControl.getText(), "Aspose.Words test");

 textBoxControl.setText("Updated text");
 Assert.assertEquals(textBoxControl.getText(), "Updated text");
 
```

**Returns:**
int - Tipo di controllo Forms 2.0. Il valore restituito è una delle costanti [Forms2OleControlType](../../com.aspose.words/forms2olecontroltype/) constants.
### getValue() {#getValue}
```
public String getValue()
```


Ottiene la proprietà Value sottostante che spesso rappresenta lo stato del controllo. Per esempio, il pulsante di opzione selezionato ha valore '1' mentre quello non selezionato ha valore '0'. Il valore predefinito è una stringa vuota.

 **Examples:** 

Mostra come verificare le proprietà di un controllo ActiveX.

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
java.lang.String - Proprietà Value sottostante che spesso rappresenta lo stato del controllo.
### getWidth() {#getWidth}
```
public double getWidth()
```


Restituisce una larghezza del controllo in punti.

 **Examples:** 

Mostra come impostare le proprietà per il controllo ActiveX.

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
double - Una larghezza del controllo in punti.
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


Restituisce true se il controllo è un [Forms2OleControl](../../com.aspose.words/forms2olecontrol/).

 **Examples:** 

Mostra come verificare le proprietà di un controllo ActiveX.

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
boolean -  true  se il controllo è un [Forms2OleControl](../../com.aspose.words/forms2olecontrol/).
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


Imposta un colore di sfondo del controllo. Il valore predefinito dipende dal tipo di controllo.

 **Examples:** 

Mostra come impostare le proprietà per il controllo ActiveX.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.awt.Color | Un colore di sfondo del controllo. |

### setCaption(String value) {#setCaption-java.lang.String}
```
public void setCaption(String value)
```


Imposta la proprietà Caption del controllo. Il valore predefinito è una stringa vuota.

 **Examples:** 

Mostra come verificare le proprietà di un controllo ActiveX.

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

Mostra come impostare la didascalia per il controllo ActiveX.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl(); { button1.setCaption("Button caption"); }
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals("Button caption", button1.getCaption());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Una proprietà Caption del controllo. |

### setForeColor(Color value) {#setForeColor-java.awt.Color}
```
public void setForeColor(Color value)
```


Imposta un colore di primo piano del controllo. Il valore predefinito dipende dal tipo di controllo.

 **Examples:** 

Mostra come impostare le proprietà per il controllo ActiveX.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.awt.Color | Un colore di primo piano del controllo. |

### setGroupName(String value) {#setGroupName-java.lang.String}
```
public void setGroupName(String value)
```


Imposta una stringa che specifica un gruppo di controlli mutuamente esclusivi. Il valore predefinito è una stringa vuota.

 **Examples:** 

Mostra come verificare le proprietà di un controllo ActiveX.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Una stringa che specifica un gruppo di controlli mutuamente esclusivi. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


Imposta un'altezza del controllo in punti.

 **Examples:** 

Mostra come impostare le proprietà per il controllo ActiveX.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Un'altezza del controllo in punti. |

### setId(int value) {#setId-int}
```
public void setId(int value)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int |  |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Imposta il nome del controllo ActiveX.

 **Examples:** 

Mostra come verificare le proprietà di un controllo ActiveX.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Nome del controllo ActiveX. |

### setText(String value) {#setText-java.lang.String}
```
public void setText(String value)
```


Imposta il testo del controllo.

 **Examples:** 

Mostra come modificare il testo del controllo OLE TextBox.

```

 Document doc = new Document(getMyDir() + "Textbox control.docm");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 TextBoxControl textBoxControl = (TextBoxControl)shape.getOleFormat().getOleControl();
 Assert.assertEquals(textBoxControl.getText(), "Aspose.Words test");

 textBoxControl.setText("Updated text");
 Assert.assertEquals(textBoxControl.getText(), "Updated text");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Un testo del controllo. |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


Imposta una larghezza del controllo in punti.

 **Examples:** 

Mostra come impostare le proprietà per il controllo ActiveX.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Una larghezza del controllo in punti. |

