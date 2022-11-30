---
title: MappedDataFieldCollection
second_title: Aspose.Words for C++ API Reference
description: Allows to automatically map between names of fields in your data source and names of mail merge fields in the document.
type: docs
weight: 66
url: /cpp/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class


Allows to automatically map between names of fields in your data source and names of mail merge fields in the document.

```cpp
class MappedDataFieldCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Adds a new field mapping. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Removes all elements from the collection. |
| [ContainsKey](./containskey/)(const System::String\&) | Determines whether a mapping from the specified field in the document exists in the collection. |
| [ContainsValue](./containsvalue/)(const System::String\&) | Determines whether a mapping from the specified field in the data source exists in the collection. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gets the number of elements contained in the collection. |
| [GetEnumerator](./getenumerator/)() override | Returns a dictionary enumerator object that can be used to iterate over all items in the collection. |
| [idx_get](./idx_get/)(const System::String\&) | Gets or sets the name of the field in the data source associated with the specified mail merge field. |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | Gets or sets the name of the field in the data source associated with the specified mail merge field. |
| [Remove](./remove/)(const System::String\&) | Removes a field mapping. |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Remarks


This is implemented as a collection of string keys into string values. The keys are the names of mail merge fields in the document and the values are the names of fields in your data source.

## See Also

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words](../../)
