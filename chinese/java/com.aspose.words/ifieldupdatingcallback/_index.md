---
title: I字段UpdatingCallback
second_title: Aspose.Words for Java API Reference
description: 如果您想在字段更新期间调用自己的自定义方法，请实现此接口。
type: docs
weight: 644
url: /zh/java/com.aspose.words/ifieldupdatingcallback/
---
```
public interface I字段UpdatingCallback
```

如果您想在字段更新期间调用自己的自定义方法，请实现此接口。
## 方法

| 方法 | 描述 |
| --- | --- |
| [fieldUpdated(字段 field)](#fieldUpdated-com.aspose.words.字段-) | 在字段更新后立即调用的用户定义方法。 |
| [fieldUpdating(字段 field)](#fieldUpdating-com.aspose.words.字段-) | 在字段更新之前调用的用户定义方法。 |
### fieldUpdated(字段 field) {#fieldUpdated-com.aspose.words.字段-}
```
public abstract void fieldUpdated(字段 field)
```


在字段更新后立即调用的用户定义方法。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| field | [字段](../../com.aspose.words/field) |  |

### fieldUpdating(字段 field) {#fieldUpdating-com.aspose.words.字段-}
```
public abstract void fieldUpdating(字段 field)
```


在字段更新之前调用的用户定义方法。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| field | [字段](../../com.aspose.words/field) |  |
