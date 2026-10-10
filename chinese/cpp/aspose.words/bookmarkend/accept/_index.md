---
title: "Aspose::Words::BookmarkEnd::Accept 方法"
linktitle: "Accept"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BookmarkEnd::Accept 方法。 在 C++ 中接受访问者。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/bookmarkend/accept/
---
## BookmarkEnd::Accept method


接受访问者。

```cpp
bool Aspose::Words::BookmarkEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 访问者 | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | 将访问该节点的访问者。 |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## 备注


调用 [VisitBookmarkEnd()](../../documentvisitor/visitbookmarkend/)。

更多信息请参阅 Visitor 设计模式。

## 另见

* Class [DocumentVisitor](../../documentvisitor/)
* Class [BookmarkEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
