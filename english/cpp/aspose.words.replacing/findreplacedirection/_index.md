---
title: FindReplaceDirection
second_title: Aspose.Words for C++ API Reference
description: Specifies direction for replace operations.
type: docs
weight: 40
url: /cpp/aspose.words.replacing/findreplacedirection/
---
## FindReplaceDirection enum


Specifies direction for replace operations.

### Values

| Name | Value | Description |
| --- | --- | --- |
| Forward | 0 | Matched items are replaced from first to last. |
| Backward | 1 | Matched items are replaced from last back to first. |


## Examples




Shows how to determine which direction a find-and-replace operation traverses the document in. 
```cpp
void Direction(FindReplaceDirection findReplaceDirection)
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    // Insert three runs which we can search for using a regex pattern.
    // Place one of those runs inside a text box.
    builder->Writeln(u"Match 1.");
    builder->Writeln(u"Match 2.");
    builder->Writeln(u"Match 3.");
    builder->Writeln(u"Match 4.");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    auto options = MakeObject<FindReplaceOptions>();

    // Assign a custom callback to the "ReplacingCallback" property.
    auto callback = MakeObject<ExRange::TextReplacementRecorder>();
    options->set_ReplacingCallback(callback);

    // Set the "Direction" property to "FindReplaceDirection.Backward" to get the find-and-replace
    // operation to start from the end of the range, and traverse back to the beginning.
    // Set the "Direction" property to "FindReplaceDirection.Backward" to get the find-and-replace
    // operation to start from the beginning of the range, and traverse to the end.
    options->set_Direction(findReplaceDirection);

    doc->get_Range()->Replace(MakeObject<System::Text::RegularExpressions::Regex>(u"Match \\d*"), u"Replacement", options);

    ASSERT_EQ(String(u"Replacement.\r") + u"Replacement.\r" + u"Replacement.\r" + u"Replacement.", doc->GetText().Trim());

    switch (findReplaceDirection)
    {
    case FindReplaceDirection::Forward:
        ASPOSE_ASSERT_EQ(MakeArray<String>({u"Match 1", u"Match 2", u"Match 3", u"Match 4"}), callback->get_Matches());
        break;

    case FindReplaceDirection::Backward:
        ASPOSE_ASSERT_EQ(MakeArray<String>({u"Match 4", u"Match 3", u"Match 2", u"Match 1"}), callback->get_Matches());
        break;
    }
}

class TextReplacementRecorder : public IReplacingCallback
{
public:
    SharedPtr<System::Collections::Generic::List<String>> get_Matches()
    {
        return mMatches;
    }

    TextReplacementRecorder() : mMatches(MakeObject<System::Collections::Generic::List<String>>())
    {
    }

private:
    SharedPtr<System::Collections::Generic::List<String>> mMatches;

    ReplaceAction Replacing(SharedPtr<ReplacingArgs> e) override
    {
        get_Matches()->Add(e->get_Match()->get_Value());
        return ReplaceAction::Replace;
    }
};
```

