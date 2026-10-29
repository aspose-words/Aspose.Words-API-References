---
title: Aspose::Words::Fields::FieldHyperlink class
linktitle: FieldHyperlink
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldHyperlink class. Implements the HYPERLINK field To learn more, visit the Working with Fields documentation article in C++.'
type: docs
weight: 53000
url: /cpp/aspose.words.fields/fieldhyperlink/
---
## FieldHyperlink class


Implements the HYPERLINK field 
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldHyperlink : public Field,
                       public IFieldCodeTokenInfoProvider,
                       public IFieldResultFormatProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_Address](./get_address/)() | Gets or sets a location where this hyperlink jumps. |
| [get_IsImageMap](./get_isimagemap/)() | Gets or sets whether to append coordinates to the hyperlink for a server-side image map. |
| [get_OpenInNewWindow](./get_openinnewwindow/)() | Gets or sets whether to open the destination site in a new web browser window. |
| [get_ScreenTip](./get_screentip/)() | Gets or sets the ScreenTip text for the hyperlink. |
| [get_SubAddress](./get_subaddress/)() | Gets or sets a location in the file, such as a bookmark, where this hyperlink jumps. |
| [get_Target](./get_target/)() | Gets or sets the target to which the link should be redirected. |
| [set_Address](./set_address/)(const System::String \&) | Sets a location where this hyperlink jumps. |
| [set_IsImageMap](./set_isimagemap/)(bool) | Sets whether to append coordinates to the hyperlink for a server-side image map. |
| [set_OpenInNewWindow](./set_openinnewwindow/)(bool) | Sets whether to open the destination site in a new web browser window. |
| [set_ScreenTip](./set_screentip/)(const System::String \&) | Sets the ScreenTip text for the hyperlink. |
| [set_SubAddress](./set_subaddress/)(const System::String \&) | Sets a location in the file, such as a bookmark, where this hyperlink jumps. |
| [set_Target](./set_target/)(const System::String \&) | Sets the target to which the link should be redirected. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| virtual [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Sets whether the field is locked (should not recalculate its result). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sets the LCID of the field. |
| [set_Result](../field/set_result/)(const System::String \&) | Sets text that is between the field separator and field end. |
## Remarks

 When selected, causes control to jump to the location such as a bookmark or a URL. 
## Examples


Shows how to use HYPERLINK fields to link to documents in the local file system.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(FieldType::FieldHyperlink, true));

// When we click this HYPERLINK field in Microsoft Word,
// it will open the linked document and then place the cursor at the specified bookmark.
field->set_Address(get_MyDir() + u"Bookmarks.docx");
field->set_SubAddress(u"MyBookmark3");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address() + u" on bookmark " + field->get_SubAddress() + u" in a new window");

builder->Writeln();

// When we click this HYPERLINK field in Microsoft Word,
// it will open the linked document, and automatically scroll down to the specified iframe.
field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(FieldType::FieldHyperlink, true));
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
