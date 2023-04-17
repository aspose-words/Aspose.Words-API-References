---
title: Aspose::Words::MailMerging::MailMerge::Execute method
linktitle: Execute
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::MailMerge::Execute method. Performs a mail merge operation for a single record in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.mailmerging/mailmerge/execute/
---
## MailMerge::Execute(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) method


Performs a mail merge operation for a single record.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::ArrayPtr<System::String> &fieldNames, const System::ArrayPtr<System::SharedPtr<System::Object>> &values)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldNames | const System::ArrayPtr\<System::String\>\& | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| values | const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\& | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in *fieldNames*. |
## Remarks


Use this method to fill mail merge fields in the document with values from an array of objects.

This method merges data for one record only. The array of field names and the array of values represent the data of a single record.

This method does not use mail merge regions.

This method ignores the [RemoveUnusedRegions](../../mailmergecleanupoptions/) option.

## See Also

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::Execute(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Performs a mail merge from a custom data source.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Parameter | Type | Description |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | An object that implements the custom mail merge data source interface. |
## Remarks


Use this method to fill mail merge fields in the document with values from any data source such as a list or hashtable or objects. You need to write your own class that implements the [IMailMergeDataSource](../../imailmergedatasource/) interface.

You can use this method only when [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) is **false**, that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

This method ignores the [RemoveUnusedRegions](../../mailmergecleanupoptions/) option.

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

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
