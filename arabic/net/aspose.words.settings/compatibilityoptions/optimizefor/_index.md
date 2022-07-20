---
title: OptimizeFor
second_title: Aspose.Words لمراجع .NET API
description: يسمح بتحسين محتويات المستند بالإضافة إلى سلوك Aspose.Words الافتراضي لإصدارات معينة من MS Word.
type: docs
weight: 720
url: /ar/net/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions.OptimizeFor method

يسمح بتحسين محتويات المستند بالإضافة إلى سلوك Aspose.Words الافتراضي لإصدارات معينة من MS Word.

استخدم هذه الطريقة لمنع MS Word من عرض شريط "وضع التوافق" عند تحميل المستند. (لاحظ أنك قد تحتاج أيضًا إلى تعيين[`Compliance`](../../../aspose.words.saving/ooxmlsaveoptions/compliance) الخاصية إلى Iso29500_2008_Transitional أو أعلى.) _ x000d_

```csharp
public void OptimizeFor(MsWordVersion version)
```

### أمثلة

يوضح كيفية محاذاة محتويات النص لمربع نص عموديًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// قم بتعيين خاصية "VerticalAnchor" على "TextBoxAnchor.Top" إلى
// محاذاة النص في مربع النص هذا مع الجانب العلوي للشكل.
// اضبط خاصية "VerticalAnchor" على "TextBoxAnchor.Middle" على
// محاذاة النص في مربع النص هذا إلى وسط الشكل.
// قم بتعيين خاصية "VerticalAnchor" على "TextBoxAnchor.Bottom" إلى
// محاذاة النص في مربع النص هذا إلى أسفل الشكل.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// المحاذاة الرأسية للنص داخل مربعات النص متاحة من Microsoft Word 2007 وما بعده.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

يوضح كيفية تعيين مواصفات توافق OOXML لمستند محفوظ للالتزام به.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا قمنا بتكوين خيارات التوافق لتتوافق مع Microsoft Word 2003 ،
// إدراج صورة سيحدد شكلها باستخدام VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// لا يدعم معيار OOXML "ISO / IEC 29500: 2008" أشكال VML.
// إذا قمنا بتعيين خاصية "الامتثال" لكائن SaveOptions على "OoxmlCompliance.Iso29500_2008_Strict" ،
 // أي مستند نقوم بحفظه أثناء تمرير هذا الكائن يجب أن يتبع هذا المعيار.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// يحدد المستند المحفوظ الشكل باستخدام DML للالتزام بمعيار OOXML "ISO / IEC 29500: 2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

يوضح كيفية تحسين المستند لإصدارات مختلفة من Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // يحتوي هذا الكائن على قائمة واسعة من العلامات الفريدة لكل مستند
    // التي تسمح لنا بتسهيل التوافق مع الإصدارات القديمة من Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // طباعة الإعدادات الافتراضية لمستند فارغ.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // يمكننا الوصول إلى هذه الإعدادات في Microsoft Word عبر "ملف" - >; "خيارات" - >. "متقدم" - >. "خيارات التوافق لـ ...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // يمكننا استخدام طريقة OptimizeFor لضمان التوافق الأمثل مع إصدار معين من Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// يجمع كل العلامات في كائن خيارات توافق المستند حسب الحالة ، ثم يطبع كل مجموعة.
/// </summary>
private static void PrintCompatibilityOptions(CompatibilityOptions options)
{
    for (int i = 1; i >= 0; i--)
    {
        Console.WriteLine(Convert.ToBoolean(i) ? "\tEnabled options:" : "\tDisabled options:");
        SortedSet<string> optionNames = new SortedSet<string>();

        foreach (System.ComponentModel.PropertyDescriptor descriptor in System.ComponentModel.TypeDescriptor.GetProperties(options))
        {
            if (descriptor.PropertyType == Type.GetType("System.Boolean") && i == Convert.ToInt32(descriptor.GetValue(options)))
            {
                optionNames.Add(descriptor.Name);
            }
        }

        foreach (string s in optionNames)
        {
            Console.WriteLine($"\t\t{s}");
        }
    }
}
```

### أنظر أيضا

* enum [MsWordVersion](../../mswordversion)
* class [CompatibilityOptions](../../compatibilityoptions)
* مساحة الاسم [Aspose.Words.Settings](../../compatibilityoptions)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
