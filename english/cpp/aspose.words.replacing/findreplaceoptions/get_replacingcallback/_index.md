---
title: get_ReplacingCallback
second_title: Aspose.Words for C++ API Reference
description: The user-defined method which is called before every replace occurrence.
type: docs
weight: 170
url: /cpp/aspose.words.replacing/findreplaceoptions/get_replacingcallback/
---
## FindReplaceOptions::get_ReplacingCallback method


The user-defined method which is called before every replace occurrence.

```cpp
System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> Aspose::Words::Replacing::FindReplaceOptions::get_ReplacingCallback() const
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


Shows how to apply a different font to new content via [FindReplaceOptions](../). 
```cpp
void ConvertNumbersToHexadecimal()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    builder->get_Font()->set_Name(u"Arial");
    builder->Writeln(String(u"Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n") + u"123, 456, 789 and 17379.");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    auto options = MakeObject<FindReplaceOptions>();

    // Set the "HighlightColor" property to a background color that we want to apply to the operation's resulting text.
    options->get_ApplyFont()->set_HighlightColor(System::Drawing::Color::get_LightGray());

    auto numberHexer = MakeObject<ExRange::NumberHexer>();
    options->set_ReplacingCallback(numberHexer);

    int replacementCount = doc->get_Range()->Replace(MakeObject<System::Text::RegularExpressions::Regex>(u"[0-9]+"), u"", options);

    std::cout << numberHexer->GetLog() << std::endl;

    ASSERT_EQ(4, replacementCount);
    ASSERT_EQ(String(u"Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\r") + u"0x7B, 0x1C8, 0x315 and 0x43E3.",
              doc->GetText().Trim());
    auto isLightGray = [](SharedPtr<Run> r)
    {
        return r->get_Font()->get_HighlightColor().ToArgb() == System::Drawing::Color::get_LightGray().ToArgb();
    };

    ASSERT_EQ(4, doc->GetChildNodes(NodeType::Run, true)->LINQ_OfType<SharedPtr<Run>>()->LINQ_Count(isLightGray));
}

class NumberHexer : public IReplacingCallback
{
public:
    ReplaceAction Replacing(SharedPtr<ReplacingArgs> args) override
    {
        mCurrentReplacementNumber++;

        int number = System::Convert::ToInt32(args->get_Match()->get_Value());

        args->set_Replacement(String::Format(u"0x{0:X}", number));

        mLog->AppendLine(String::Format(u"Match #{0}", mCurrentReplacementNumber));
        mLog->AppendLine(String::Format(u"\tOriginal value:\t{0}", args->get_Match()->get_Value()));
        mLog->AppendLine(String::Format(u"\tReplacement:\t{0}", args->get_Replacement()));
        mLog->AppendLine(String::Format(u"\tOffset in parent {0} node:\t{1}", args->get_MatchNode()->get_NodeType(), args->get_MatchOffset()));

        mLog->AppendLine(String::IsNullOrEmpty(args->get_GroupName()) ? String::Format(u"\tGroup index:\t{0}", args->get_GroupIndex())
                                                                      : String::Format(u"\tGroup name:\t{0}", args->get_GroupName()));

        return ReplaceAction::Replace;
    }

    String GetLog()
    {
        return mLog->ToString();
    }

    NumberHexer() : mCurrentReplacementNumber(0), mLog(MakeObject<System::Text::StringBuilder>())
    {
    }

private:
    int mCurrentReplacementNumber;
    SharedPtr<System::Text::StringBuilder> mLog;
};
```

## See Also

* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words](../../../)
