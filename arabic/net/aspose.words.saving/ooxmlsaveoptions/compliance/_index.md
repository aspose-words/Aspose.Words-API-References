---
title: OoxmlSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words لـ .NET
description: اكتشف توافق OoxmlSaveOptions لاختيار إصدار OOXML المناسب لمستندات الإخراج. حسّن ملفاتك باستخدام إعداد Ecma376_2006 الافتراضي.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/ooxmlsaveoptions/compliance/
---
## OoxmlSaveOptions.Compliance property

يحدد إصدار OOXML للمستند الناتج. القيمة الافتراضية هيEcma376_2006 .

```csharp
public OoxmlCompliance Compliance { get; set; }
```

## أمثلة

يوضح كيفية إدراج أشكال DML في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي نوعان من التغليف الذي قد تمتلكه الأشكال.
// 1 - عائم:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - مضمن:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// إذا كنت بحاجة إلى إنشاء أشكال "غير بدائية"، مثل SingleCornerSnipped وTopCornersSnipped وDiagonalCornersSnipped،
// TopCornersOneRoundedOneSnipped، SingleCornerRounded، TopCornersRounded، أو DiagonalCornersRounded،
// ثم احفظ المستند بالتوافق "الصارم" أو "الانتقالي"، والذي يسمح بحفظ الشكل كـ DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

يوضح كيفية تكوين قائمة لإعادة تشغيل الترقيم في كل قسم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// سيتم تطبيق خاصية "IsRestartAtEachSection" فقط عندما
// مستوى توافق OOXML الخاص بالمستند هو معيار أحدث من "OoxmlComplianceCore.Ecma376".
OoxmlSaveOptions options = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

builder.ListFormat.List = list;

builder.Writeln("List item 1");
builder.Writeln("List item 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("List item 3");
builder.Writeln("List item 4");

doc.Save(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

Assert.AreEqual(restartListAtEachSection, doc.Lists[0].IsRestartAtEachSection);
```

يوضح كيفية تعيين مواصفات توافق OOXML للمستند المحفوظ للالتزام بها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا قمنا بتكوين خيارات التوافق لتتوافق مع Microsoft Word 2003،
// إدراج صورة سيؤدي إلى تحديد شكلها باستخدام VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// لا يدعم معيار OOXML "ISO/IEC 29500:2008" أشكال VML.
// إذا قمنا بتعيين خاصية "التوافق" لكائن SaveOptions إلى "OoxmlCompliance.Iso29500_2008_Strict"،
 // أي مستند نقوم بحفظه أثناء تمرير هذا الكائن يجب أن يتبع هذا المعيار.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// تحدد مستندنا المحفوظ الشكل باستخدام DML للالتزام بمعيار OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### أنظر أيضا

* enum [OoxmlCompliance](../../ooxmlcompliance/)
* class [OoxmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
