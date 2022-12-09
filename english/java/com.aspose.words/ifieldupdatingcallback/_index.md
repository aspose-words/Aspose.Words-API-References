---
title: IFieldUpdatingCallback
second_title: Aspose.Words for Java API Reference
description: Implement this interface if you want to have your own custom methods called during a field update.
type: docs
weight: 647
url: /java/com.aspose.words/ifieldupdatingcallback/
---
```
public interface IFieldUpdatingCallback
```

Implement this interface if you want to have your own custom methods called during a field update.
## Methods

| Method | Description |
| --- | --- |
| [fieldUpdated(Field field)](#fieldUpdated-com.aspose.words.Field) | A user defined method that is called just after a field is updated. |
| [fieldUpdating(Field field)](#fieldUpdating-com.aspose.words.Field) | A user defined method that is called just before a field is updated. |
### fieldUpdated(Field field) {#fieldUpdated-com.aspose.words.Field}
```
public abstract void fieldUpdated(Field field)
```


A user defined method that is called just after a field is updated.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field) |  |

### fieldUpdating(Field field) {#fieldUpdating-com.aspose.words.Field}
```
public abstract void fieldUpdating(Field field)
```


A user defined method that is called just before a field is updated.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field) |  |

