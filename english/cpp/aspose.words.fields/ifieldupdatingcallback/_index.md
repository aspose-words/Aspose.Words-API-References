---
title: Aspose::Words::Fields::IFieldUpdatingCallback interface
linktitle: IFieldUpdatingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::IFieldUpdatingCallback interface. Implement this interface if you want to have your own custom methods called during a field update in C++.'
type: docs
weight: 123000
url: /cpp/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface


Implement this interface if you want to have your own custom methods called during a field update.

```cpp
class IFieldUpdatingCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [FieldUpdated](./fieldupdated/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | A user defined method that is called just after a field is updated. |
| virtual [FieldUpdating](./fieldupdating/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | A user defined method that is called just before a field is updated. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Examples



Shows how to use callback methods during a field update. 
```cpp
void FieldUpdatingCallbackTest()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    builder->InsertField(u" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder->InsertField(u" TIME ");
    builder->InsertField(u" REVNUM ");
    builder->InsertField(u" AUTHOR  \"John Doe\" ");
    builder->InsertField(u" SUBJECT \"My Subject\" ");
    builder->InsertField(u" QUOTE \"Hello world!\" ");

    auto callback = MakeObject<ExField::FieldUpdatingCallback>();
    doc->get_FieldOptions()->set_FieldUpdatingCallback(callback);

    doc->UpdateFields();

    ASSERT_TRUE(callback->get_FieldUpdatedCalls()->Contains(u"Updating John Doe"));
}

class FieldUpdatingCallback : public IFieldUpdatingCallback
{
public:
    SharedPtr<System::Collections::Generic::IList<String>> get_FieldUpdatedCalls()
    {
        return pr_FieldUpdatedCalls;
    }

    FieldUpdatingCallback()
    {
        pr_FieldUpdatedCalls = MakeObject<System::Collections::Generic::List<String>>();
    }

private:
    SharedPtr<System::Collections::Generic::IList<String>> pr_FieldUpdatedCalls;

    void FieldUpdating(SharedPtr<Field> field) override
    {
        if (field->get_Type() == FieldType::FieldAuthor)
        {
            auto fieldAuthor = System::DynamicCast<FieldAuthor>(field);
            fieldAuthor->set_AuthorName(u"Updating John Doe");
        }
    }

    void FieldUpdated(SharedPtr<Field> field) override
    {
        get_FieldUpdatedCalls()->Add(field->get_Result());
    }
};
```

## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
