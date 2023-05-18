---
title: Aspose::Words::Replacing::ReplacingArgs::get_Replacement method
linktitle: get_Replacement
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::ReplacingArgs::get_Replacement method. Gets or sets the replacement string in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.replacing/replacingargs/get_replacement/
---
## ReplacingArgs::get_Replacement method


Gets or sets the replacement string.

```cpp
System::String Aspose::Words::Replacing::ReplacingArgs::get_Replacement() const
```


## Examples



Shows how to replace all occurrences of a regular expression pattern with another string, while tracking all such replacements. 
```cpp
void ReplaceWithCallback()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    builder->Writeln(String(u"Our new location in New York City is opening tomorrow. ") + u"Hope to see all our NYC-based customers at the opening!");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    auto options = MakeObject<FindReplaceOptions>();

    // Set a callback that tracks any replacements that the "Replace" method will make.
    auto logger = MakeObject<ExRange::TextFindAndReplacementLogger>();
    options->set_ReplacingCallback(logger);

    doc->get_Range()->Replace(MakeObject<System::Text::RegularExpressions::Regex>(u"New York City|NYC"), u"Washington", options);

    ASSERT_EQ(String(u"Our new location in (Old value:\"New York City\") Washington is opening tomorrow. ") +
                  u"Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!",
              doc->GetText().Trim());

    ASSERT_EQ(String(u"\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n") +
                  u"\"NYC\" converted to \"Washington\" 42 characters into a Run node.",
              logger->GetLog().Trim());
}

class TextFindAndReplacementLogger : public IReplacingCallback
{
public:
    String GetLog()
    {
        return mLog->ToString();
    }

    TextFindAndReplacementLogger() : mLog(MakeObject<System::Text::StringBuilder>())
    {
    }

private:
    SharedPtr<System::Text::StringBuilder> mLog;

    ReplaceAction Replacing(SharedPtr<ReplacingArgs> args) override
    {
        mLog->AppendLine(String::Format(u"\"{0}\" converted to \"{1}\" ", args->get_Match()->get_Value(), args->get_Replacement()) +
                         String::Format(u"{0} characters into a {1} node.", args->get_MatchOffset(), args->get_MatchNode()->get_NodeType()));

        args->set_Replacement(String::Format(u"(Old value:\"{0}\") {1}", args->get_Match()->get_Value(), args->get_Replacement()));
        return ReplaceAction::Replace;
    }
};
```

## See Also

* Class [ReplacingArgs](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
