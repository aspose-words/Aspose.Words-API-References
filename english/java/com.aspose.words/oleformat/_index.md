---
title: OleFormat
second_title: Aspose.Words for Java API Reference
description: Provides access to the data of an OLE object or ActiveX control.
type: docs
weight: 425
url: /java/com.aspose.words/oleformat/
---

**Inheritance:**
java.lang.Object
```
public class OleFormat
```

Provides access to the data of an OLE object or ActiveX control.

To learn more, visit the **Working with Ole Objects** documentation article.

Use the [Shape.getOleFormat()](../../com.aspose.words/shape\#getOleFormat--) property to access the data of an OLE object. You do not create instances of the [OleFormat](../../com.aspose.words/oleformat) class directly.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAutoUpdate()](#getAutoUpdate--) | Specifies whether the link to the OLE object is automatically updated or not in Microsoft Word. |
| [getClass()](#getClass--) |  |
| [getClsid()](#getClsid--) | Gets the CLSID of the OLE object. |
| [getIconCaption()](#getIconCaption--) | Gets icon caption of OLE object. |
| [getOleControl()](#getOleControl--) | Gets [getOleControl()](../../com.aspose.words/oleformat\#getOleControl--) objects if this OLE object is an ActiveX control. |
| [getOleEntry(String oleEntryName)](#getOleEntry-java.lang.String-) |  |
| [getOleIcon()](#getOleIcon--) | Gets the draw aspect of the OLE object. |
| [getOlePackage()](#getOlePackage--) | Provide access to [OlePackage](../../com.aspose.words/olepackage) if OLE object is an OLE Package. |
| [getProgId()](#getProgId--) | Gets the ProgID of the OLE object. |
| [getRawData()](#getRawData--) | Gets OLE object raw data. |
| [getSourceFullName()](#getSourceFullName--) | Gets the path and name of the source file for the linked OLE object. |
| [getSourceItem()](#getSourceItem--) | Gets a string that is used to identify the portion of the source file that is being linked. |
| [getSuggestedExtension()](#getSuggestedExtension--) | Gets the file extension suggested for the current embedded object if you want to save it into a file. |
| [getSuggestedFileName()](#getSuggestedFileName--) | Gets the file name suggested for the current embedded object if you want to save it into a file. |
| [hashCode()](#hashCode--) |  |
| [isLink()](#isLink--) | Returns true if the OLE object is linked (when [getSourceFullName()](../../com.aspose.words/oleformat\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat\#setSourceFullName-java.lang.String-) is specified). |
| [isLocked()](#isLocked--) | Specifies whether the link to the OLE object is locked from updates. |
| [isLocked(boolean value)](#isLocked-boolean-) | Specifies whether the link to the OLE object is locked from updates. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [save(OutputStream stream)](#save-java.io.OutputStream-) |  |
| [save(String fileName)](#save-java.lang.String-) | Saves the data of the embedded object into a file with the specified name. |
| [setAutoUpdate(boolean value)](#setAutoUpdate-boolean-) | Specifies whether the link to the OLE object is automatically updated or not in Microsoft Word. |
| [setProgId(String value)](#setProgId-java.lang.String-) | Sets the ProgID of the OLE object. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String-) | Sets the path and name of the source file for the linked OLE object. |
| [setSourceItem(String value)](#setSourceItem-java.lang.String-) | Sets a string that is used to identify the portion of the source file that is being linked. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getAutoUpdate() {#getAutoUpdate--}
```
public boolean getAutoUpdate()
```


Specifies whether the link to the OLE object is automatically updated or not in Microsoft Word.

The default value is **false**.

**Returns:**
boolean - The corresponding  boolean  value.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getClsid() {#getClsid--}
```
public UUID getClsid()
```


Gets the CLSID of the OLE object.

**Returns:**
java.util.UUID - The CLSID of the OLE object.
### getIconCaption() {#getIconCaption--}
```
public String getIconCaption()
```


Gets icon caption of OLE object.

In case of OLE object is not embedded as icon or caption couldn't be retrieved returns empty string.

**Returns:**
java.lang.String - Icon caption of OLE object.
### getOleControl() {#getOleControl--}
```
public OleControl getOleControl()
```


Gets [getOleControl()](../../com.aspose.words/oleformat\#getOleControl--) objects if this OLE object is an ActiveX control. Otherwise this property is null.

**Returns:**
[OleControl](../../com.aspose.words/olecontrol) - \{[getOleControl()](../../com.aspose.words/oleformat\#getOleControl--) objects if this OLE object is an ActiveX control.
### getOleEntry(String oleEntryName) {#getOleEntry-java.lang.String-}
```
public byte[] getOleEntry(String oleEntryName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| oleEntryName | java.lang.String |  |

**Returns:**
byte[]
### getOleIcon() {#getOleIcon--}
```
public boolean getOleIcon()
```


Gets the draw aspect of the OLE object. When **true**, the OLE object is displayed as an icon. When **false**, the OLE object is displayed as content.

Aspose.Words does not allow to set this property to avoid confusion. If you were able to change the draw aspect in Aspose.Words, Microsoft Word would still display the OLE object in its original draw aspect until you edit or update the OLE object in Microsoft Word.

**Returns:**
boolean - The draw aspect of the OLE object.
### getOlePackage() {#getOlePackage--}
```
public OlePackage getOlePackage()
```


Provide access to [OlePackage](../../com.aspose.words/olepackage) if OLE object is an OLE Package. Returns null otherwise. OLE Package is a legacy technology that allows to wrap any file format not present in the OLE registry of a Windows system into a generic package allowing to embed almost anything into a document. See [OlePackage](../../com.aspose.words/olepackage) type for more info.

**Returns:**
[OlePackage](../../com.aspose.words/olepackage) - The corresponding [OlePackage](../../com.aspose.words/olepackage) value.
### getProgId() {#getProgId--}
```
public String getProgId()
```


Gets the ProgID of the OLE object.

The ProgID property is not always present in Microsoft Word documents and cannot be relied upon.

Cannot be null.

The default value is an empty string.

**Returns:**
java.lang.String - The ProgID of the OLE object.
### getRawData() {#getRawData--}
```
public byte[] getRawData()
```


Gets OLE object raw data.

**Returns:**
byte[]
### getSourceFullName() {#getSourceFullName--}
```
public String getSourceFullName()
```


Gets the path and name of the source file for the linked OLE object.

The default value is an empty string.

If [getSourceFullName()](../../com.aspose.words/oleformat\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat\#setSourceFullName-java.lang.String-) is not an empty string, the OLE object is linked.

**Returns:**
java.lang.String - The path and name of the source file for the linked OLE object.
### getSourceItem() {#getSourceItem--}
```
public String getSourceItem()
```


Gets a string that is used to identify the portion of the source file that is being linked.

The default value is an empty string.

For example, if the source file is a Microsoft Excel workbook, the [getSourceItem()](../../com.aspose.words/oleformat\#getSourceItem--) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat\#setSourceItem-java.lang.String-) property might return "Workbook1!R3C1:R4C2" if the OLE object contains only a few cells from the worksheet.

**Returns:**
java.lang.String - A string that is used to identify the portion of the source file that is being linked.
### getSuggestedExtension() {#getSuggestedExtension--}
```
public String getSuggestedExtension()
```


Gets the file extension suggested for the current embedded object if you want to save it into a file.

**Returns:**
java.lang.String - The file extension suggested for the current embedded object if you want to save it into a file.
### getSuggestedFileName() {#getSuggestedFileName--}
```
public String getSuggestedFileName()
```


Gets the file name suggested for the current embedded object if you want to save it into a file.

**Returns:**
java.lang.String - The file name suggested for the current embedded object if you want to save it into a file.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### isLink() {#isLink--}
```
public boolean isLink()
```


Returns true if the OLE object is linked (when [getSourceFullName()](../../com.aspose.words/oleformat\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat\#setSourceFullName-java.lang.String-) is specified).

**Returns:**
boolean - True if the OLE object is linked (when [getSourceFullName()](../../com.aspose.words/oleformat\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat\#setSourceFullName-java.lang.String-) is specified).
### isLocked() {#isLocked--}
```
public boolean isLocked()
```


Specifies whether the link to the OLE object is locked from updates.

The default value is **false**.

**Returns:**
boolean - The corresponding  boolean  value.
### isLocked(boolean value) {#isLocked-boolean-}
```
public void isLocked(boolean value)
```


Specifies whether the link to the OLE object is locked from updates.

The default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### save(OutputStream stream) {#save-java.io.OutputStream-}
```
public void save(OutputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String-}
```
public void save(String fileName)
```


Saves the data of the embedded object into a file with the specified name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Name of the file to save the OLE object data. |

### setAutoUpdate(boolean value) {#setAutoUpdate-boolean-}
```
public void setAutoUpdate(boolean value)
```


Specifies whether the link to the OLE object is automatically updated or not in Microsoft Word.

The default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setProgId(String value) {#setProgId-java.lang.String-}
```
public void setProgId(String value)
```


Sets the ProgID of the OLE object.

The ProgID property is not always present in Microsoft Word documents and cannot be relied upon.

Cannot be null.

The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The ProgID of the OLE object. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String-}
```
public void setSourceFullName(String value)
```


Sets the path and name of the source file for the linked OLE object.

The default value is an empty string.

If [getSourceFullName()](../../com.aspose.words/oleformat\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat\#setSourceFullName-java.lang.String-) is not an empty string, the OLE object is linked.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The path and name of the source file for the linked OLE object. |

### setSourceItem(String value) {#setSourceItem-java.lang.String-}
```
public void setSourceItem(String value)
```


Sets a string that is used to identify the portion of the source file that is being linked.

The default value is an empty string.

For example, if the source file is a Microsoft Excel workbook, the [getSourceItem()](../../com.aspose.words/oleformat\#getSourceItem--) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat\#setSourceItem-java.lang.String-) property might return "Workbook1!R3C1:R4C2" if the OLE object contains only a few cells from the worksheet.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A string that is used to identify the portion of the source file that is being linked. |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

