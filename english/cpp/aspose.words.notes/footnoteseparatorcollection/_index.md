---
title: Aspose::Words::Notes::FootnoteSeparatorCollection class
linktitle: FootnoteSeparatorCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Notes::FootnoteSeparatorCollection class. Provides typed access to FootnoteSeparator nodes of a document in C++.'
type: docs
weight: 3667
url: /cpp/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class


Provides typed access to [FootnoteSeparator](../footnoteseparator/) nodes of a document.

```cpp
class FootnoteSeparatorCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator>>
```

## Methods

| Method | Description |
| --- | --- |
| [FootnoteSeparatorCollection](./footnoteseparatorcollection/)() |  |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::Notes::FootnoteSeparatorType) | Retrieves a [FootnoteSeparator](../footnoteseparator/) of the specified type. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Examples



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
