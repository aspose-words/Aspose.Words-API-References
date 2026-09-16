---
title: "Aspose::Words::Saving::IDocumentSavingCallback::Notify 方法"
linktitle: "Notify"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::IDocumentSavingCallback::Notify 方法。此方法在 C++ 中用于通知文档保存进度。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback::Notify method


此方法用于通知文档保存进度。

```cpp
virtual void Aspose::Words::Saving::IDocumentSavingCallback::Notify(System::SharedPtr<Aspose::Words::Saving::DocumentSavingArgs> args)=0
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| args | System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\> | 事件的参数。 |
## 备注


此接口的主要用途是允许应用程序代码获取进度状态并中止保存过程。

应在进度回调中抛出异常以中止加载，并在调用方代码中捕获该异常。

## 另见

* Class [DocumentSavingArgs](../../documentsavingargs/)
* Interface [IDocumentSavingCallback](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
