---
title: Document.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مستنداتك بسهولة باستخدام طريقة RemoveBlankPages، والتخلص من الصفحات الفارغة غير المرغوب فيها للحصول على مظهر مصقول واحترافي.
type: docs
weight: 700
url: /ar/net/aspose.words/document/removeblankpages/
---
## Document.RemoveBlankPages method

يزيل الصفحات الفارغة من المستند.

```csharp
public List<int> RemoveBlankPages()
```

### قيمة الإرجاع

لقد تم اعتبار قائمة أرقام الصفحات فارغة وتم إزالتها.

## ملاحظات

لن تحتوي الوثيقة الناتجة على صفحات تعتبر فارغة بينما يجب أن يظل المحتوى الآخر، بما في ذلك الترقيم والرؤوس/التذييلات والتخطيط العام دون تغيير. تُعتبر الصفحة فارغة عندما لا يحتوي نص الصفحة على أي محتوى مرئي، على سبيل المثال، سيتم اعتبار الجدول الفارغ الذي لا يحتوي على حدود غير مرئي وبالتالي سيتم اكتشاف الصفحة على أنها فارغة.

## أمثلة

يوضح كيفية إزالة الصفحات الفارغة من المستند.

```csharp
Document doc = new Document(MyDir + "Blank pages.docx");
Assert.AreEqual(2, doc.PageCount);
doc.RemoveBlankPages();
doc.UpdatePageLayout();
Assert.AreEqual(1, doc.PageCount);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
