---
title: Notify
second_title: Aspose.Words for C++ API Reference
description: This is called to notify of document saving progress.
type: docs
weight: 40
url: /cpp/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback::Notify method


This is called to notify of document saving progress.

```cpp
virtual void Aspose::Words::Saving::IDocumentSavingCallback::Notify(System::SharedPtr<Aspose::Words::Saving::DocumentSavingArgs> args)=0
```


| Parameter | Type | Description |
| --- | --- | --- |
| args | System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\> | An argument of the event. |
## Remarks


The primary uses for this interface is to allow application code to obtain progress status and abort saving process.

An exception should be threw from the progress callback for abortion and it should be caught in the consumer code.

## See Also

* Class [DocumentSavingArgs](../../documentsavingargs/)
* Interface [IDocumentSavingCallback](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
