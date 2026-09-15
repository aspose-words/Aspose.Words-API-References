---
title: "Aspose::Words::Saving::OdtSaveOptions::get_Password method"
linktitle: "get_Password"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::OdtSaveOptions::get_Password method. يحصل على أو يعيّن كلمة مرور لتشفير المستند في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/odtsaveoptions/get_password/
---
## OdtSaveOptions::get_Password method


يحصل أو يعيّن كلمة مرور لتشفير المستند.

```cpp
System::String Aspose::Words::Saving::OdtSaveOptions::get_Password() const
```

## ملاحظات


لحفظ المستند بدون تشفير يجب أن تكون هذه الخاصية **null** أو سلسلة فارغة.

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

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
