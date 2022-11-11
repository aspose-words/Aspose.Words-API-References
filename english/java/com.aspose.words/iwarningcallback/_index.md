---
title: IWarningCallback
second_title: Aspose.Words for Java API Reference
description: Implement this interface if you want to have your own custom method called to capture loss of fidelity warnings that can occur during document loading or saving.
type: docs
weight: 661
url: /java/com.aspose.words/iwarningcallback/
---
```
public interface IWarningCallback
```

Implement this interface if you want to have your own custom method called to capture loss of fidelity warnings that can occur during document loading or saving.
## Methods

| Method | Description |
| --- | --- |
| [warning(WarningInfo info)](#warning-com.aspose.words.WarningInfo-) | Aspose.Words invokes this method when it encounters some issue during document loading or saving that might result in loss of formatting or data fidelity. |
### warning(WarningInfo info) {#warning-com.aspose.words.WarningInfo-}
```
public abstract void warning(WarningInfo info)
```


Aspose.Words invokes this method when it encounters some issue during document loading or saving that might result in loss of formatting or data fidelity.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| info | [WarningInfo](../../com.aspose.words/warninginfo) |  |

