---
title: BuiltInDocumentProperties.CreatedTime
linktitle: CreatedTime
articleTitle: CreatedTime
second_title: Aspose.Words لـ .NET
description: BuiltInDocumentProperties CreatedTime ملكية. الحصول على أو تحديد تاريخ إنشاء المستند بالتوقيت العالمي المنسق UTC في C#.
type: docs
weight: 100
url: /ar/net/aspose.words.properties/builtindocumentproperties/createdtime/
---
## BuiltInDocumentProperties.CreatedTime property

الحصول على أو تحديد تاريخ إنشاء المستند بالتوقيت العالمي المنسق (UTC).

```csharp
public DateTime CreatedTime { get; set; }
```

## ملاحظات

بالنسبة للمستندات التي تم إنشاؤها من تنسيق RTF، تقوم هذه الخاصية بإرجاع التوقيت المحلي لجهاز المؤلف في لحظة إنشاء المستند.

لا يقوم Aspose.Words بتحديث هذه الخاصية.

## أمثلة

يوضح كيفية العمل مع خصائص المستند في فئة "الأصل".

```csharp
// افتح مستندًا قمنا بإنشائه وتحريره باستخدام Microsoft Word.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// تحتوي الخصائص المضمنة التالية على معلومات تتعلق بإنشاء هذا المستند وتحريره.
// يمكننا النقر بزر الماوس الأيمن فوق هذا المستند في مستكشف Windows والعثور عليه
// هذه الخصائص عبر "الخصائص" -> "التفاصيل" -> فئة "الأصل".
// يمكن لحقول مثل PRINTDATE وEDITTIME عرض هذه القيم في نص المستند.
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// يمكننا أيضًا تغيير قيم الخصائص المضمنة.
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// يقوم Microsoft Word بتحديث الخصائص التالية تلقائيًا عندما نحفظ المستند.
// لاستخدام هذه الخصائص مع Aspose.Words، سنحتاج إلى تعيين قيم لها يدويًا.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// يمكننا النقر بزر الماوس الأيمن فوق هذا المستند في مستكشف Windows والعثور عليه these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### أنظر أيضا

* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
