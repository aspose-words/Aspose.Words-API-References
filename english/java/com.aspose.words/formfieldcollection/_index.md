---
title: FormFieldCollection
second_title: Aspose.Words for Java API Reference
description: A collection of  objects that represent all the form fields in a range.
type: docs
weight: 299
url: /java/com.aspose.words/formfieldcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class FormFieldCollection implements Iterable
```

A collection of [FormField](../../com.aspose.words/formfield) objects that represent all the form fields in a range.

To learn more, visit the [ Working with Form Fields ][Working with Form Fields] documentation article.


[Working with Form Fields]: https://docs.aspose.com/words/java/working-with-form-fields/
## Methods

| Method | Description |
| --- | --- |
| [clear()](#clear) | Removes all form fields from this collection and from the document. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int index)](#get-int) | Returns a form field at the specified index. |
| [get(String bookmarkName)](#get-java.lang.String) | Returns a form field by bookmark name. |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) | Returns the number of form fields in the collection. |
| [hashCode()](#hashCode) |  |
| [iterator()](#iterator) | Returns an enumerator object. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove(String formField)](#remove-java.lang.String) | Removes a form field with the specified name. |
| [removeAt(int index)](#removeAt-int) | Removes a form field at the specified index. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### clear() {#clear}
```
public void clear()
```


Removes all form fields from this collection and from the document.

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### get(int index) {#get-int}
```
public FormField get(int index)
```


Returns a form field at the specified index.

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[FormField](../../com.aspose.words/formfield) - A form field at the specified index.
### get(String bookmarkName) {#get-java.lang.String}
```
public FormField get(String bookmarkName)
```


Returns a form field by bookmark name. Returns  null  if the form field with the specified bookmark name cannot be found.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Case-insensitive bookmark name. |

**Returns:**
[FormField](../../com.aspose.words/formfield) - A form field by bookmark name.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCount() {#getCount}
```
public int getCount()
```


Returns the number of form fields in the collection.

**Returns:**
int - The number of form fields in the collection.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an enumerator object.

**Returns:**
java.util.Iterator
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### remove(String formField) {#remove-java.lang.String}
```
public void remove(String formField)
```


Removes a form field with the specified name. If there is a bookmark associated with the form field, the bookmark is not removed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| formField | java.lang.String | The case-insensitive name of the form field to remove. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Removes a form field at the specified index. If there is a bookmark associated with the form field, the bookmark is not removed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the form field to remove. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

