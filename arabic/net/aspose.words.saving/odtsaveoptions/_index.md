---
title: OdtSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفOdt أو x000d_Ott التنسيق ._ x000d_
type: docs
weight: 5050
url: /ar/net/aspose.words.saving/odtsaveoptions/
---
## OdtSaveOptions class

يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفOdt أو x000d_Ott التنسيق ._ x000d_

```csharp
public class OdtSaveOptions : SaveOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [OdtSaveOptions](odtsaveoptions#constructor)() | يقوم بتهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ مستند بتنسيقOdt التنسيق ._ x000d_ |
| [OdtSaveOptions](odtsaveoptions#constructor_1)(SaveFormat) | يقوم بتهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ مستند بتنسيقOdt أو x000d_Ott التنسيق ._ x000d_ |
| [OdtSaveOptions](odtsaveoptions#constructor_2)(string) | يقوم بتهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ مستند بتنسيقOdt format مشفر بكلمة مرور. x000d_ |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إلى ما إذا كان سيتم السماح بدمج الخطوط مع مخططات PostScript عند حفظ خطوط TrueType في مستند ما . القيمة الافتراضية هي **خاطئة** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | الحصول على أو تعيين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ / الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | الحصول على أو تعيين المسار للقالب الافتراضي (بما في ذلك اسم الملف) ._ x000d_ القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة** (Empty ) ._ x000d_ |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض التأثيرات ثلاثية الأبعاد ._ x000d_ |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض تأثيرات DrawingML . |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض أشكال DrawingML . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | عندما يكون صحيحًا ، يتسبب في تضمين اسم ونسخة Aspose. Words في الملفات المنتجة. القيمة الافتراضية هي **حقيقي** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | الحصول على القيمة أو تعيينها لتحديد تنسيقات المستندات التي يُسمح لها بالتعيين[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . بشكل افتراضي فقطFlatOpc يُسمح بتعيين تنسيق المستند. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض كائنات الحبر (InkML). |
| [IsStrictSchema11](../../aspose.words.saving/odtsaveoptions/isstrictschema11) { get; set; } | يحدد ما إذا كان يجب أن يتوافق التصدير مع مواصفات ODT 1.1 بشكل صارم. OOo 3.0 يعرض الملفات بشكل صحيح عندما تحتوي على عناصر وسمات ODT 1.2. استخدم "false" لهذا الغرض ، أو "true" للتوافق الصارم مع المواصفات 1.1. القيمة الافتراضية هي **خاطئة** . |
| [MeasureUnit](../../aspose.words.saving/odtsaveoptions/measureunit) { get; set; } | يسمح بتحديد وحدات قياس لتطبيقها على محتوى المستند. القيمة الافتراضية هيCentimeters |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **خاطئة** . |
| [Password](../../aspose.words.saving/odtsaveoptions/password) { get; set; } | الحصول على أو تعيين كلمة مرور لتشفير المستند. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | متى`حقيقي` ، جميلة تنسيقات الإخراج حيثما أمكن ذلك. القيمة الافتراضية هي **خاطئة** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | يتم الاتصال به أثناء حفظ المستند ويقبل البيانات حول حفظ التقدم ._ x000d_ |
| override [SaveFormat](../../aspose.words.saving/odtsaveoptions/saveformat) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا ._ x000d_ يمكن أن يكونOdt أوOtt . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي ، هذه الخاصية هي`لا شيء` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية خاطئة ؛ |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تحديث حقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت ._ x000d_ القيمة الافتراضية لهذه الخاصية هي **حقيقي** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان محتوى[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) يتم تحديثه قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام الصقل للعرض أم لا. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |

### ملاحظات

في الوقت الحالي يوفر فقط ملف[`SaveFormat`](./saveformat) الخاصية ، ولكن في المستقبل ستتم إضافة خيارات أخرى ، مثل كلمة مرور التشفير أو إعدادات التوقيع الرقمي.

### أمثلة

يوضح كيفية جعل مستند محفوظ يتوافق مع مخطط ODT أقدم.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

يوضح كيفية استخدام وحدات قياس مختلفة لتحديد معلمات النمط لمستند ODT محفوظ.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// عندما نقوم بتصدير المستند إلى .odt ، يمكننا استخدام كائن OdtSaveOptions لتعديل كيفية حفظ المستند.
// يمكننا تعيين خاصية "MeasureUnit" على "OdtSaveMeasureUnit.Centimeters"
// لتعريف محتوى مثل معلمات النمط باستخدام النظام المتري الذي يستخدمه Open Office. 
// يمكننا تعيين خاصية "MeasureUnit" على "OdtSaveMeasureUnit.Inches"
// لتعريف محتوى مثل معلمات النمط باستخدام النظام الإمبراطوري الذي يستخدمه Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### أنظر أيضا

* class [SaveOptions](../saveoptions)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
