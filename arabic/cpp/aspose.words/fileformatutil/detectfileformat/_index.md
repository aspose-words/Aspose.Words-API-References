---
title: "طريقة Aspose::Words::FileFormatUtil::DetectFileFormat"
linktitle: "DetectFileFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::FileFormatUtil::DetectFileFormat. تكتشف وتعيد المعلومات حول تنسيق مستند مخزن في تدفق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/fileformatutil/detectfileformat/
---
## FileFormatUtil::DetectFileFormat(const System::SharedPtr\<System::IO::Stream\>\&) method


يكشف ويعيد المعلومات حول صيغة مستند مخزن في تدفق.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::SharedPtr<System::IO::Stream> &stream)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| تدفق | const System::SharedPtr\<System::IO::Stream\>\& | التدفق. |

### ReturnValue

كائن [FileFormatInfo](../../fileformatinfo/) يحتوي على المعلومات المكتشفة.
## ملاحظات


يجب أن يكون التدفق موضعه في بداية المستند.

عند عودة هذه الطريقة، يتم استعادة موضع التدفق إلى الموضع الأصلي.

حتى إذا اكتشفت هذه الطريقة تنسيق المستند، فإنها لا تضمن أن المستند المحدد صالح. هذه الطريقة تكتشف تنسيق المستند فقط بقراءة البيانات الكافية للاكتشاف. للتحقق الكامل من صلاحية المستند، تحتاج إلى تحميل المستند إلى كائن [Document](../../document/).

تقوم هذه الطريقة برمي [FileCorruptedException](../../filecorruptedexception/) عندما يتم التعرف على التنسيق، لكن لا يمكن إكمال الكشف بسبب الفساد.

## أمثلة



يظهر كيفية استخدام طرق [FileFormatUtil](../) لاكتشاف تنسيق المستند.
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

## انظر أيضًا

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(const System::String\&) method


يكشف ويعيد المعلومات حول صيغة مستند مخزن في ملف على القرص.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::String &fileName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | اسم الملف. |

### ReturnValue

كائن [FileFormatInfo](../../fileformatinfo/) يحتوي على المعلومات المكتشفة.
## ملاحظات


حتى إذا اكتشفت هذه الطريقة تنسيق المستند، فإنها لا تضمن أن المستند المحدد صالح. هذه الطريقة تكتشف تنسيق المستند فقط بقراءة البيانات الكافية للاكتشاف. للتحقق الكامل من صلاحية المستند، تحتاج إلى تحميل المستند إلى كائن [Document](../../document/).

تقوم هذه الطريقة برمي [FileCorruptedException](../../filecorruptedexception/) عندما يتم التعرف على التنسيق، لكن لا يمكن إكمال الكشف بسبب الفساد.

## أمثلة



يوضح كيفية استخدام الفئة [FileFormatUtil](../) لاكتشاف تنسيق المستند والتشفير.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// قم بتهيئة كائن SaveOptions لتشفير المستند
// مع كلمة مرور عند حفظه، ثم احفظ المستند.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// تحقق من نوع ملف مستندنا وحالة تشفيره.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```


يوضح كيفية استخدام الفئة [FileFormatUtil](../) لاكتشاف تنسيق المستند ووجود التوقيعات الرقمية.
```cpp
// استخدم مثيل FileFormatInfo للتحقق من أن المستند غير موقع رقمياً.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx");

ASSERT_EQ(u".docx", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// استخدم FileFormatInstance جديدًا لتأكيد أنه موقع.
info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// يمكننا تحميل والوصول إلى توقيعات مستند موقع في مجموعة مثل هذه.
ASSERT_EQ(1, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx")->get_Count());
```

## انظر أيضًا

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(std::basic_istream<CharType, Traits> &stream)
```

## انظر أيضًا

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
