---
title: get_UseLegacyOrder
second_title: Aspose.Words for C++ API Reference
description: True indicates that a text search is performed sequentially from top to bottom considering the text boxes. Default value is false.
type: docs
weight: 209
url: /cpp/aspose.words.replacing/findreplaceoptions/get_uselegacyorder/
---
## FindReplaceOptions::get_UseLegacyOrder method


True indicates that a text search is performed sequentially from top to bottom considering the text boxes. Default value is **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_UseLegacyOrder() const
```


## Examples



Shows how to change the searching order of nodes when performing a find-and-replace text operation. 
```cpp
void UseLegacyOrder(bool useLegacyOrder)
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    // Insert three runs which we can search for using a regex pattern.
    // Place one of those runs inside a text box.
    builder->Writeln(u"[tag 1]");
    SharedPtr<Shape> textBox = builder->InsertShape(ShapeType::TextBox, 100, 50);
    builder->Writeln(u"[tag 2]");
    builder->MoveTo(textBox->get_FirstParagraph());
    builder->Write(u"[tag 3]");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    auto options = MakeObject<FindReplaceOptions>();

    // Assign a custom callback to the "ReplacingCallback" property.
    auto callback = MakeObject<ExRange::TextReplacementTracker>();
    options->set_ReplacingCallback(callback);

    // If we set the "UseLegacyOrder" property to "true", the
    // find-and-replace operation will go through all the runs outside of a text box
    // before going through the ones inside a text box.
    // If we set the "UseLegacyOrder" property to "false", the
    // find-and-replace operation will go over all the runs in a range in sequential order.
    options->set_UseLegacyOrder(useLegacyOrder);

    doc->get_Range()->Replace(MakeObject<System::Text::RegularExpressions::Regex>(u"\\[tag \\d*\\]"), u"", options);

    SharedPtr<System::Collections::Generic::List<String>> matches = MakeObject<System::Collections::Generic::List<String>>();
    matches->Add(u"[tag 1]");
    if (useLegacyOrder)
    {
        matches->Add(u"[tag 3]");
        matches->Add(u"[tag 2]");
    }
    else
    {
        matches->Add(u"[tag 2]");
        matches->Add(u"[tag 3]");
    }
    ASPOSE_ASSERT_EQ(matches, callback->get_Matches());
}

class TextReplacementTracker : public IReplacingCallback
{
public:
    SharedPtr<System::Collections::Generic::List<String>> get_Matches()
    {
        return mMatches;
    }

    TextReplacementTracker() : mMatches(MakeObject<System::Collections::Generic::List<String>>())
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

## See Also

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words](../../../)
