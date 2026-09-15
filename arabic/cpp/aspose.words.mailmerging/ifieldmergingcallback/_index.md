---
title: "واجهة Aspose::Words::MailMerging::IFieldMergingCallback"
linktitle: "IFieldMergingCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::MailMerging::IFieldMergingCallback. نفّذ هذه الواجهة إذا كنت تريد التحكم في كيفية إدراج البيانات في حقول الدمج أثناء عملية دمج البريد في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.mailmerging/ifieldmergingcallback/
---
## IFieldMergingCallback interface


نفّذ هذه الواجهة إذا كنت تريد التحكم في كيفية إدراج البيانات في حقول الدمج أثناء عملية دمج البريد.

```cpp
class IFieldMergingCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [FieldMerging](./fieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::FieldMergingArgs\>) | يتم استدعاؤها عندما يكون محرك دمج البريد Aspose.Words على وشك إدراج البيانات في حقل دمج في المستند. |
| [GetType](./gettype/)() const override |  |
| virtual [ImageFieldMerging](./imagefieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::ImageFieldMergingArgs\>) | يتم استدعاؤها عندما يكون محرك دمج البريد Aspose.Words على وشك إدراج صورة في حقل دمج. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
