---
title: Frameset.IsFrameLinkToFile
linktitle: IsFrameLinkToFile
articleTitle: IsFrameLinkToFile
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية Frameset IsFrameLinkToFile تصميم موقعك الإلكتروني من خلال ربط الموارد الخارجية بسلاسة. حسّن إطاراتك لأداء أفضل!
type: docs
weight: 40
url: /ar/net/aspose.words.framesets/frameset/isframelinktofile/
---
## Frameset.IsFrameLinkToFile property

يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان اسم ملف صفحة الويب أو المستند المحدد في [`FrameDefaultUrl`](../framedefaulturl/) الخاصية هي مورد خارجي يرتبط به الإطار.

```csharp
public bool IsFrameLinkToFile { get; set; }
```

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

* class [Frameset](../)
* مساحة الاسم [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* المجسم [Aspose.Words](../../../)
