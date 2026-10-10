---
title: "Aspose::Words::Comment::get_Id 方法"
linktitle: "get_Id"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Comment::get_Id 方法。获取或设置 C++ 中的评论标识符。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words/comment/get_id/
---
## Comment::get_Id method


获取或设置评论标识符。

```cpp
int32_t Aspose::Words::Comment::get_Id() const
```

## 备注


评论标识符允许将评论锚定到文档中的文本区域。该区域必须使用 [CommentRangeStart](../../commentrangestart/) 和 [CommentRangeEnd](../../commentrangeend/) 对象进行标记，并且这些对象的标识符值需与 [Comment](../) 对象相同。

在查找与此评论关联的 [CommentRangeStart](../../commentrangestart/) 和 [CommentRangeEnd](../../commentrangeend/) 节点时，需要使用该值。

[Comment](../) identifiers are supposed to be unique across a document and Aspose.Words automatically maintains comment identifiers when loading, saving and combining documents. 
## 另见

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
