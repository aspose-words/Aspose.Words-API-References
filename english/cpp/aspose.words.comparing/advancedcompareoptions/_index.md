---
title: Aspose::Words::Comparing::AdvancedCompareOptions class
linktitle: AdvancedCompareOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comparing::AdvancedCompareOptions class. Allows to set advanced compare options in C++.'
type: docs
weight: 500
url: /cpp/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class


Allows to set advanced compare options.

```cpp
class AdvancedCompareOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [AdvancedCompareOptions](./advancedcompareoptions/)() |  |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() const | Specifies whether to ignore difference in DrawingML unique Id. |
| [get_IgnoreStoreItemId](./get_ignorestoreitemid/)() const | Specifies whether to ignore difference in StructuredDocumentTag store item Id. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | Setter for [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/). |
| [set_IgnoreStoreItemId](./set_ignorestoreitemid/)(bool) | Setter for [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId](./get_ignorestoreitemid/). |
| static [Type](./type/)() |  |

## Examples



Shows how to compare SDT with same content but different store item id. 
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// Configure options to compare SDT with same content but different store item id.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## See Also

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
