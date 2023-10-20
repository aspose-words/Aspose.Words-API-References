---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words لـ .NET
description: SaveOptions TempFolder ملكية. يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي تكون هذه الخاصيةباطل ولا يتم استخدام أي ملفات مؤقتة في C#.
type: docs
weight: 140
url: /ar/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية`باطل` ولا يتم استخدام أي ملفات مؤقتة.

```csharp
public string TempFolder { get; set; }
```

## ملاحظات

عندما يقوم Aspose.Words بحفظ مستند، فإنه يحتاج إلى إنشاء هياكل داخلية مؤقتة. افتراضيًا، يتم إنشاء هذه الهياكل الداخلية في الذاكرة ويرتفع استخدام الذاكرة لفترة قصيرة أثناء يتم حفظ المستند. عند اكتمال الحفظ، يتم تحرير الذاكرة واستعادتها بواسطة أداة تجميع البيانات المهملة.

إذا كنت تقوم بحفظ مستند كبير جدًا (آلاف الصفحات) و/أو تقوم بمعالجة العديد من المستندات في نفس الوقت، ، فقد يكون ارتفاع الذاكرة أثناء الحفظ كبيرًا بما يكفي لتسبب رمي النظامOutOfMemoryException . تحديد مجلد مؤقت باستخدام`TempFolder` سيؤدي إلى قيام Aspose.Words بالاحتفاظ بالهياكل الداخلية في ملفات مؤقتة بدلاً من الذاكرة. فهو يقلل من استخدام الذاكرة أثناء الحفظ، ولكنه سيقلل من أداء الحفظ.

يجب أن يكون المجلد موجودًا وقابلاً للكتابة، وإلا فسيتم طرح استثناء.

يقوم Aspose.Words تلقائيًا بحذف جميع الملفات المؤقتة عند اكتمال الحفظ.

## أمثلة

يوضح كيفية استخدام القرص الصلب بدلاً من الذاكرة عند حفظ مستند.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// عندما نقوم بحفظ مستند، يتم تخزين عناصر مختلفة مؤقتًا في الذاكرة أثناء إجراء عملية الحفظ.
// يمكننا استخدام هذا الخيار لاستخدام مجلد مؤقت في نظام الملفات المحلي بدلاً من ذلك،
// مما سيقلل من الحمل الزائد لذاكرة تطبيقنا.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// يجب أن يكون المجلد المؤقت المحدد موجودًا في نظام الملفات المحلي قبل عملية الحفظ.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// سيستمر المجلد بدون أي محتويات متبقية من عملية التحميل.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
