---
title: IMailMergeDataSource
second_title: Aspose.Words for C++ API Reference
description: Implement this interface to allow mail merge from a custom data source, such as a list of objects. Master-detail data is also supported.
type: docs
weight: 105
url: /cpp/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface


Implement this interface to allow mail merge from a custom data source, such as a list of objects. Master-detail data is also supported.

```cpp
class IMailMergeDataSource : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [get_TableName](./get_tablename/)() | Returns the name of the data source. |
| virtual [GetChildDataSource](./getchilddatasource/)(System::String) | The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a nested mail merge region. |
| virtual [GetValue](./getvalue/)(System::String, System::SharedPtr\<System::Object\>\&) |  |
| virtual [MoveNext](./movenext/)() | Advances to the next record in the data source. |
## Remarks


When a data source is created, it should be initialized to point to BOF (before the first record). The Aspose.Words mail merge engine will invoke [MoveNext](./movenext/) to advance to next record and then invoke [GetValue()](./getvalue/) for every merge field it encounters in the document or the current mail merge region.

## Examples



Shows how to execute a mail merge with a data source in the form of a custom object. 
```cpp
void CustomDataSource()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);
    builder->InsertField(u" MERGEFIELD FullName ");
    builder->InsertParagraph();
    builder->InsertField(u" MERGEFIELD Address ");

    SharedPtr<System::Collections::Generic::List<SharedPtr<ExMailMergeCustom::Customer>>> customers =
        MakeObject<System::Collections::Generic::List<SharedPtr<ExMailMergeCustom::Customer>>>();
    customers->Add(MakeObject<ExMailMergeCustom::Customer>(u"Thomas Hardy", u"120 Hanover Sq., London"));
    customers->Add(MakeObject<ExMailMergeCustom::Customer>(u"Paolo Accorti", u"Via Monte Bianco 34, Torino"));

    // To use a custom object as a data source, it must implement the IMailMergeDataSource interface.
    auto dataSource = MakeObject<ExMailMergeCustom::CustomerMailMergeDataSource>(customers);

    doc->get_MailMerge()->Execute(dataSource);

    doc->Save(ArtifactsDir + u"MailMergeCustom.CustomDataSource.docx");
}

class Customer : public System::Object
{
public:
    String get_FullName()
    {
        return pr_FullName;
    }

    void set_FullName(String value)
    {
        pr_FullName = value;
    }

    String get_Address()
    {
        return pr_Address;
    }

    void set_Address(String value)
    {
        pr_Address = value;
    }

    Customer(String aFullName, String anAddress)
    {
        set_FullName(aFullName);
        set_Address(anAddress);
    }

private:
    String pr_FullName;
    String pr_Address;
};

class CustomerMailMergeDataSource : public IMailMergeDataSource
{
public:
    String get_TableName() override
    {
        return u"Customer";
    }

    CustomerMailMergeDataSource(SharedPtr<System::Collections::Generic::List<SharedPtr<ExMailMergeCustom::Customer>>> customers) : mRecordIndex(0)
    {
        mCustomers = customers;

        // When we initialize the data source, its position must be before the first record.
        mRecordIndex = -1;
    }

    bool GetValue(String fieldName, SharedPtr<System::Object>& fieldValue) override
    {
        if (fieldName == u"FullName")
        {
            fieldValue = System::ObjectExt::Box<String>(mCustomers->idx_get(mRecordIndex)->get_FullName());
            return true;
        }
        else if (fieldName == u"Address")
        {
            fieldValue = System::ObjectExt::Box<String>(mCustomers->idx_get(mRecordIndex)->get_Address());
            return true;
        }
        else
        {
            fieldValue.reset();
            return false;
        }
    }

    bool MoveNext() override
    {
        if (!get_IsEof())
        {
            mRecordIndex++;
        }

        return !get_IsEof();
    }

    SharedPtr<IMailMergeDataSource> GetChildDataSource(String tableName) override
    {
        return nullptr;
    }

private:
    bool get_IsEof()
    {
        return mRecordIndex >= mCustomers->get_Count();
    }

    SharedPtr<System::Collections::Generic::List<SharedPtr<ExMailMergeCustom::Customer>>> mCustomers;
    int mRecordIndex;
};
```

## See Also

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words](../../)
