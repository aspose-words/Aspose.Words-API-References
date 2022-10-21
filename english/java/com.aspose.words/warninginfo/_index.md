---
title: WarningInfo
second_title: Aspose.Words for Java API Reference
description: Contains information about a warning that Aspose.Words issued during document loading or saving.
type: docs
weight: 604
url: /java/com.aspose.words/warninginfo/
---

**Inheritance:**
java.lang.Object
```
public class WarningInfo
```

Contains information about a warning that Aspose.Words issued during document loading or saving.

To learn more, visit the **Programming with Documents** documentation article.

You do not create instances of this class. Objects of this class are created and passed by Aspose.Words to the [IWarningCallback.warning(com.aspose.words.WarningInfo)](../../com.aspose.words/iwarningcallback\#warning-com.aspose.words.WarningInfo-) method.
## Methods

| Method | Description |
| --- | --- |
| [getWarningType()](#getWarningType--) | Returns the type of the warning. |
| [getDescription()](#getDescription--) | Returns the description of the warning. |
| [getSource()](#getSource--) | Returns the source of the warning. |
### getWarningType() {#getWarningType--}
```
public int getWarningType()
```


Returns the type of the warning.

**Returns:**
int - The type of the warning. The returned value is a bitwise combination of [WarningType](../../com.aspose.words/warningtype) constants.
### getDescription() {#getDescription--}
```
public String getDescription()
```


Returns the description of the warning.

**Returns:**
java.lang.String - The description of the warning.
### getSource() {#getSource--}
```
public int getSource()
```


Returns the source of the warning.

**Returns:**
int - The source of the warning. The returned value is one of [WarningSource](../../com.aspose.words/warningsource) constants.
