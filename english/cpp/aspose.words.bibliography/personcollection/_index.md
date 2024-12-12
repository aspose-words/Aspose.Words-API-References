---
title: Aspose::Words::Bibliography::PersonCollection class
linktitle: PersonCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Bibliography::PersonCollection class. Represents a list of persons who are bibliography source contributors in C++.'
type: docs
weight: 750
url: /cpp/aspose.words.bibliography/personcollection/
---
## PersonCollection class


Represents a list of persons who are bibliography source contributors.

```cpp
class PersonCollection : public Aspose::Words::Bibliography::Contributor,
                         public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bibliography::Person>>
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Bibliography::Person\>\&) | Adds a [Person](../person/) to the collection. |
| [Clear](./clear/)() | Removes all items from the collection. |
| [Contains](./contains/)(const System::SharedPtr\<Aspose::Words::Bibliography::Person\>\&) | Determines whether the collection contains a specific person. |
| [get_Count](./get_count/)() | Gets the number of persons contained in the collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gets or sets a person at the specified index. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Bibliography::Person\>\&) | Gets or sets a person at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PersonCollection](./personcollection/)() | Initialize a new instance of the [PersonCollection](./) class. |
| [PersonCollection](./personcollection/)(const System::SharedPtr\<System::Collections::Generic::IEnumerable\<System::SharedPtr\<Aspose::Words::Bibliography::Person\>\>\>\&) |  |
| [PersonCollection](./personcollection/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Bibliography::Person\>\>\&) | Initialize a new instance of the [PersonCollection](./) class. |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Bibliography::Person\>\&) | Removes the person from the collection. |
| [RemoveAt](./removeat/)(int32_t) | Removes the person at the specified index. |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| static [Type](./type/)() |  |
## See Also

* Class [Contributor](../contributor/)
* Namespace [Aspose::Words::Bibliography](../)
* Library [Aspose.Words for C++](../../)
