---
title: Frameset.FrameDefaultUrl
second_title: Aspose.Words لمراجع .NET API
description: Frameset ملكية. الحصول على أو تحديد عنوان URL لصفحة الويب أو اسم ملف المستند ليتم عرضه في هذا الإطار.
type: docs
weight: 30
url: /ar/net/aspose.words.framesets/frameset/framedefaulturl/
---
## Frameset.FrameDefaultUrl property

الحصول على أو تحديد عنوان URL لصفحة الويب أو اسم ملف المستند ليتم عرضه في هذا الإطار.

```csharp
public string FrameDefaultUrl { get; set; }
```

### أمثلة

يوضح كيفية الوصول إلى الإطارات على الصفحة.

```csharp
// يحتوي المستند على عدة إطارات مع روابط لمستندات أخرى.
Document doc = new Document(MyDir + "Frameset.docx");

// يمكننا التحقق من عنوان URL الافتراضي (عنوان URL لصفحة ويب أو مستند محلي) أو إذا كان الإطار مصدرًا خارجيًا.
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx "،
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// تغيير خصائص أحد إطاراتنا.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute٪20position٪20tab.docx ";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### أنظر أيضا

* class [Frameset](../)
* مساحة الاسم [Aspose.Words.Framesets](../../frameset/)
* المجسم [Aspose.Words](../../../)


