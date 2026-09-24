---
title: "OptionButtonControl"
linktitle: "OptionButtonControl"
second_title: "Aspose.Words Java için"
description: "OptionButton kontrolü, Java'da birbirini dışlayan sınırlı bir seçenek kümesinde tek bir seçim yapılmasını sağlar."
type: docs
weight: 506
url: /tr/java/com.aspose.words/optionbuttoncontrol/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.OleControl](../../com.aspose.words/olecontrol/), [com.aspose.words.Forms2OleControl](../../com.aspose.words/forms2olecontrol/), [com.aspose.words.MorphDataControl](../../com.aspose.words/morphdatacontrol/)
```
public class OptionButtonControl extends MorphDataControl
```

OptionButton denetimi, sınırlı bir karşılıklı dışlayıcı seçim kümesinde tek bir seçeneği etkinleştirir.

 **Examples:** 

Radyo düğmesinin nasıl seçileceğini gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getBackColor()](#getBackColor) | Kontrolün arka plan rengini alır. |
| [getCaption()](#getCaption) | Kontrolün Caption özelliğini alır. |
| [getChildNodes()](#getChildNodes) | Doğrudan alt kontrol koleksiyonunu alır. |
| [getClsidInternal()](#getClsidInternal) |  |
| [getEnabled()](#getEnabled) | Kontrol etkin durumdaysa  true  döndürür. |
| [getExtensionForUser(String progId)](#getExtensionForUser-java.lang.String) |  |
| [getFileNameForUser()](#getFileNameForUser) |  |
| [getForeColor()](#getForeColor) | Kontrolün ön plan rengini alır. |
| [getGroupName()](#getGroupName) | Karşılıklı olarak birbirini dışlayan kontroller grubunu belirten bir dize alır. |
| [getHeight()](#getHeight) | Kontrolün yüksekliğini puan cinsinden alır. |
| [getId()](#getId) |  |
| [getName()](#getName) | ActiveX kontrolünün adını alır. |
| [getSelected()](#getSelected) | Bu [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) seçili mi değil mi gösteren bir boolean değer alır. |
| [getType()](#getType) | Forms 2.0 kontrolünün tipini alır. |
| [getValue()](#getValue) | Genellikle kontrol durumunu temsil eden temel Value özelliğini alır. |
| [getWidth()](#getWidth) | Kontrolün genişliğini puan cinsinden alır. |
| [isEmpty()](#isEmpty) |  |
| [isForms2OleControl()](#isForms2OleControl) | Kontrol bir [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) ise  true  döndürür. |
| [isForms2OleControlInternal()](#isForms2OleControlInternal) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Kontrolün arka plan rengini ayarlar. |
| [setCaption(String value)](#setCaption-java.lang.String) | Kontrolün Caption özelliğini ayarlar. |
| [setForeColor(Color value)](#setForeColor-java.awt.Color) | Kontrolün ön plan rengini ayarlar. |
| [setGroupName(String value)](#setGroupName-java.lang.String) | Birbirini dışlayan kontroller grubunu belirten bir dize ayarlar. |
| [setHeight(double value)](#setHeight-double) | Kontrolün yüksekliğini puan cinsinden ayarlar. |
| [setId(int value)](#setId-int) |  |
| [setName(String value)](#setName-java.lang.String) | ActiveX kontrolünün adını ayarlar. |
| [setSelected(boolean value)](#setSelected-boolean) | Bu [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) seçili mi değil mi gösteren bir boolean değer ayarlar. |
| [setWidth(double value)](#setWidth-double) | Kontrolün genişliğini puan cinsinden ayarlar. |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Kontrolün arka plan rengini alır. Varsayılan değer kontrolün tipine bağlıdır.

 **Examples:** 

ActiveX kontrolü için özelliklerin nasıl ayarlanacağını gösterir.

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
java.awt.Color - Kontrolün arka plan rengi.
### getCaption() {#getCaption}
```
public String getCaption()
```


Kontrolün Caption özelliğini alır. Varsayılan değer boş bir dizedir.

 **Examples:** 

ActiveX kontrolünün özelliklerinin nasıl doğrulanacağını gösterir.

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

ActiveX kontrolü için başlığın nasıl ayarlanacağını gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl(); { button1.setCaption("Button caption"); }
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals("Button caption", button1.getCaption());
 
```

**Returns:**
java.lang.String - Kontrolün Caption özelliği.
### getChildNodes() {#getChildNodes}
```
public Forms2OleControlCollection getChildNodes()
```


Doğrudan alt kontrol koleksiyonunu alır.

 **Remarks:** 

Bu kontrolün alt öğeleri olamaması durumunda  null  döndürür.

 **Examples:** 

ActiveX kontrolünün özelliklerinin nasıl doğrulanacağını gösterir.

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


Kontrol etkin durumdaysa  true  döndürür.

 **Examples:** 

ActiveX kontrolünün özelliklerinin nasıl doğrulanacağını gösterir.

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
boolean -  true  eğer kontrol etkin durumdaysa.
### getExtensionForUser(String progId) {#getExtensionForUser-java.lang.String}
```
public String getExtensionForUser(String progId)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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


Kontrolün ön plan rengini alır. Varsayılan değer kontrolün tipine bağlıdır.

 **Examples:** 

ActiveX kontrolü için özelliklerin nasıl ayarlanacağını gösterir.

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
java.awt.Color - Kontrolün ön plan rengi.
### getGroupName() {#getGroupName}
```
public String getGroupName()
```


Birbirini dışlayan kontroller grubunu belirten bir dize alır. Varsayılan değer boş bir dizedir.

 **Examples:** 

ActiveX kontrolünün özelliklerinin nasıl doğrulanacağını gösterir.

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
java.lang.String - Birbirini dışlayan kontroller grubunu belirten bir dize.
### getHeight() {#getHeight}
```
public double getHeight()
```


Kontrolün yüksekliğini puan cinsinden alır.

 **Examples:** 

ActiveX kontrolü için özelliklerin nasıl ayarlanacağını gösterir.

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
double - Kontrolün puan cinsinden yüksekliği.
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


ActiveX kontrolünün adını alır.

 **Examples:** 

ActiveX kontrolünün özelliklerinin nasıl doğrulanacağını gösterir.

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
java.lang.String - ActiveX kontrolünün adı.
### getSelected() {#getSelected}
```
public boolean getSelected()
```


Bu [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) seçili mi değil mi gösteren bir boolean değer alır.

 **Remarks:** 

Not, bu özellik aynı [Forms2OleControl.getGroupName()](../../com.aspose.words/forms2olecontrol/\#getGroupName) / [Forms2OleControl.setGroupName(java.lang.String)](../../com.aspose.words/forms2olecontrol/\#setGroupName-java.lang.String) ile bir grup [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) içinde birden fazla öğe seçmenize izin verir. Bu [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) seçili yaparken, daha önce seçili olan öğenin seçimini kaldırmayı sizin sorumluluğunuzdadır.

 **Examples:** 

Radyo düğmesinin nasıl seçileceğini gösterir.

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
boolean - Bu [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) seçili mi değil mi gösteren bir boolean değer.
### getType() {#getType}
```
public int getType()
```


Forms 2.0 kontrolünün tipini alır.

 **Examples:** 

Radyo düğmesinin nasıl seçileceğini gösterir.

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
int - Forms 2.0 kontrolünün tipi. Döndürülen değer [Forms2OleControlType](../../com.aspose.words/forms2olecontroltype/) sabitlerinden biridir.
### getValue() {#getValue}
```
public String getValue()
```


Temel Value özelliğini alır; bu genellikle kontrol durumunu temsil eder. Örneğin işaretli seçenek düğmesi '1' değerine, işaretsiz olan ise '0' değerine sahiptir. Varsayılan değer boş bir dizedir.

 **Examples:** 

ActiveX kontrolünün özelliklerinin nasıl doğrulanacağını gösterir.

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
java.lang.String - Temel Value özelliği, genellikle kontrol durumunu temsil eder.
### getWidth() {#getWidth}
```
public double getWidth()
```


Kontrolün genişliğini puan cinsinden alır.

 **Examples:** 

ActiveX kontrolü için özelliklerin nasıl ayarlanacağını gösterir.

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
double - Kontrolün nokta cinsinden genişliği.
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


Kontrol bir [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) ise  true  döndürür.

 **Examples:** 

ActiveX kontrolünün özelliklerinin nasıl doğrulanacağını gösterir.

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
boolean -  true  eğer kontrol bir [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) ise.
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


Kontrolün arka plan rengini ayarlar. Varsayılan değer kontrolün türüne bağlıdır.

 **Examples:** 

ActiveX kontrolü için özelliklerin nasıl ayarlanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | Kontrolün arka plan rengi. |

### setCaption(String value) {#setCaption-java.lang.String}
```
public void setCaption(String value)
```


Kontrolün Caption özelliğini ayarlar. Varsayılan değer boş bir dizedir.

 **Examples:** 

ActiveX kontrolünün özelliklerinin nasıl doğrulanacağını gösterir.

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

ActiveX kontrolü için başlığın nasıl ayarlanacağını gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl(); { button1.setCaption("Button caption"); }
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals("Button caption", button1.getCaption());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Kontrolün Caption özelliği. |

### setForeColor(Color value) {#setForeColor-java.awt.Color}
```
public void setForeColor(Color value)
```


Kontrolün ön plan rengini ayarlar. Varsayılan değer kontrolün türüne bağlıdır.

 **Examples:** 

ActiveX kontrolü için özelliklerin nasıl ayarlanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | Kontrolün ön plan rengi. |

### setGroupName(String value) {#setGroupName-java.lang.String}
```
public void setGroupName(String value)
```


Birbirini dışlayan kontrol grubunu belirten bir dize ayarlar. Varsayılan değer boş bir dizedir.

 **Examples:** 

ActiveX kontrolünün özelliklerinin nasıl doğrulanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Birbirini dışlayan kontrol grubunu belirten bir dize. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


Kontrolün yüksekliğini puan cinsinden ayarlar.

 **Examples:** 

ActiveX kontrolü için özelliklerin nasıl ayarlanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Kontrolün nokta cinsinden yüksekliği. |

### setId(int value) {#setId-int}
```
public void setId(int value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int |  |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


ActiveX kontrolünün adını ayarlar.

 **Examples:** 

ActiveX kontrolünün özelliklerinin nasıl doğrulanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | ActiveX kontrolünün adı. |

### setSelected(boolean value) {#setSelected-boolean}
```
public void setSelected(boolean value)
```


Bu [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) seçili mi değil mi gösteren bir boolean değer ayarlar.

 **Remarks:** 

Not, bu özellik aynı [Forms2OleControl.getGroupName()](../../com.aspose.words/forms2olecontrol/\#getGroupName) / [Forms2OleControl.setGroupName(java.lang.String)](../../com.aspose.words/forms2olecontrol/\#setGroupName-java.lang.String) ile bir grup [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) içinde birden fazla öğe seçmenize izin verir. Bu [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) seçili yaparken, daha önce seçili olan öğenin seçimini kaldırmayı sizin sorumluluğunuzdadır.

 **Examples:** 

Radyo düğmesinin nasıl seçileceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | boolean | Bu [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) seçili mi değil mi gösteren bir boolean değer. |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


Kontrolün genişliğini puan cinsinden ayarlar.

 **Examples:** 

ActiveX kontrolü için özelliklerin nasıl ayarlanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Kontrolün nokta cinsinden genişliği. |

