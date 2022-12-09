---
title: IReplacingCallback
second_title: Aspose.Words for Java API Reference
description: Implement this interface if you want to have your own custom method called during a find and replace operation.
type: docs
weight: 659
url: /java/com.aspose.words/ireplacingcallback/
---
```
public interface IReplacingCallback
```

Implement this interface if you want to have your own custom method called during a find and replace operation.
## Methods

| Method | Description |
| --- | --- |
| [replacing(ReplacingArgs args)](#replacing-com.aspose.words.ReplacingArgs) | A user defined method that is called during a replace operation for each match found just before a replace is made. |
### replacing(ReplacingArgs args) {#replacing-com.aspose.words.ReplacingArgs}
```
public abstract int replacing(ReplacingArgs args)
```


A user defined method that is called during a replace operation for each match found just before a replace is made.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| args | [ReplacingArgs](../../com.aspose.words/replacingargs) |  |

**Returns:**
int - A [ReplaceAction](../../com.aspose.words/replaceaction) value that specifies the action to be taken for the current match. The returned value is one of [ReplaceAction](../../com.aspose.words/replaceaction) constants.
