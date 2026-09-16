---
title: "Aspose::Words::Loading::IDocumentLoadingCallback::Notify 方法"
linktitle: "Notify"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::IDocumentLoadingCallback::Notify 方法。 此方法在 C++ 中用于通知文档加载进度。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback::Notify method


此方法在通知文档加载进度时被调用。

```cpp
virtual void Aspose::Words::Loading::IDocumentLoadingCallback::Notify(System::SharedPtr<Aspose::Words::Loading::DocumentLoadingArgs> args)=0
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| args | System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\> | 事件的参数。 |
## 备注


此接口的主要用途是允许应用程序代码获取进度状态并中止加载过程。

应在进度回调中抛出异常以中止加载，并在调用方代码中捕获该异常。

## 另见

* Class [DocumentLoadingArgs](../../documentloadingargs/)
* Interface [IDocumentLoadingCallback](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
