---
title: OleFormat.SuggestedFileName
linktitle: SuggestedFileName
articleTitle: SuggestedFileName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية OleFormat SuchenFileName لاسترداد اسم الملف الموصى به بسهولة لحفظ الكائنات المضمنة بسلاسة.
type: docs
weight: 130
url: /ar/net/aspose.words.drawing/oleformat/suggestedfilename/
---
## OleFormat.SuggestedFileName property

يحصل على اسم الملف المقترح للكائن المضمن الحالي إذا كنت تريد حفظه في ملف.

```csharp
public string SuggestedFileName { get; }
```

## أمثلة

يوضح كيفية الحصول على اسم الملف المقترح لكائن OLE.

```csharp
Document doc = new Document(MyDir + "OLE shape.rtf");

Shape oleShape = (Shape)doc.FirstSection.Body.GetChild(NodeType.Shape, 0, true);

// يمكن لكائنات OLE توفير اسم ملف وملحق مقترحين،
// والذي يمكننا استخدامه عند حفظ محتويات الكائن في ملف في نظام الملفات المحلي.
string suggestedFileName = oleShape.OleFormat.SuggestedFileName;

Assert.AreEqual("CSV.csv", suggestedFileName);

using (FileStream fileStream = new FileStream(ArtifactsDir + suggestedFileName, FileMode.Create))
{
    oleShape.OleFormat.Save(fileStream);
}
```

### أنظر أيضا

* class [OleFormat](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
