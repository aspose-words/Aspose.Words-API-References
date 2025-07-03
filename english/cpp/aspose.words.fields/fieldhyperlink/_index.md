---
title: Aspose::Words::Fields::FieldHyperlink class
linktitle: FieldHyperlink
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldHyperlink class. Implements the HYPERLINK field To learn more, visit the  documentation article in C++.'
type: docs
weight: 53000
url: /cpp/aspose.words.fields/fieldhyperlink/
---
## FieldHyperlink class


Implements the HYPERLINK field To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldHyperlink : public Aspose::Words::Fields::Field,
                       public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                       public Aspose::Words::Fields::IFieldResultFormatProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_Address](./get_address/)() | Gets or sets a location where this hyperlink jumps. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsImageMap](./get_isimagemap/)() | Gets or sets whether to append coordinates to the hyperlink for a server-side image map. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_OpenInNewWindow](./get_openinnewwindow/)() | Gets or sets whether to open the destination site in a new web browser window. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_ScreenTip](./get_screentip/)() | Gets or sets the ScreenTip text for the hyperlink. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_SubAddress](./get_subaddress/)() | Gets or sets a location in the file, such as a bookmark, where this hyperlink jumps. |
| [get_Target](./get_target/)() | Gets or sets the target to which the link should be redirected. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_Address](./set_address/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldHyperlink::get_Address](./get_address/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsImageMap](./set_isimagemap/)(bool) | Setter for [Aspose::Words::Fields::FieldHyperlink::get_IsImageMap](./get_isimagemap/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_OpenInNewWindow](./set_openinnewwindow/)(bool) | Setter for [Aspose::Words::Fields::FieldHyperlink::get_OpenInNewWindow](./get_openinnewwindow/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScreenTip](./set_screentip/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldHyperlink::get_ScreenTip](./get_screentip/). |
| [set_SubAddress](./set_subaddress/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldHyperlink::get_SubAddress](./get_subaddress/). |
| [set_Target](./set_target/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldHyperlink::get_Target](./get_target/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples



Shows how to use HYPERLINK fields to link to documents in the local file system. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));

// When we click this HYPERLINK field in Microsoft Word,
// it will open the linked document and then place the cursor at the specified bookmark.
field->set_Address(get_MyDir() + u"Bookmarks.docx");
field->set_SubAddress(u"MyBookmark3");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address() + u" on bookmark " + field->get_SubAddress() + u" in a new window");

builder->Writeln();

// When we click this HYPERLINK field in Microsoft Word,
// it will open the linked document, and automatically scroll down to the specified iframe.
field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));
field->set_Address(get_MyDir() + u"Iframes.html");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address());
field->set_Target(u"iframe_3");
field->set_OpenInNewWindow(true);
field->set_IsImageMap(false);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.HYPERLINK.docx");
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
