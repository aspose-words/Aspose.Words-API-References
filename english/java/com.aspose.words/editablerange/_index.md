---
title: EditableRange
second_title: Aspose.Words for Java API Reference
description: Represents a single editable range.
type: docs
weight: 136
url: /java/com.aspose.words/editablerange/
---

**Inheritance:**
java.lang.Object
```
public class EditableRange
```

Represents a single editable range.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

[EditableRange](../../com.aspose.words/editablerange) is a "facade" object that encapsulates two nodes [getEditableRangeStart()](../../com.aspose.words/editablerange\#getEditableRangeStart--) and [getEditableRangeEnd()](../../com.aspose.words/editablerange\#getEditableRangeEnd--) in a document tree and allows to work with an editable range as a single object.
## Methods

| Method | Description |
| --- | --- |
| [remove()](#remove--) | Removes the editable range from the document. |
| [getId()](#getId--) | Gets the editable range identifier. |
| [getSingleUser()](#getSingleUser--) | Gets the single user for editable range. |
| [setSingleUser(String value)](#setSingleUser-java.lang.String-) | Sets the single user for editable range. |
| [getEditorGroup()](#getEditorGroup--) | Gets an alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range. |
| [setEditorGroup(int value)](#setEditorGroup-int-) | Sets an alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range. |
| [getEditableRangeStart()](#getEditableRangeStart--) | Gets the node that represents the start of the editable range. |
| [getEditableRangeEnd()](#getEditableRangeEnd--) | Gets the node that represents the end of the editable range. |
### remove() {#remove--}
```
public void remove()
```


Removes the editable range from the document. Does not remove content inside the editable range.

### getId() {#getId--}
```
public int getId()
```


Gets the editable range identifier.

The region must be demarcated using the [getEditableRangeStart()](../../com.aspose.words/editablerange\#getEditableRangeStart--) and [getEditableRangeEnd()](../../com.aspose.words/editablerange\#getEditableRangeEnd--)

Editable range identifiers are supposed to be unique across a document and Aspose.Words automatically maintains editable range identifiers when loading, saving and combining documents.

**Returns:**
int - The editable range identifier.
### getSingleUser() {#getSingleUser--}
```
public String getSingleUser()
```


Gets the single user for editable range.

This editor can be stored in one of the following forms:

DOMAIN\\Username - for users whose access shall be authenticated using the current user's domain credentials.

user@domain.com - for users whose access shall be authenticated using the user's e-mail address as credentials.

user - for users whose access shall be authenticated using the current user's machine credentials.

Single user and editor group cannot be set simultaneously for the specific editable range, if the one is set, the other will be clear.

**Returns:**
java.lang.String - The single user for editable range.
### setSingleUser(String value) {#setSingleUser-java.lang.String-}
```
public void setSingleUser(String value)
```


Sets the single user for editable range.

This editor can be stored in one of the following forms:

DOMAIN\\Username - for users whose access shall be authenticated using the current user's domain credentials.

user@domain.com - for users whose access shall be authenticated using the user's e-mail address as credentials.

user - for users whose access shall be authenticated using the current user's machine credentials.

Single user and editor group cannot be set simultaneously for the specific editable range, if the one is set, the other will be clear.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The single user for editable range. |

### getEditorGroup() {#getEditorGroup--}
```
public int getEditorGroup()
```


Gets an alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range.

Single user and editor group cannot be set simultaneously for the specific editable range, if the one is set, the other will be clear.

**Returns:**
int - An alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range. The returned value is one of [EditorType](../../com.aspose.words/editortype) constants.
### setEditorGroup(int value) {#setEditorGroup-int-}
```
public void setEditorGroup(int value)
```


Sets an alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range.

Single user and editor group cannot be set simultaneously for the specific editable range, if the one is set, the other will be clear.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | An alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range. The value must be one of [EditorType](../../com.aspose.words/editortype) constants. |

### getEditableRangeStart() {#getEditableRangeStart--}
```
public EditableRangeStart getEditableRangeStart()
```


Gets the node that represents the start of the editable range.

**Returns:**
[EditableRangeStart](../../com.aspose.words/editablerangestart) - The node that represents the start of the editable range.
### getEditableRangeEnd() {#getEditableRangeEnd--}
```
public EditableRangeEnd getEditableRangeEnd()
```


Gets the node that represents the end of the editable range.

**Returns:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend) - The node that represents the end of the editable range.
