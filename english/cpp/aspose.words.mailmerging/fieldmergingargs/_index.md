---
title: Aspose::Words::MailMerging::FieldMergingArgs class
linktitle: FieldMergingArgs
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::FieldMergingArgs class. Provides data for the MergeField event. To learn more, visit the  documentation article in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class


Provides data for the **MergeField** event. To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) documentation article.

```cpp
class FieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Methods

| Method | Description |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Returns the [Document](../fieldmergingargsbase/get_document/) object for which the mail merge is performed. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Gets the name of the merge field as specified in the document. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Gets the object that represents the current merge field. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Gets the name of the merge field in the data source. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Gets the value of the field from the data source. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Gets the zero based index of the record that is being merged. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Gets the name of the data table for the current merge operation or empty string if the name is not available. |
| [get_Text](./get_text/)() const | Gets or sets the text that will be inserted into the document for the current merge field. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Sets the value of the field from the data source. |
| [set_Text](./set_text/)(const System::String\&) | Setter for [Aspose::Words::MailMerging::FieldMergingArgs::get_Text](./get_text/). |
| static [Type](./type/)() |  |
## Remarks


The **MergeField** event occurs during mail merge when a simple mail merge field is encountered in the document. You can respond to this event to return text for the mail merge engine to insert into the document.

## See Also

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
