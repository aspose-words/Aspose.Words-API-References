---
title: "طريقة Aspose::Words::Comment::get_Id"
linktitle: "get_Id"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Comment::get_Id. يحصل على معرف التعليق أو يضبطه في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/comment/get_id/
---
## Comment::get_Id method


يحصل أو يعيّن معرف التعليق.

```cpp
int32_t Aspose::Words::Comment::get_Id() const
```

## ملاحظات


معرف التعليق يسمح بربط التعليق بمنطقة نص في المستند. يجب تحديد المنطقة باستخدام كائن [CommentRangeStart](../../commentrangestart/) و[CommentRangeEnd](../../commentrangeend/) الذين يشتركان في نفس قيمة المعرف مثل كائن [Comment](../).

ستستخدم هذه القيمة عند البحث عن عقد [CommentRangeStart](../../commentrangestart/) و[CommentRangeEnd](../../commentrangeend/) المرتبطة بهذا التعليق.

[Comment](../) identifiers are supposed to be unique across a document and Aspose.Words automatically maintains comment identifiers when loading, saving and combining documents. 
## انظر أيضًا

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
