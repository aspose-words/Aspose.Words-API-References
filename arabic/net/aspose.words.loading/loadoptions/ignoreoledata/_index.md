---
title: LoadOptions.IgnoreOleData
second_title: Aspose.Words لمراجع .NET API
description: LoadOptions ملكية. يحدد ما إذا كان سيتم تجاهل بيانات OLE أم لا.
type: docs
weight: 70
url: /ar/net/aspose.words.loading/loadoptions/ignoreoledata/
---
## LoadOptions.IgnoreOleData property

يحدد ما إذا كان سيتم تجاهل بيانات OLE أم لا.

```csharp
public bool IgnoreOleData { get; set; }
```

### ملاحظات

قد يؤدي تجاهل بيانات OLE إلى تقليل استهلاك الذاكرة وزيادة الأداء دون فقدان البيانات في حالة عدم دعم تنسيق الوجهة لكائنات OLE.

القيمة الافتراضية هي`خطأ شنيع`.

### أمثلة

يوضح كيفية إدخال بيانات OLE أثناء التحميل.

```csharp
// قد يؤدي تجاهل بيانات OLE إلى تقليل استهلاك الذاكرة وزيادة الأداء
// بدون فقدان البيانات في حالة عدم دعم تنسيق الوجهة لكائنات OLE.
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Document doc = new Document(MyDir + "OLE objects.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.IgnoreOleData.docx");
```

### أنظر أيضا

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../loadoptions/)
* المجسم [Aspose.Words](../../../)


