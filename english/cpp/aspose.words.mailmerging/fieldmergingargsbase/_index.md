---
title: Aspose::Words::MailMerging::FieldMergingArgsBase class
linktitle: FieldMergingArgsBase
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::FieldMergingArgsBase class. Base class for FieldMergingArgs and ImageFieldMergingArgs. To learn more, visit the  documentation article in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.mailmerging/fieldmergingargsbase/
---
## FieldMergingArgsBase class


Base class for [FieldMergingArgs](../fieldmergingargs/) and [ImageFieldMergingArgs](../imagefieldmergingargs/). To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) documentation article.

```cpp
class FieldMergingArgsBase : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Document](./get_document/)() const | Returns the [Document](./get_document/) object for which the mail merge is performed. |
| [get_DocumentFieldName](./get_documentfieldname/)() const | Gets the name of the merge field as specified in the document. |
| [get_Field](./get_field/)() const | Gets the object that represents the current merge field. |
| [get_FieldName](./get_fieldname/)() const | Gets the name of the merge field in the data source. |
| [get_FieldValue](./get_fieldvalue/)() const | Gets the value of the field from the data source. |
| [get_RecordIndex](./get_recordindex/)() const | Gets the zero based index of the record that is being merged. |
| [get_TableName](./get_tablename/)() const | Gets the name of the data table for the current merge operation or empty string if the name is not available. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](./set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Sets the value of the field from the data source. |
| static [Type](./type/)() |  |

## See Also

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
