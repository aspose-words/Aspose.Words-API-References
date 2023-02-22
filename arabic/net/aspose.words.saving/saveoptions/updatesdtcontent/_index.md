---
title: SaveOptions.UpdateSdtContent
second_title: Aspose.Words لمراجع .NET API
description: SaveOptions ملكية. الحصول على قيمة أو تعيينها لتحديد ما إذا كان محتوىStructuredDocumentTag يتم تحديثه قبل الحفظ.
type: docs
weight: 200
url: /ar/net/aspose.words.saving/saveoptions/updatesdtcontent/
---
## SaveOptions.UpdateSdtContent property

الحصول على قيمة أو تعيينها لتحديد ما إذا كان محتوى[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) يتم تحديثه قبل الحفظ.

```csharp
public bool UpdateSdtContent { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`حقيقي` .

### أمثلة

يوضح كيفية تحديث علامات المستند المهيكلة أثناء حفظ مستند في PDF.

```csharp
Document doc = new Document();

// إدراج علامة مستند منظم للقائمة المنسدلة.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
tag.ListItems.Add(new SdtListItem("Value 1"));
tag.ListItems.Add(new SdtListItem("Value 2"));
tag.ListItems.Add(new SdtListItem("Value 3"));

// تعرض القائمة المنسدلة حاليًا "اختر عنصرًا" كنص افتراضي.
// قم بتعيين خاصية "SelectedValue" إلى أحد عناصر القائمة للحصول على العلامة
// عرض قيمة عنصر القائمة بدلاً من النص الافتراضي.
tag.ListItems.SelectedValue = tag.ListItems[1];

doc.FirstSection.Body.AppendChild(tag);

// قم بإنشاء كائن "PdfSaveOptions" لتمريره إلى أسلوب "حفظ" المستند
// لتعديل كيفية حفظ هذه الطريقة المستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "UpdateSdtContent" على "false" وليس لتحديث علامات المستند المهيكلة
// أثناء حفظ المستند في PDF. سيعرضون قيمهم الافتراضية كما كانت في وقت الإنشاء.
// اضبط خاصية "UpdateSdtContent" على "true" للتأكد من أن العلامات تعرض القيم المحدثة في PDF.
options.UpdateSdtContent = updateSdtContent;

doc.Save(ArtifactsDir + "StructuredDocumentTag.UpdateSdtContent.pdf", options);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../saveoptions/)
* المجسم [Aspose.Words](../../../)


