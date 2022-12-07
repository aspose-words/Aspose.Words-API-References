---
title: RevisionGroupCollection
second_title: Aspose.Words for C++ API Reference
description: A collection of RevisionGroup objects that represent revision groups in the document. To learn more, visit the  documentation article.
type: docs
weight: 703
url: /cpp/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class


A collection of [RevisionGroup](../revisiongroup/) objects that represent revision groups in the document. To learn more, visit the [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/) documentation article.

```cpp
class RevisionGroupCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::RevisionGroup>>
```

## Methods

| Method | Description |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Returns the number of revision groups in the collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returns a revision group at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
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


You do not create instances of this class directly. Use the [Groups](../revisioncollection/get_groups/) property to get revision groups present in a document.

## Examples



Shows how to print info about a group of revisions in a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Revisions.docx");

ASSERT_EQ(7, doc->get_Revisions()->get_Groups()->get_Count());

for (const auto& group : doc->get_Revisions()->get_Groups())
{
    std::cout << String::Format(u"Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group->get_Author(), group->get_RevisionType(),
                                group->get_Text())
              << std::endl;
}
```


Shows how to get a group of revisions in a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Revisions.docx");

SharedPtr<RevisionGroup> revisionGroup = doc->get_Revisions()->get_Groups()->idx_get(0);
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
