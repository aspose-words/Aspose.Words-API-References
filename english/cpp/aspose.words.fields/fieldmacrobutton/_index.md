---
title: FieldMacroButton
second_title: Aspose.Words for C++ API Reference
description: Implements the MACROBUTTON field.
type: docs
weight: 833
url: /cpp/aspose.words.fields/fieldmacrobutton/
---
## FieldMacroButton class


Implements the MACROBUTTON field.

```cpp
class FieldMacroButton : public Aspose::Words::Fields::Field, public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_DisplayText](./get_displaytext/)() | Gets or sets the text to appear as the "button" that is selected to run the macro or command. |
| [get_End](./get_end/)() override | Gets the node that represents the field end. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_MacroName](./get_macroname/)() | Gets or sets the name of the macro or command to run. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](./get_separator/)() override | Gets the node that represents the field separator. Can be null. |
| [get_Start](./get_start/)() override | Gets the node that represents the start of the field. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_DisplayText](./set_displaytext/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldMacroButton::get_DisplayText](./get_displaytext/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_MacroName](./set_macroname/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldMacroButton::get_MacroName](./get_macroname/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

Allows a macro or command to be run.

In Aspose.Words this field can also act as a merge field.

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

