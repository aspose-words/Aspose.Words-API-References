---
title: OoxmlCompliance Enum
linktitle: OoxmlCompliance
articleTitle: OoxmlCompliance
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.OoxmlCompliance تعداد. يسمح بتحديد مواصفات OOXML التي سيتم استخدامها عند الحفظ بتنسيق DOCX في C#.
type: docs
weight: 5340
url: /ar/net/aspose.words.saving/ooxmlcompliance/
---
## OoxmlCompliance enumeration

يسمح بتحديد مواصفات OOXML التي سيتم استخدامها عند الحفظ بتنسيق DOCX.

```csharp
public enum OoxmlCompliance
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Ecma376_2006 | `0` | الإصدار الأول من ECMA-376، 2006. |
| Iso29500_2008_Transitional | `1` | ISO/IEC 29500:2008 مستوى الامتثال الانتقالي. |
| Iso29500_2008_Strict | `2` | ISO/IEC 29500:2008 مستوى الامتثال الصارم. |

## أمثلة

يوضح كيفية إدراج أشكال DML في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي نوعان من الالتفاف الذي قد تحتوي عليه الأشكال.
// 1 - عائم:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - مضمنة:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// إذا كنت بحاجة إلى إنشاء أشكال "غير بدائية"، مثل SingleCornerSnipped، وTopCornersSnipped، وDiagonalCornersSnipped،
// TopCornersOneRoundedOneSnipped، أو SingleCornerRounded، أو TopCornersRounded، أو DiagonalCornersRounded،
// ثم احفظ المستند بالتوافق "الصارم" أو "الانتقالي"، والذي يسمح بحفظ الشكل بتنسيق DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

يوضح كيفية تكوين قائمة لإعادة بدء الترقيم في كل قسم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// الخاصية "IsRestartAtEachSection" ستكون قابلة للتطبيق فقط عندما
// مستوى توافق OOXML للمستند هو معيار أحدث من "OoxmlComplianceCore.Ecma376".
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

يوضح كيفية تعيين مواصفات توافق OOXML للمستند المحفوظ للالتزام به.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا قمنا بتكوين خيارات التوافق لتتوافق مع Microsoft Word 2003،
// إدراج صورة سيحدد شكلها باستخدام VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// لا يدعم معيار OOXML "ISO/IEC 29500:2008" أشكال VML.
// إذا قمنا بتعيين خاصية "الامتثال" لكائن SaveOptions على "OoxmlCompliance.Iso29500_2008_Strict"،
 // أي مستند نحفظه أثناء تمرير هذا الكائن يجب أن يتبع هذا المعيار.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// يحدد مستندنا المحفوظ الشكل باستخدام DML للالتزام بمعيار OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
