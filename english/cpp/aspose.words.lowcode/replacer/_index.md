---
title: Aspose::Words::LowCode::Replacer class
linktitle: Replacer
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Replacer class. Provides methods intended to find and replace text in the document in C++.'
type: docs
weight: 1250
url: /cpp/aspose.words.lowcode/replacer/
---
## Replacer class


Provides methods intended to find and replace text in the document.

```cpp
class Replacer : public Aspose::Words::LowCode::Processor
```

## Methods

| Method | Description |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ReplacerContext\>\&) | Creates new instance of the replacer processor. |
| [Execute](../processor/execute/)() | Execute the processor action. |
| [From](../processor/from/)(const System::String\&) | Specifies input document for processing. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifies input document for processing. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Specifies input document for processing. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifies input document for processing. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file, with the specified save format and additional options. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file, with the specified save format and additional options. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file, with the specified save format and additional options. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file, with the specified save format and additional options. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input stream, with the specified save format and additional options. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input stream, with the specified save format and additional options. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input stream, with the specified save format and additional options. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input stream, with the specified save format and additional options. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file using a regular expression. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file using a regular expression, with the specified save format and additional options. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file using a regular expression, with the specified save format and additional options. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input stream using a regular expression, with the specified save format and additional options. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input stream using a regular expression, with the specified save format and additional options. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file. Renders output to images. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file. Renders output to images. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file. Renders output to images. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file. Renders output to images. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Replaces all occurrences of a specified regular expression pattern with a replacement string in the input file. Renders output to images. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Replaces all occurrences of a specified regular expression pattern with a replacement string in the input file. Renders output to images. |
| [To](../processor/to/)(const System::String\&) | Specifies output file for the processor. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Specifies output file for the processor. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Specifies output file for the processor. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Specifies output stream for the processor. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Specifies output stream for the processor. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## See Also

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
