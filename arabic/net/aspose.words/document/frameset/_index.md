---
title: Document.Frameset
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Frameset للمستندات. احصل على نسخة Frameset لدمج الصفحات المؤطرة بسلاسة. حسّن تجربة تصفحك اليوم!
type: docs
weight: 170
url: /ar/net/aspose.words/document/frameset/
---
## Document.Frameset property

يعيد`Frameset` مثال إذا كانت هذه الوثيقة تمثل صفحة إطارات.

```csharp
public Frameset Frameset { get; }
```

## ملاحظات

إذا لم يتم تأطير المستند، فإن الخاصية تحتوي على`باطل` القيمة.

## أمثلة

يوضح كيفية الوصول إلى الإطارات الموجودة على الصفحة.

```csharp
//تحتوي الوثيقة على عدة إطارات تحتوي على روابط لوثائق أخرى.
Document doc = new Document(MyDir + "Frameset.docx");

Assert.AreEqual(3, doc.Frameset.ChildFramesets.Count);
// يمكننا التحقق من عنوان URL الافتراضي (عنوان URL لصفحة ويب أو مستند محلي) أو ما إذا كان الإطار عبارة عن مورد خارجي.
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx"،
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// تغيير خصائص أحد إطاراتنا.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### أنظر أيضا

* class [Frameset](../../../aspose.words.framesets/frameset/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
