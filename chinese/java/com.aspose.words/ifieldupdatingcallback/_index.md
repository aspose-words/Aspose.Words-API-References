---
title: IFieldUpdatingCallback
second_title: Aspose.Words for Java API 参考
description: 如果您想在字段更新期间调用自己的自定义方法，请实现此接口。
type: docs
weight: 644
url: /zh/java/com.aspose.words/ifieldupdatingcallback/
---
```
public interface IFieldUpdatingCallback
```

如果您想在字段更新期间调用自己的自定义方法，请实现此接口。
## 方法

| 方法 | 描述 |
| --- | --- |
| [fieldUpdated(Field field)](#fieldUpdated-com.aspose.words.Field-) | 在字段更新后立即调用的用户定义方法。 |
| [fieldUpdating(Field field)](#fieldUpdating-com.aspose.words.Field-) | 在更新字段之前调用的用户定义方法。 |
### fieldUpdated(Field field) {#fieldUpdated-com.aspose.words.Field-}
```
public abstract void fieldUpdated(Field field)
```


在字段更新后立即调用的用户定义方法。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field) |  |

### fieldUpdating(Field field) {#fieldUpdating-com.aspose.words.Field-}
```
public abstract void fieldUpdating(Field field)
```


在更新字段之前调用的用户定义方法。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field) |  |
