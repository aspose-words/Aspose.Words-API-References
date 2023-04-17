---
title: Aspose::Words::Range::get_FormFields method
linktitle: get_FormFields
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Range::get_FormFields method. Returns a FormFields collection that represents all form fields in the range in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/range/get_formfields/
---
## Range::get_FormFields method


Returns a [FormFields](./) collection that represents all form fields in the range.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormFieldCollection> Aspose::Words::Range::get_FormFields()
```


## Examples



Shows how insert different kinds of form fields into a document, and process them with using a document visitor implementation. 
```cpp
void Visitor()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    // Use a document builder to insert a combo box.
    builder->Write(u"Choose a value from this combo box: ");
    SharedPtr<FormField> comboBox = builder->InsertComboBox(u"MyComboBox", MakeArray<String>({u"One", u"Two", u"Three"}), 0);
    comboBox->set_CalculateOnExit(true);
    ASSERT_EQ(3, comboBox->get_DropDownItems()->get_Count());
    ASSERT_EQ(0, comboBox->get_DropDownSelectedIndex());
    ASSERT_TRUE(comboBox->get_Enabled());

    builder->InsertBreak(BreakType::ParagraphBreak);

    // Use a document builder to insert a check box.
    builder->Write(u"Click this check box to tick/untick it: ");
    SharedPtr<FormField> checkBox = builder->InsertCheckBox(u"MyCheckBox", false, 50);
    checkBox->set_IsCheckBoxExactSize(true);
    checkBox->set_HelpText(u"Right click to check this box");
    checkBox->set_OwnHelp(true);
    checkBox->set_StatusText(u"Checkbox status text");
    checkBox->set_OwnStatus(true);
    ASPOSE_ASSERT_EQ(50.0, checkBox->get_CheckBoxSize());
    ASSERT_FALSE(checkBox->get_Checked());
    ASSERT_FALSE(checkBox->get_Default());

    builder->InsertBreak(BreakType::ParagraphBreak);

    // Use a document builder to insert text input form field.
    builder->Write(u"Enter text here: ");
    SharedPtr<FormField> textInput = builder->InsertTextInput(u"MyTextInput", TextFormFieldType::Regular, u"", u"Placeholder text", 50);
    textInput->set_EntryMacro(u"EntryMacro");
    textInput->set_ExitMacro(u"ExitMacro");
    textInput->set_TextInputDefault(u"Regular");
    textInput->set_TextInputFormat(u"FIRST CAPITAL");
    textInput->SetTextInputValue(System::ObjectExt::Box<String>(u"New placeholder text"));
    ASSERT_EQ(TextFormFieldType::Regular, textInput->get_TextInputType());
    ASSERT_EQ(50, textInput->get_MaxLength());

    // This collection contains all our form fields.
    SharedPtr<FormFieldCollection> formFields = doc->get_Range()->get_FormFields();
    ASSERT_EQ(3, formFields->get_Count());

    // Fields display our form fields. We can see their field codes by opening this document
    // in Microsoft and pressing Alt + F9. These fields have no switches,
    // and members of the FormField object fully govern their form fields' content.
    ASSERT_EQ(3, doc->get_Range()->get_Fields()->get_Count());
    ASSERT_EQ(u" FORMDROPDOWN \u0001", doc->get_Range()->get_Fields()->idx_get(0)->GetFieldCode());
    ASSERT_EQ(u" FORMCHECKBOX \u0001", doc->get_Range()->get_Fields()->idx_get(1)->GetFieldCode());
    ASSERT_EQ(u" FORMTEXT \u0001", doc->get_Range()->get_Fields()->idx_get(2)->GetFieldCode());

    // Allow each form field to accept a document visitor.
    auto formFieldVisitor = MakeObject<ExFormFields::FormFieldVisitor>();

    {
        SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<FormField>>> fieldEnumerator = formFields->GetEnumerator();
        while (fieldEnumerator->MoveNext())
        {
            fieldEnumerator->get_Current()->Accept(formFieldVisitor);
        }
    }

    std::cout << formFieldVisitor->GetText() << std::endl;

    doc->UpdateFields();
    doc->Save(ArtifactsDir + u"FormFields.Visitor.html");
}

class FormFieldVisitor : public DocumentVisitor
{
public:
    FormFieldVisitor()
    {
        mBuilder = MakeObject<System::Text::StringBuilder>();
    }

    VisitorAction VisitFormField(SharedPtr<FormField> formField) override
    {
        AppendLine(System::ObjectExt::ToString(formField->get_Type()) + u": \"" + formField->get_Name() + u"\"");
        AppendLine(String(u"\tStatus: ") + (formField->get_Enabled() ? String(u"Enabled") : String(u"Disabled")));
        AppendLine(String(u"\tHelp Text:  ") + formField->get_HelpText());
        AppendLine(String(u"\tEntry macro name: ") + formField->get_EntryMacro());
        AppendLine(String(u"\tExit macro name: ") + formField->get_ExitMacro());

        switch (formField->get_Type())
        {
        case FieldType::FieldFormDropDown:
            AppendLine(String(u"\tDrop-down items count: ") + formField->get_DropDownItems()->get_Count() + u", default selected item index: " +
                       formField->get_DropDownSelectedIndex());
            AppendLine(String(u"\tDrop-down items: ") + String::Join(u", ", formField->get_DropDownItems()->LINQ_ToArray()));
            break;

        case FieldType::FieldFormCheckBox:
            AppendLine(String(u"\tCheckbox size: ") + formField->get_CheckBoxSize());
            AppendLine(String(u"\t") + u"Checkbox is currently: " + (formField->get_Checked() ? String(u"checked, ") : String(u"unchecked, ")) +
                       u"by default: " + (formField->get_Default() ? String(u"checked") : String(u"unchecked")));
            break;

        case FieldType::FieldFormTextInput:
            AppendLine(String(u"\tInput format: ") + formField->get_TextInputFormat());
            AppendLine(String(u"\tCurrent contents: ") + formField->get_Result());
            break;

        default:
            break;
        }

        // Let the visitor continue visiting other nodes.
        return VisitorAction::Continue;
    }

    String GetText()
    {
        return mBuilder->ToString();
    }

private:
    SharedPtr<System::Text::StringBuilder> mBuilder;

    void AppendLine(String text)
    {
        mBuilder->Append(text + u'\n');
    }
};
```

## See Also

* Class [FormFieldCollection](../../../aspose.words.fields/formfieldcollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
