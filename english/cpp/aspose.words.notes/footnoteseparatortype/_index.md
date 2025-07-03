---
title: Aspose::Words::Notes::FootnoteSeparatorType enum
linktitle: FootnoteSeparatorType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Notes::FootnoteSeparatorType enum. Specifies the type of the footnote/endnote separator in C++.'
type: docs
weight: 6500
url: /cpp/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enum


Specifies the type of the footnote/endnote separator.

```cpp
enum class FootnoteSeparatorType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| FootnoteSeparator | 0 | Separator between main text and footnote text. |
| FootnoteContinuationSeparator | 1 | Printed above footnote text on a page when the text must be continued from a previous page. |
| FootnoteContinuationNotice | 2 | Printed below footnote text on a page when footnote text must be continued on a succeeding page. |
| EndnoteSeparator | 3 | Separator between main text and endnote text. |
| EndnoteContinuationSeparator | 4 | Printed above endnote text on a page when the text must be continued from a previous page. |
| EndnoteContinuationNotice | 5 | Printed below endnote text on a page when endnote text must be continued on a succeeding page. |


## Examples



Shows how to remove endnote separator. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> endnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::EndnoteSeparator);
// Remove endnote separator.
endnoteSeparator->get_FirstParagraph()->get_FirstChild()->Remove();
```


Shows how to manage footnote separator format. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Align footnote separator.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## See Also

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
