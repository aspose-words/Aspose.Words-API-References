---
title: "طريقة Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat. تحدد الصيغة التي سيُحفظ بها المستند إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن تكون Odt أو Ott في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.saving/odtsaveoptions/get_saveformat/
---
## OdtSaveOptions::get_SaveFormat method


تحدد الصيغة التي سيُحفظ بها المستند إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن تكون [Odt](../../../aspose.words/saveformat/) أو [Ott](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat() override
```


## أمثلة



يوضح كيفية تشفير مستند ODT/OTT محفوظ باستخدام كلمة مرور، ثم تحميله باستخدام Aspose.Words.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// إنشاء OdtSaveOptions جديد، وتمرير إما "SaveFormat.Odt"،
// أو "SaveFormat.Ott" كالصيغة لحفظ المستند فيها.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(saveFormat);
saveOptions->set_Password(u"@sposeEncrypted_1145");

System::String extensionString = Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat);

// إذا فتحنا هذا المستند باستخدام محرر مناسب،
// سوف يطلب منا كلمة المرور التي حددناها في كائن SaveOptions.
doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, saveOptions);

System::SharedPtr<Aspose::Words::FileFormatInfo> docInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString);

ASSERT_TRUE(docInfo->get_IsEncrypted());

// إذا رغبنا في فتح أو تعديل هذا المستند مرة أخرى باستخدام Aspose.Words،
// سيتعين علينا توفير كائن LoadOptions مع كلمة المرور الصحيحة إلى مُنشئ التحميل.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"@sposeEncrypted_1145"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
