---
title: Rule
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 36
url: /java/com.aspose.words.net.system.data/rule/
---

**Inheritance:**
java.lang.Object, java.lang.Enum
```
public enum Rule extends Enum<System.Data.Rule>
```

A utility class providing constants. Indicates the action that occurs when a [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) is enforced.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | No action taken on related rows. |
| [CASCADE](#CASCADE) | Delete or update related rows. |
| [SET_NULL](#SET-NULL) | Set values in related rows to DBNull. |
| [SET_DEFAULT](#SET-DEFAULT) | Set values in related rows to the value contained in the [DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn\#getDefaultValue--) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn\#setDefaultValue-java.lang.Object-) property. |
## Methods

| Method | Description |
| --- | --- |
| [values()](#values--) |  |
| [valueOf(String name)](#valueOf-java.lang.String-) |  |
### NONE {#NONE}
```
public static final System.Data.Rule NONE
```


No action taken on related rows.

### CASCADE {#CASCADE}
```
public static final System.Data.Rule CASCADE
```


Delete or update related rows. This is the default.

### SET_NULL {#SET-NULL}
```
public static final System.Data.Rule SET_NULL
```


Set values in related rows to DBNull.

### SET_DEFAULT {#SET-DEFAULT}
```
public static final System.Data.Rule SET_DEFAULT
```


Set values in related rows to the value contained in the [DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn\#getDefaultValue--) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn\#setDefaultValue-java.lang.Object-) property.

### values() {#values--}
```
public static System.Data.Rule[] values()
```




**Returns:**
com.aspose.words.net.System.Data.Rule[]
### valueOf(String name) {#valueOf-java.lang.String-}
```
public static System.Data.Rule valueOf(String name)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule)
