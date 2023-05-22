---
title: Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource method
linktitle: GetDataSource
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource method. The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a top-level mail merge region in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot::GetDataSource method


The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a top-level mail merge region.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource(System::String tableName)=0
```


| Parameter | Type | Description |
| --- | --- | --- |
| tableName | System::String | The name of the mail merge region as specified in the template document. Case-insensitive. |

### ReturnValue

A data source object that will provide access to the data records of the specified table.
## Remarks


When the Aspose.Words mail merge engines populates a document with data and encounters MERGEFIELD TableStart:TableName, it invokes [GetDataSource()](./) on this object. Your implementation needs to return a new data source object. Aspose.Words will use the returned data source to populate the mail merge region.

If a data source (table) with the specified name does not exist, your implementation should return **null**.

## Examples



Performs mail merge from a custom data source with master-detail data. 
```cpp
void CustomDataSourceRoot()
{
    // Create a document with two mail merge regions named "Washington" and "Seattle".
    ArrayPtr<String> mailMergeRegions = MakeArray<String>({u"Vancouver", u"Seattle"});
    SharedPtr<Document> doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Create two data sources for the mail merge.
    SharedPtr<System::Collections::Generic::List<SharedPtr<ExMailMergeCustom::Employee>>> employeesWashingtonBranch =
        MakeObject<System::Collections::Generic::List<SharedPtr<ExMailMergeCustom::Employee>>>();
    employeesWashingtonBranch->Add(MakeObject<ExMailMergeCustom::Employee>(u"John Doe", u"Sales"));
    employeesWashingtonBranch->Add(MakeObject<ExMailMergeCustom::Employee>(u"Jane Doe", u"Management"));

    SharedPtr<System::Collections::Generic::List<SharedPtr<ExMailMergeCustom::Employee>>> employeesSeattleBranch =
        MakeObject<System::Collections::Generic::List<SharedPtr<ExMailMergeCustom::Employee>>>();
    employeesSeattleBranch->Add(MakeObject<ExMailMergeCustom::Employee>(u"John Cardholder", u"Management"));
    employeesSeattleBranch->Add(MakeObject<ExMailMergeCustom::Employee>(u"Joe Bloggs", u"Sales"));

    // Register our data sources by name in a data source root.
    //  If we are about to use this data source root in a mail merge with regions,
    // each source's registered name must match the name of an existing mail merge region in the mail merge source document.
    auto sourceRoot = MakeObject<ExMailMergeCustom::DataSourceRoot>();
    sourceRoot->RegisterSource(mailMergeRegions[0], MakeObject<ExMailMergeCustom::EmployeeListMailMergeSource>(employeesWashingtonBranch));
    sourceRoot->RegisterSource(mailMergeRegions[1], MakeObject<ExMailMergeCustom::EmployeeListMailMergeSource>(employeesSeattleBranch));

    // Since we have consecutive mail merge regions, we would normally have to perform two mail merges.
    // However, one mail merge source with a data root can fill in multiple regions
    // if the root contains tables with corresponding names/column names.
    doc->get_MailMerge()->ExecuteWithRegions(sourceRoot);

    doc->Save(ArtifactsDir + u"MailMergeCustom.CustomDataSourceRoot.docx");
}

static SharedPtr<Document> CreateSourceDocumentWithMailMergeRegions(ArrayPtr<String> regions)
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    for (String s : regions)
    {
        builder->Writeln(String(u"\n") + s + u" branch: ");
        builder->InsertField(String(u" MERGEFIELD TableStart:") + s);
        builder->InsertField(u" MERGEFIELD FullName");
        builder->Write(u", ");
        builder->InsertField(u" MERGEFIELD Department");
        builder->InsertField(String(u" MERGEFIELD TableEnd:") + s);
    }

    return doc;
}

class Employee : public System::Object
{
public:
    String get_FullName()
    {
        return pr_FullName;
    }

    String get_Department()
    {
        return pr_Department;
    }

    Employee(String aFullName, String aDepartment)
    {
        pr_FullName = aFullName;
        pr_Department = aDepartment;
    }

private:
    String pr_FullName;
    String pr_Department;
};

class DataSourceRoot : public IMailMergeDataSourceRoot
{
public:
    SharedPtr<IMailMergeDataSource> GetDataSource(String tableName) override
    {
        SharedPtr<ExMailMergeCustom::EmployeeListMailMergeSource> source = mSources->idx_get(tableName);
        source->Reset();
        return mSources->idx_get(tableName);
    }

    void RegisterSource(String sourceName, SharedPtr<ExMailMergeCustom::EmployeeListMailMergeSource> source)
    {
        mSources->Add(sourceName, source);
    }

    DataSourceRoot() : mSources(MakeObject<System::Collections::Generic::Dictionary<String, SharedPtr<ExMailMergeCustom::EmployeeListMailMergeSource>>>())
    {
    }

private:
    SharedPtr<System::Collections::Generic::Dictionary<String, SharedPtr<ExMailMergeCustom::EmployeeListMailMergeSource>>> mSources;
};

class EmployeeListMailMergeSource : public IMailMergeDataSource
{
public:
    String get_TableName() override
    {
        return u"Employees";
    }

    EmployeeListMailMergeSource(SharedPtr<System::Collections::Generic::List<SharedPtr<ExMailMergeCustom::Employee>>> employees) : mRecordIndex(0)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    bool MoveNext() override
    {
        if (!get_IsEof())
        {
            mRecordIndex++;
        }

        return !get_IsEof();
    }

    void Reset()
    {
        mRecordIndex = -1;
    }

    bool GetValue(String fieldName, SharedPtr<System::Object>& fieldValue) override
    {
        if (fieldName == u"FullName")
        {
            fieldValue = System::ObjectExt::Box<String>(mEmployees->idx_get(mRecordIndex)->get_FullName());
            return true;
        }
        else if (fieldName == u"Department")
        {
            fieldValue = System::ObjectExt::Box<String>(mEmployees->idx_get(mRecordIndex)->get_Department());
            return true;
        }
        else
        {
            fieldValue.reset();
            return false;
        }
    }

    SharedPtr<IMailMergeDataSource> GetChildDataSource(String tableName) override
    {
        throw System::NotImplementedException();
    }

private:
    bool get_IsEof()
    {
        return mRecordIndex >= mEmployees->get_Count();
    }

    SharedPtr<System::Collections::Generic::List<SharedPtr<ExMailMergeCustom::Employee>>> mEmployees;
    int mRecordIndex;
};
```

## See Also

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Interface [IMailMergeDataSourceRoot](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
