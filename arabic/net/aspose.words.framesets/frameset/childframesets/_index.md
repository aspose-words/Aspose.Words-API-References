---
title: Frameset.ChildFramesets
linktitle: ChildFramesets
articleTitle: ChildFramesets
second_title: Aspose.Words لـ .NET
description: Frameset ChildFramesets ملكية. الحصول على مجموعة الإطارات الفرعية وصفحات الإطارات في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.framesets/frameset/childframesets/
---
## Frameset.ChildFramesets property

الحصول على مجموعة الإطارات الفرعية وصفحات الإطارات.

```csharp
public FramesetCollection ChildFramesets { get; }
```

## أمثلة

يوضح كيفية الوصول إلى الإطارات الموجودة على الصفحة.

```csharp
// تحتوي الوثيقة على عدة إطارات مع روابط لمستندات أخرى.
Document doc = new Document(MyDir + "Frameset.docx");

// يمكننا التحقق من عنوان URL الافتراضي (عنوان URL لصفحة ويب أو مستند محلي) أو ما إذا كان الإطار مصدرًا خارجيًا.
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx"،
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// تغيير خصائص أحد الإطارات لدينا.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### أنظر أيضا

* class [FramesetCollection](../../framesetcollection/)
* class [Frameset](../)
* مساحة الاسم [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* المجسم [Aspose.Words](../../../)
