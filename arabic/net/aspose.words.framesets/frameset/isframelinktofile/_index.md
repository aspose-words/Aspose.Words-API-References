---
title: Frameset.IsFrameLinkToFile
second_title: Aspose.Words لمراجع .NET API
description: Frameset ملكية. الحصول على أو تعيين قيمة تشير إلى ما إذا كانت صفحة الويب أو اسم ملف المستند محددًا في FrameDefaultUrl الخاصية هي مورد خارجي يرتبط به الإطار.
type: docs
weight: 40
url: /ar/net/aspose.words.framesets/frameset/isframelinktofile/
---
## Frameset.IsFrameLinkToFile property

الحصول على أو تعيين قيمة تشير إلى ما إذا كانت صفحة الويب أو اسم ملف المستند محددًا في [`FrameDefaultUrl`](../framedefaulturl/) الخاصية هي مورد خارجي يرتبط به الإطار.

```csharp
public bool IsFrameLinkToFile { get; set; }
```

### أمثلة

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

* class [Frameset](../)
* مساحة الاسم [Aspose.Words.Framesets](../../frameset/)
* المجسم [Aspose.Words](../../../)


