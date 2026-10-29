---
title: Aspose::Words::MailMerging::MappedDataFieldCollection class
linktitle: MappedDataFieldCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::MappedDataFieldCollection class. Allows to automatically map between names of fields in your data source and names of mail merge fields in the document. To learn more, visit the Mail Merge and Reporting documentation article in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class


Allows to automatically map between names of fields in your data source and names of mail merge fields in the document. 
To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) documentation article.

```cpp
class MappedDataFieldCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(const System::String \&, const System::String \&) | Adds a new field mapping. |
| [Clear](./clear/)() | Removes all elements from the collection. |
| [ContainsKey](./containskey/)(const System::String \&) | Determines whether a mapping from the specified field in the document exists in the collection. |
| [ContainsValue](./containsvalue/)(const System::String \&) | Determines whether a mapping from the specified field in the data source exists in the collection. |
| [GetEnumerator](./getenumerator/)() override | Returns a dictionary enumerator object that can be used to iterate over all items in the collection. |
| [Remove](./remove/)(const System::String \&) | Removes a field mapping. |
| [get_Count](./get_count/)() | Gets the number of elements contained in the collection. |
| [idx_get](./idx_get/)(const System::String \&) | Gets or sets the name of the field in the data source associated with the specified mail merge field. |
| [idx_set](./idx_set/)(const System::String \&, const System::String \&) | Gets or sets the name of the field in the data source associated with the specified mail merge field. |
## Remarks


This is implemented as a collection of string keys into string values. The keys are the names of mail merge fields in the document and the values are the names of fields in your data source.
## See Also

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
