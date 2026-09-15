---
title: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions constructor"
linktitle: "OdtSaveOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions constructor. يهيئ نسخة جديدة من هذا الصنف يمكن استخدامها لحفظ مستند بصيغة Odt في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions::OdtSaveOptions() constructor


يهيئ نسخة جديدة من هذا الصنف يمكن استخدامها لحفظ مستند بصيغة [Odt](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions()
```


## أمثلة



يظهر كيفية جعل المستند المحفوظ يتوافق مع مخطط ODT أقدم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## انظر أيضًا

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat) constructor


يهيئ نسخة جديدة من هذا الصنف يمكن استخدامها لحفظ مستند بصيغة [Odt](../../../aspose.words/saveformat/) أو [Ott](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | يمكن أن تكون [Odt](../../../aspose.words/saveformat/) أو [Ott](../../../aspose.words/saveformat/). |

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
## OdtSaveOptions::OdtSaveOptions(const System::String\&) constructor


يهيئ نسخة جديدة من هذا الصنف يمكن استخدامها لحفظ مستند بصيغة [Odt](../../../aspose.words/saveformat/) مشفّرة بكلمة مرور.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(const System::String &password)
```

## انظر أيضًا

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
