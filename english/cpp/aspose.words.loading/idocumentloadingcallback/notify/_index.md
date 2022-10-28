---
title: Notify
second_title: Aspose.Words for C++ API Reference
description: This is called to notify of document loading progress.
type: docs
weight: 1
url: /cpp/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback.Notify method


This is called to notify of document loading progress.

```cpp
virtual void Aspose::Words::Loading::IDocumentLoadingCallback::Notify(System::SharedPtr<Aspose::Words::Loading::DocumentLoadingArgs> args)=0
```


| Parameter | Type | Description |
| --- | --- | --- |
| args | System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\> | An argument of the event. |

The primary uses for this interface is to allow application code to obtain progress status and abort loading process.

An exception should be threw from the progress callback for abortion and it should be caught in the consumer code.


