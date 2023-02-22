---
title: SaveOptions.TempFolder
second_title: Aspose.Words لمراجع .NET API
description: SaveOptions ملكية. يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي  هذه الخاصية هيلا شيء ولا يتم استخدام أي ملفات مؤقتة.
type: docs
weight: 150
url: /ar/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي ، هذه الخاصية هي`لا شيء` ولا يتم استخدام أي ملفات مؤقتة.

```csharp
public string TempFolder { get; set; }
```

### ملاحظات

عندما يحفظ Aspose.Words مستندًا ، فإنه يحتاج إلى إنشاء هياكل داخلية مؤقتة. بشكل افتراضي ، يتم إنشاء هذه الهياكل الداخلية في الذاكرة ويزيد استخدام الذاكرة لفترة قصيرة أثناء حفظ المستند . عند اكتمال الحفظ ، يتم تحرير الذاكرة واستعادتها بواسطة أداة تجميع البيانات المهملة.

إذا كنت تحفظ مستندًا كبيرًا جدًا (بآلاف الصفحات) و / أو تقوم بمعالجة العديد من المستندات في نفس الوقت ، فإن الارتفاع المفاجئ في الذاكرة أثناء الحفظ يمكن أن يكون كبيرًا بما يكفي لإلقاء النظامOutOfMemoryException . تحديد مجلد مؤقت باستخدام`TempFolder` سيؤدي إلى احتفاظ Aspose.Words بالبنى الداخلية في ملفات مؤقتة بدلاً من الذاكرة. يقلل من استخدام الذاكرة أثناء الحفظ ، لكنه يقلل من أداء الحفظ.

يجب أن يكون المجلد موجودًا وأن يكون قابلاً للكتابة ، وإلا فسيتم طرح استثناء.

يحذف Aspose.Words جميع الملفات المؤقتة تلقائيًا عند اكتمال الحفظ.

### أمثلة

يوضح كيفية استخدام القرص الصلب بدلاً من الذاكرة عند حفظ مستند.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// عندما نحفظ مستندًا ، يتم تخزين عناصر مختلفة مؤقتًا في الذاكرة أثناء إجراء عملية الحفظ.
// يمكننا استخدام هذا الخيار لاستخدام مجلد مؤقت في نظام الملفات المحلي بدلاً من ذلك ،
// مما سيقلل من حمل ذاكرة تطبيقنا.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// يجب أن يكون المجلد المؤقت المحدد موجودًا في نظام الملفات المحلي قبل عملية الحفظ.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// سيستمر المجلد مع عدم وجود محتويات متبقية من عملية التحميل.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../saveoptions/)
* المجسم [Aspose.Words](../../../)


