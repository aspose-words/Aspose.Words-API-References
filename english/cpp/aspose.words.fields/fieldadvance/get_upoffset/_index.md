---
title: Aspose::Words::Fields::FieldAdvance::get_UpOffset method
linktitle: get_UpOffset
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldAdvance::get_UpOffset method. Gets or sets the number of points by which the text that follows the field should be moved up in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.fields/fieldadvance/get_upoffset/
---
## FieldAdvance::get_UpOffset method


Gets or sets the number of points by which the text that follows the field should be moved up.

```cpp
System::String Aspose::Words::Fields::FieldAdvance::get_UpOffset()
```


## Examples



Shows how to insert an ADVANCE field, and edit its properties. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// Below are two ways of using the ADVANCE field to adjust the position of text that follows it.
// The effects of an ADVANCE field continue to be applied until the paragraph ends,
// or another ADVANCE field updates the offset/coordinate values.
// 1 -  Specify a directional offset:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_RightOffset(u"5");
field->set_UpOffset(u"5");

ASSERT_EQ(u" ADVANCE  \\r 5 \\u 5", field->GetFieldCode());

builder->Write(u"This text will be moved up and to the right.");

field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_DownOffset(u"5");
field->set_LeftOffset(u"100");

ASSERT_EQ(u" ADVANCE  \\d 5 \\l 100", field->GetFieldCode());

builder->Writeln(u"This text is moved down and to the left, overlapping the previous text.");

// 2 -  Move text to a position specified by coordinates:
field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(get_ArtifactsDir() + u"Field.ADVANCE.docx");
```

## See Also

* Class [FieldAdvance](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
