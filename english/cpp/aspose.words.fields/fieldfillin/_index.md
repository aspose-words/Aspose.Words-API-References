---
title: FieldFillIn
second_title: Aspose.Words for C++ API Reference
description: Implements the FILLIN field. To learn more, visit the  documentation article.
type: docs
weight: 547
url: /cpp/aspose.words.fields/fieldfillin/
---
## FieldFillIn class


Implements the FILLIN field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldFillIn : public Aspose::Words::Fields::Field,
                    public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_DefaultResponse](./get_defaultresponse/)() | Gets or sets default user response (initial value contained in the prompt window). |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_PromptOnceOnMailMerge](./get_promptonceonmailmerge/)() | Gets or sets whether the user response should be recieved once per a mail merge operation. |
| [get_PromptText](./get_prompttext/)() | Gets or sets the prompt text (the title of the prompt window). |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_DefaultResponse](./set_defaultresponse/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldFillIn::get_DefaultResponse](./get_defaultresponse/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PromptOnceOnMailMerge](./set_promptonceonmailmerge/)(bool) | Setter for [Aspose::Words::Fields::FieldFillIn::get_PromptOnceOnMailMerge](./get_promptonceonmailmerge/). |
| [set_PromptText](./set_prompttext/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldFillIn::get_PromptText](./get_prompttext/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples



Shows how to use the FILLIN field to prompt the user for a response. 
```cpp
void FieldFillIn_()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    // Insert a FILLIN field. When we manually update this field in Microsoft Word,
    // it will prompt us to enter a response. The field will then display the response as text.
    auto field = System::DynamicCast<FieldFillIn>(builder->InsertField(FieldType::FieldFillIn, true));
    field->set_PromptText(u"Please enter a response:");
    field->set_DefaultResponse(u"A default response.");

    // We can also use these fields to ask the user for a unique response for each page
    // created during a mail merge done using Microsoft Word.
    field->set_PromptOnceOnMailMerge(true);

    ASSERT_EQ(u" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field->GetFieldCode());

    auto mergeField = System::DynamicCast<FieldMergeField>(builder->InsertField(FieldType::FieldMergeField, true));
    mergeField->set_FieldName(u"MergeField");

    // If we perform a mail merge programmatically, we can use a custom prompt respondent
    // to automatically edit responses for FILLIN fields that the mail merge encounters.
    doc->get_FieldOptions()->set_UserPromptRespondent(MakeObject<ExField::PromptRespondent>());
    doc->get_MailMerge()->Execute(MakeArray<String>({u"MergeField"}), MakeArray<SharedPtr<System::Object>>({System::ObjectExt::Box<String>(u"")}));

    doc->UpdateFields();
    doc->Save(ArtifactsDir + u"Field.FILLIN.docx");
}

class PromptRespondent : public IFieldUserPromptRespondent
{
public:
    String Respond(String promptText, String defaultResponse) override
    {
        return String(u"Response modified by PromptRespondent. ") + defaultResponse;
    }
};
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words](../../)
