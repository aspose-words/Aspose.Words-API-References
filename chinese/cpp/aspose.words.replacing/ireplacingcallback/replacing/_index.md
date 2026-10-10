---
title: "Aspose::Words::Replacing::IReplacingCallback::Replacing 方法"
linktitle: "替换"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::IReplacingCallback::Replacing 方法。用户自定义的方法，在 C++ 中的替换操作期间，对每个找到的匹配在实际替换之前被调用。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.replacing/ireplacingcallback/replacing/
---
## IReplacingCallback::Replacing method


在替换操作期间，对每个找到的匹配，在实际替换之前调用的用户自定义方法。

```cpp
virtual Aspose::Words::Replacing::ReplaceAction Aspose::Words::Replacing::IReplacingCallback::Replacing(System::SharedPtr<Aspose::Words::Replacing::ReplacingArgs> args)=0
```


### ReturnValue

一个指定对当前匹配应采取的操作的 [ReplaceAction](../../replaceaction/) 值。

## 另见

* Enum [ReplaceAction](../../replaceaction/)
* Class [ReplacingArgs](../../replacingargs/)
* Interface [IReplacingCallback](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
