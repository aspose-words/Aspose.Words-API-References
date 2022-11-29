---
title: get_DisplayText
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the text to appear as the "button" that is selected to run the macro or command.
type: docs
weight: 1
url: /cpp/aspose.words.fields/fieldmacrobutton/get_displaytext/
---
## FieldMacroButton::get_DisplayText method


Gets or sets the text to appear as the "button" that is selected to run the macro or command.

```cpp
System::String Aspose::Words::Fields::FieldMacroButton::get_DisplayText()
```


## Examples



Shows how to use MACROBUTTON fields to allow us to run a document's macros by clicking. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Macro.docm");
auto builder = MakeObject<DocumentBuilder>(doc);

ASSERT_TRUE(doc->get_HasMacros());

// Insert a MACROBUTTON field, and reference one of the document's macros by name in the MacroName property.
auto field = System::DynamicCast<FieldMacroButton>(builder->InsertField(FieldType::FieldMacroButton, true));
field->set_MacroName(u"MyMacro");
field->set_DisplayText(String(u"Double click to run macro: ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field->GetFieldCode());

// Use the property to reference "ViewZoom200", a macro that ships with Microsoft Word.
// We can find all other macros via View -> Macros (dropdown) -> View Macros.
// In that menu, select "Word Commands" from the "Macros in:" drop down.
// If our document contains a custom macro with the same name as a stock macro,
// our macro will be the one that the MACROBUTTON field runs.
builder->InsertParagraph();
field = System::DynamicCast<FieldMacroButton>(builder->InsertField(FieldType::FieldMacroButton, true));
field->set_MacroName(u"ViewZoom200");
field->set_DisplayText(String(u"Run ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  ViewZoom200 Run ViewZoom200", field->GetFieldCode());

// Save the document as a macro-enabled document type.
doc->Save(ArtifactsDir + u"Field.MACROBUTTON.docm");
```

## See Also

* Class [FieldMacroButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
