---
title: GetEnumerator
second_title: Aspose.Words for C++ API Reference
description: Returns an enumerator object.
type: docs
weight: 40
url: /cpp/aspose.words/revisioncollection/getenumerator/
---
## RevisionCollection::GetEnumerator method


Returns an enumerator object.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Revision>>> Aspose::Words::RevisionCollection::GetEnumerator() override
```


## Examples



Shows how to work with a document's collection of revisions. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Revisions.docx");
SharedPtr<RevisionCollection> revisions = doc->get_Revisions();

// This collection itself has a collection of revision groups.
// Each group is a sequence of adjacent revisions.
std::cout << revisions->get_Groups()->get_Count() << " revision groups:" << std::endl;

// Iterate over the collection of groups and print the text that the revision concerns.
{
    SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<RevisionGroup>>> e = revisions->get_Groups()->GetEnumerator();
    while (e->MoveNext())
    {
        std::cout << (String::Format(u"\tGroup type \"{0}\", ", e->get_Current()->get_RevisionType()) +
                      String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_Text().Trim()))
                  << std::endl;
    }
}

// Each Run that a revision affects gets a corresponding Revision object.
// The revisions' collection is considerably larger than the condensed form we printed above,
// depending on how many Runs we have segmented the document into during Microsoft Word editing.
std::cout << "\n" << revisions->get_Count() << " revisions:" << std::endl;

{
    SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<Revision>>> e = revisions->GetEnumerator();
    while (e->MoveNext())
    {
        // A StyleDefinitionChange strictly affects styles and not document nodes. This means the "ParentStyle"
        // property will always be in use, while the ParentNode will always be null.
        // Since all other changes affect nodes, ParentNode will conversely be in use, and ParentStyle will be null.
        if (e->get_Current()->get_RevisionType() == RevisionType::StyleDefinitionChange)
        {
            std::cout << (String::Format(u"\tRevision type \"{0}\", ", e->get_Current()->get_RevisionType()) +
                          String::Format(u"author: {0}, style: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_ParentStyle()->get_Name()))
                      << std::endl;
        }
        else
        {
            std::cout << (String::Format(u"\tRevision type \"{0}\", ", e->get_Current()->get_RevisionType()) +
                          String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(),
                                         e->get_Current()->get_ParentNode()->GetText().Trim()))
                      << std::endl;
        }
    }
}

// Reject all revisions via the collection, reverting the document to its original form.
revisions->RejectAll();

ASSERT_EQ(0, revisions->get_Count());
```

## See Also

* Class [Revision](../../revision/)
* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
