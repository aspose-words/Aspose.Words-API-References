---
title: List.HasSameTemplate
second_title: Aspose.Words لمراجع .NET API
description: List طريقة. إرجاع صحيح إذا تم إنشاء القائمة الحالية والقائمة المحددة من نفس القالب.
type: docs
weight: 120
url: /ar/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

إرجاع صحيح إذا تم إنشاء القائمة الحالية والقائمة المحددة من نفس القالب.

```csharp
public bool HasSameTemplate(List other)
```

### أمثلة

يوضح كيفية تحديد القوائم بنفس ListDefId.

```csharp
Document doc = new Document(MyDir + "Different lists.docx");

Assert.True(doc.Lists[0].HasSameTemplate(doc.Lists[1]));
Assert.False(doc.Lists[1].HasSameTemplate(doc.Lists[2]));
```

### أنظر أيضا

* class [List](../)
* مساحة الاسم [Aspose.Words.Lists](../../list/)
* المجسم [Aspose.Words](../../../)


