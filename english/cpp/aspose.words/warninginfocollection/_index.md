---
title: Aspose::Words::WarningInfoCollection class
linktitle: WarningInfoCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::WarningInfoCollection class. Represents a typed collection of WarningInfo objects. To learn more, visit the  documentation article in C++.'
type: docs
weight: 75000
url: /cpp/aspose.words/warninginfocollection/
---
## WarningInfoCollection class


Represents a typed collection of [WarningInfo](../warninginfo/) objects. To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) documentation article.

```cpp
class WarningInfoCollection : public Aspose::Words::IWarningCallback,
                              public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::WarningInfo>>
```

## Methods

| Method | Description |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Removes all elements from the collection. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gets the number of elements contained in the collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gets an item at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
| [Warning](./warning/)(System::SharedPtr\<Aspose::Words::WarningInfo\>) override | Implements the [IWarningCallback](../iwarningcallback/) interface. Adds a warning to this collection. |
| [WarningInfoCollection](./warninginfocollection/)() |  |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Remarks


You can use this collection object as the simplest form of [IWarningCallback](../iwarningcallback/) implementation to gather all warnings that Aspose.Words generates during a load or save operation. Create an instance of this class and assign it to the [WarningCallback](../../aspose.words.loading/loadoptions/get_warningcallback/) or [WarningCallback](../documentbase/get_warningcallback/) property.

## See Also

* Interface [IWarningCallback](../iwarningcallback/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
