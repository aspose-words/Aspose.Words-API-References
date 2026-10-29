---
title: Aspose::Words::MailMerging::IFieldMergingCallback interface
linktitle: IFieldMergingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::IFieldMergingCallback interface. Implement this interface if you want to control how data is inserted into merge fields during a mail merge operation in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.mailmerging/ifieldmergingcallback/
---
## IFieldMergingCallback interface


Implement this interface if you want to control how data is inserted into merge fields during a mail merge operation.

```cpp
class IFieldMergingCallback : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [FieldMerging](./fieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::FieldMergingArgs\>) | Called when the Aspose.Words mail merge engine is about to insert data into a merge field in the document. |
| virtual [ImageFieldMerging](./imagefieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::ImageFieldMergingArgs\>) | Called when the Aspose.Words mail merge engine is about to insert an image into a merge field. |
## See Also

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
