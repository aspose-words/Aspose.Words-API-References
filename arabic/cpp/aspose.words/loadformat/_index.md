---
title: "تعداد Aspose::Words::LoadFormat"
linktitle: "LoadFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::LoadFormat enum. يشير إلى تنسيق المستند الذي سيتم تحميله في C++."
type: docs
weight: 97000
url: /ar/cpp/aspose.words/loadformat/
---
## LoadFormat enum


يشير إلى تنسيق المستند الذي سيتم تحميله.

```cpp
enum class LoadFormat
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| تلقائي | 0 | يُوجه Aspose.Words لتحديد التنسيق تلقائيًا. |
| MsWorks | 8 | Microsoft Works 8 [Document](../document/). |
| Doc | 10 | Microsoft Word 95 أو Word 97 - 2003 [Document](../document/). |
| Dot | 11 | قالب Microsoft Word 95 أو Word 97 - 2003. |
| DocPreWord60 | 12 | المستند بتنسيق pre-Word 95. لا يدعم Aspose.Words حاليًا تحميل مثل هذه المستندات. |
| Docx | 20 | Office Open XML WordprocessingML [Document](../document/) (بدون ماكرو). |
| Docm | 21 | Office Open XML WordprocessingML Macro-Enabled [Document](../document/). |
| Dotx | 22 | قالب Office Open XML WordprocessingML (بدون ماكرو). |
| Dotm | 23 | قالب Office Open XML WordprocessingML Macro-Enabled. |
| FlatOpc | 24 | Office Open XML WordprocessingML مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcMacroEnabled | 25 | Office Open XML WordprocessingML Macro-Enabled [Document](../document/) مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcTemplate | 26 | قالب Office Open XML WordprocessingML (بدون ماكرو) مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| FlatOpcTemplateMacroEnabled | 27 | قالب Office Open XML WordprocessingML Macro-Enabled مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| Rtf | 30 | تنسيق RTF. |
| WordML | 31 | تنسيق Microsoft Word 2003 WordprocessingML. |
| Html | 50 | تنسيق HTML. |
| Mhtml | 51 | تنسيق MHTML (أرشيف ويب). |
| Mobi | 52 | تنسيق MOBI. يُستخدم بواسطة قارئ MobiPocket وقارئات Amazon Kindle. |
| Chm | 53 | تنسيق CHM (مساعدة HTML المجمعة). |
| Azw3 | 54 | تنسيق AZW3. يُستخدم بواسطة قارئات Amazon Kindle. |
| Epub | 55 | تنسيق EPUB. |
| Odt | 60 | نص ODF [Document](../document/). |
| Ott | 61 | قالب نص ODF [Document](../document/). |
| Text | 62 | نص عادي. |
| Markdown | 63 | مستند نص Markdown. |
| Xml | 65 | مستند XML. |
| Unknown | 255 | تنسيق غير معروف، لا يمكن تحميله بواسطة [Aspose.Words](../). |


## أمثلة



يظهر كيفية استخدام طرق [FileFormatUtil](../fileformatutil/) لاكتشاف تنسيق المستند.
```cpp
// حمّل مستندًا من ملف يفتقر إلى امتداد ملف، ثم اكتشف تنسيق الملف.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // فيما يلي طريقتان لتحويل LoadFormat إلى SaveFormat المقابل.
    // 1 - احصل على سلسلة امتداد الملف لـ LoadFormat، ثم احصل على SaveFormat المقابل من تلك السلسلة:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 - حوّل LoadFormat مباشرةً إلى SaveFormat الخاص به:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // حمّل مستندًا من الدفق، ثم احفظه بامتداد الملف المكتشف تلقائيًا.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```


يعرض كيفية تحديد عنوان URI أساسي عند فتح مستند html.
```cpp
// افترض أننا نريد تحميل مستند .html يحتوي على صورة مرتبطة بعنوان URI نسبي
// في حين أن الصورة موجودة في موقع مختلف. في هذه الحالة، سنحتاج إلى تحويل عنوان URI النسبي إلى عنوان مطلق.
// يمكننا توفير عنوان URI أساسي باستخدام كائن HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// بينما كانت الصورة مكسورة في ملف .html المدخل، ساعدنا عنوان URI الأساسي المخصص في إصلاح الرابط.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// سيعرض مستند الإخراج هذه الصورة التي كانت مفقودة.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
