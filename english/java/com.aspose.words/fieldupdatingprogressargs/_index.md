---
title: FieldUpdatingProgressArgs
linktitle: FieldUpdatingProgressArgs
second_title: Aspose.Words for Java
description: Provides data for the field updating progress event in Java.
type: docs
weight: 280
url: /java/com.aspose.words/fieldupdatingprogressargs/
---

**Inheritance:**
java.lang.Object
```
public class FieldUpdatingProgressArgs
```

Provides data for the field updating progress event.
## Methods

| Method | Description |
| --- | --- |
| [getTotalFieldsCount()](#getTotalFieldsCount) | Gets the total fields count to be updated. |
| [getUpdateCompleted()](#getUpdateCompleted) | Gets a value indicating whether field updating is completed. |
| [getUpdatedFieldsCount()](#getUpdatedFieldsCount) | Gets the number of updated fields. |
### getTotalFieldsCount() {#getTotalFieldsCount}
```
public int getTotalFieldsCount()
```


Gets the total fields count to be updated.

 **Remarks:** 

The value is not constant and may be increased during updating process.

**Returns:**
int - The total fields count to be updated.
### getUpdateCompleted() {#getUpdateCompleted}
```
public boolean getUpdateCompleted()
```


Gets a value indicating whether field updating is completed.

**Returns:**
boolean - A value indicating whether field updating is completed.
### getUpdatedFieldsCount() {#getUpdatedFieldsCount}
```
public int getUpdatedFieldsCount()
```


Gets the number of updated fields.

**Returns:**
int - The number of updated fields.
