---
title: LoadOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words لـ .NET
description: حسّن قراءة المستندات باستخدام خاصية TempFolder في LoadOptions. أدر الملفات المؤقتة بسهولة لتحسين المعالجة والأداء.
type: docs
weight: 150
url: /ar/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

يسمح باستخدام الملفات المؤقتة عند قراءة المستند. بشكل افتراضي، هذه الخاصية هي`باطل` ولا يتم استخدام أي ملفات مؤقتة.

```csharp
public string TempFolder { get; set; }
```

## ملاحظات

يجب أن يكون المجلد موجودًا وقابلًا للكتابة، وإلا فسيتم طرح استثناء.

يقوم Aspose.Words تلقائيًا بحذف جميع الملفات المؤقتة عند اكتمال القراءة.

## أمثلة

يوضح كيفية تحميل مستند باستخدام الملفات المؤقتة.

```csharp
// لاحظ أن مثل هذا النهج يمكن أن يقلل من استخدام الذاكرة ولكنه يقلل من السرعة
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// تأكد من وجود الدليل وقم بتحميله
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

يوضح كيفية استخدام القرص الصلب بدلاً من الذاكرة عند تحميل مستند.

```csharp
// عندما نقوم بتحميل مستند، يتم تخزين عناصر مختلفة مؤقتًا في الذاكرة أثناء حدوث عملية الحفظ.
// يمكننا استخدام هذا الخيار لاستخدام مجلد مؤقت في نظام الملفات المحلي بدلاً من ذلك،
// مما سيقلل من تكلفة الذاكرة لتطبيقنا.
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// يجب أن يكون المجلد المؤقت المحدد موجودًا في نظام الملفات المحلي قبل عملية التحميل.
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// سوف يظل المجلد بدون أي محتويات متبقية من عملية التحميل.
Assert.AreEqual(0, Directory.GetFiles(options.TempFolder).Length);
```

### أنظر أيضا

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
