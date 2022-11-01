---
title: get_Match
second_title: Aspose.Words for C++ API Reference
description: The Match resulting from a single regular expression match during a Replace.
type: docs
weight: 27
url: /cpp/aspose.words.replacing/replacingargs/get_match/
---
## ReplacingArgs.get_Match method


The **Match** resulting from a single regular expression match during a **Replace**.

```cpp
System::SharedPtr<System::Text::RegularExpressions::Match> Aspose::Words::Replacing::ReplacingArgs::get_Match() const
```


**Match.Index** gets the zero-based starting position of the match from the start of the find and replace range.

## Examples

Shows how to apply a different font to new content via FindReplaceOptions.
```cpp
void ConvertNumbersToHexadecimal()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    builder->get_Font()->set_Name(u"Arial");
    builder->Writeln(String(u"Numbers that the find-and-replace operation will convert to hexadecimal and highlight:") + u"123, 456, 789 and 17379.");

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

/// <summary>
/// Replaces numeric find-and-replacement matches with their hexadecimal equivalents.
/// Maintains a log of every replacement.
/// </summary>
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
                                                                      : String::Format(u"\tGroup name:\t{0}", args->[get_GroupName()](../get_groupname/)));**

        return ReplaceAction::Replace;
    }

    String GetLog() { return mLog->ToString(); }

    NumberHexer() : mCurrentReplacementNumber(0), mLog(MakeObject<System::Text::StringBuilder>()) { }

private:
    int mCurrentReplacementNumber;
    SharedPtr<System::Text::StringBuilder> mLog;
};
```
