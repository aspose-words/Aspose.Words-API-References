---
title: List.HasSameTemplate
linktitle: HasSameTemplate
articleTitle: HasSameTemplate
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة HasSameTemplate، وتحقق بسهولة مما إذا كانت القائمتان تشتركان في نفس القالب، مما يضمن الاتساق والكفاءة في إدارة البيانات الخاصة بك.
type: docs
weight: 120
url: /ar/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

يعود صحيحًا إذا تم إنشاء القائمة الحالية والقائمة المحددة من نفس القالب.

```csharp
public bool HasSameTemplate(List other)
```

## أمثلة

يوضح كيفية تعريف القوائم بنفس ListDefId.

```csharp
Document doc = new Document(MyDir + "Different lists.docx");

Assert.True(doc.Lists[0].HasSameTemplate(doc.Lists[1]));
Assert.False(doc.Lists[1].HasSameTemplate(doc.Lists[2]));
```

### أنظر أيضا

* class [List](../)
* مساحة الاسم [Aspose.Words.Lists](../../../aspose.words.lists/)
* المجسم [Aspose.Words](../../../)
