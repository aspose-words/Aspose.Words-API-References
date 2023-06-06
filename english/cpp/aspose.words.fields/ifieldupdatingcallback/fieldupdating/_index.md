---
title: Aspose::Words::Fields::IFieldUpdatingCallback::FieldUpdating method
linktitle: FieldUpdating
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::IFieldUpdatingCallback::FieldUpdating method. A user defined method that is called just before a field is updated in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.fields/ifieldupdatingcallback/fieldupdating/
---
## IFieldUpdatingCallback::FieldUpdating method


A user defined method that is called just before a field is updated.

```cpp
virtual void Aspose::Words::Fields::IFieldUpdatingCallback::FieldUpdating(System::SharedPtr<Aspose::Words::Fields::Field> field)=0
```


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
            auto fieldAuthor = System::ExplicitCast<FieldAuthor>(field);
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

* Class [Field](../../field/)
* Interface [IFieldUpdatingCallback](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
