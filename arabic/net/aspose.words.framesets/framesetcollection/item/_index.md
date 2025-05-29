---
title: FramesetCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: الوصول إلى إطارات محددة باستخدام FramesetCollection. استرجاع صفحات الإطارات بسهولة حسب الفهرس لتصفح ويب فعال وتجربة مستخدم مُحسّنة.
type: docs
weight: 30
url: /ar/net/aspose.words.framesets/framesetcollection/item/
---
## FramesetCollection indexer

يحصل على إطار أو إطارات الصفحة عند الفهرس المحدد.

```csharp
public Frameset this[int index] { get; }
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

* class [Frameset](../../frameset/)
* class [FramesetCollection](../)
* مساحة الاسم [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* المجسم [Aspose.Words](../../../)
