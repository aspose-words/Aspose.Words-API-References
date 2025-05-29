---
title: BuiltInDocumentProperties.Manager
linktitle: Manager
articleTitle: Manager
second_title: Aspose.Words لـ .NET
description: أدر خصائص المستندات المضمنة بسهولة باستخدام أداتنا سهلة الاستخدام. احصل على الخصائص أو عيّنها بسهولة لتحسين تجربة التعامل مع مستنداتك.
type: docs
weight: 210
url: /ar/net/aspose.words.properties/builtindocumentproperties/manager/
---
## BuiltInDocumentProperties.Manager property

يحصل على خاصية المدير أو يعينها.

```csharp
public string Manager { get; set; }
```

## أمثلة

يوضح كيفية العمل مع خصائص المستند في فئة "الأصل".

```csharp
// افتح المستند الذي قمنا بإنشائه وتحريره باستخدام Microsoft Word.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// تحتوي الخصائص المضمنة التالية على معلومات تتعلق بإنشاء هذا المستند وتحريره.
// يمكننا النقر بزر الماوس الأيمن على هذا المستند في مستكشف Windows والعثور عليه
// هذه الخصائص عبر "الخصائص" -> "التفاصيل" -> فئة "الأصل".
// يمكن للحقول مثل PRINTDATE وEDITTIME عرض هذه القيم في نص المستند.
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

//يمكننا أيضًا تغيير قيم الخصائص المضمنة.
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// يقوم Microsoft Word بتحديث الخصائص التالية تلقائيًا عند حفظ المستند.
// لاستخدام هذه الخصائص مع Aspose.Words، سنحتاج إلى تعيين القيم لها يدويًا.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// يمكننا النقر بزر الماوس الأيمن على هذا المستند في مستكشف Windows والعثور عليه these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### أنظر أيضا

* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
