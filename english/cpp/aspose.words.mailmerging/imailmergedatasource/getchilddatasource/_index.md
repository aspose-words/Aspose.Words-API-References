---
title: Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource method
linktitle: GetChildDataSource
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource method. The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a nested mail merge region in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource::GetChildDataSource method


The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a nested mail merge region.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource(System::String tableName)=0
```


| Parameter | Type | Description |
| --- | --- | --- |
| tableName | System::String | The name of the mail merge region as specified in the template document. Case-insensitive. |

### ReturnValue

A data source object that will provide access to the data records of the specified table.
## Remarks


When the Aspose.Words mail merge engines populates a mail merge region with data and encounters the beginning of a nested mail merge region in the form of MERGEFIELD TableStart:TableName, it invokes [GetChildDataSource()](./) on the current data source object. Your implementation needs to return a new data source object that will provide access to the child records of the current parent record. Aspose.Words will use the returned data source to populate the nested mail merge region.

Below are the rules that the implementation of [GetChildDataSource()](./) must follow.

If the table that is represented by this data source object has a related child (detail) table with the specified name, then your implementation needs to return a new [IMailMergeDataSource](../) object that will provide access to the child records of the current record. An example of this is Orders / OrderDetails relationship. Let's assume that the current [IMailMergeDataSource](../) object represents the Orders table and it has a current order record. Next, Aspose.Words encounters "MERGEFIELD TableStart:OrderDetails" in the document and invokes [GetChildDataSource()](./). You need to create and return a [IMailMergeDataSource](../) object that will allow Aspose.Words to access the OrderDetails record for the current order.

If this data source object does not have a relation to the table with the specified name, then you need to return a [IMailMergeDataSource](../) object that will provide access to all records of the specified table.

If a table with the specified name does not exist, your implementation should return **null**.

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

* Interface [IMailMergeDataSource](../)
* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
