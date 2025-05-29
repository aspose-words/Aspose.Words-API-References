---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words لـ .NET
description: قم بتحسين حفظ المستندات باستخدام خاصية TempFolder في SaveOptions، والتي تقوم بتعيين مجلد للملفات المؤقتة DOC وDOCX، مما يعزز الكفاءة.
type: docs
weight: 140
url: /ar/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية`باطل` ولا يتم استخدام أي ملفات مؤقتة.

```csharp
public string TempFolder { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| OutOfMemoryException | يمكن أن يكون ارتفاع الذاكرة أثناء الحفظ كبيرًا بما يكفي للتسبب في الاستثناء. |

## ملاحظات

عند حفظ مستند Aspose.Words، يحتاج إلى إنشاء هياكل داخلية مؤقتة. افتراضيًا، تُنشأ هذه الهياكل الداخلية في الذاكرة، ويرتفع استهلاك الذاكرة لفترة قصيرة أثناء حفظ المستند. عند اكتمال الحفظ، تُحرر الذاكرة وتُستعاد بواسطة جامع البيانات المهملة.

تحديد مجلد مؤقت باستخدام`TempFolder` سيؤدي ذلك إلى احتفاظ Aspose.Words بالهياكل الداخلية في ملفات مؤقتة x000d_ بدلاً من الذاكرة. هذا يقلل من استخدام الذاكرة أثناء الحفظ، ولكنه سيؤثر سلبًا على أدائه.

يجب أن يكون المجلد موجودًا وقابلًا للكتابة، وإلا فسيتم طرح استثناء.

يقوم Aspose.Words تلقائيًا بحذف جميع الملفات المؤقتة عند اكتمال الحفظ.

## أمثلة

يوضح كيفية استخدام القرص الصلب بدلاً من الذاكرة عند حفظ مستند.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// عندما نحفظ مستندًا، يتم تخزين عناصر مختلفة مؤقتًا في الذاكرة أثناء إجراء عملية الحفظ.
// يمكننا استخدام هذا الخيار لاستخدام مجلد مؤقت في نظام الملفات المحلي بدلاً من ذلك،
// مما سيقلل من تكلفة الذاكرة لتطبيقنا.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// يجب أن يكون المجلد المؤقت المحدد موجودًا في نظام الملفات المحلي قبل عملية الحفظ.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// سوف يظل المجلد بدون أي محتويات متبقية من عملية التحميل.
Assert.AreEqual(0, Directory.GetFiles(options.TempFolder).Length);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
