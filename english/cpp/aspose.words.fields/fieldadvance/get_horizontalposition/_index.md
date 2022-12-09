---
title: get_HorizontalPosition
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the number of points by which the text that follows the field should be moved horizontally from the left edge of the column, frame, or text box.
type: docs
weight: 27
url: /cpp/aspose.words.fields/fieldadvance/get_horizontalposition/
---
## FieldAdvance::get_HorizontalPosition method


Gets or sets the number of points by which the text that follows the field should be moved horizontally from the left edge of the column, frame, or text box.

```cpp
System::String Aspose::Words::Fields::FieldAdvance::get_HorizontalPosition()
```


## Examples



Shows how to insert an ADVANCE field, and edit its properties. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// Below are two ways of using the ADVANCE field to adjust the position of text that follows it.
// The effects of an ADVANCE field continue to be applied until the paragraph ends,
// or another ADVANCE field updates the offset/coordinate values.
// 1 -  Specify a directional offset:
auto field = System::DynamicCast<FieldAdvance>(builder->InsertField(FieldType::FieldAdvance, true));
field->set_RightOffset(u"5");
field->set_UpOffset(u"5");

ASSERT_EQ(u" ADVANCE  \\r 5 \\u 5", field->GetFieldCode());

builder->Write(u"This text will be moved up and to the right.");

field = System::DynamicCast<FieldAdvance>(builder->InsertField(FieldType::FieldAdvance, true));
field->set_DownOffset(u"5");
field->set_LeftOffset(u"100");

ASSERT_EQ(u" ADVANCE  \\d 5 \\l 100", field->GetFieldCode());

builder->Writeln(u"This text is moved down and to the left, overlapping the previous text.");

// 2 -  Move text to a position specified by coordinates:
field = System::DynamicCast<FieldAdvance>(builder->InsertField(FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(ArtifactsDir + u"Field.ADVANCE.docx");
```

## See Also

* Class [FieldAdvance](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
