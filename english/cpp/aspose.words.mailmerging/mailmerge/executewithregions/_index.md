---
title: Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions method
linktitle: ExecuteWithRegions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions method. Performs a mail merge from a custom data source with mail merge regions in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.mailmerging/mailmerge/executewithregions/
---
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Performs a mail merge from a custom data source with mail merge regions.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Parameter | Type | Description |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | An object that implements the custom mail merge data source interface. |
## Remarks


Use this method to fill mail merge fields in the document with values from any custom data source such as an XML file or collections of business objects. You need to write your own class that implements the [IMailMergeDataSource](../../imailmergedatasource/) interface.

You can use this method only when [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) is **false**, that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

## Examples



Shows how to use mail merge regions to execute a nested mail merge. 
```cpp
void CustomDataSource()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    // Normally, MERGEFIELDs contain the name of a column of a mail merge data source.
    // Instead, we can use "TableStart:" and "TableEnd:" prefixes to begin/end a mail merge region.
    // Each region will belong to a table with a name that matches the string immediately after the prefix's colon.
    builder->InsertField(u" MERGEFIELD TableStart:Customers");

    // These MERGEFIELDs are inside the mail merge region of the "Customers" table.
    // When we execute the mail merge, this field will receive data from rows in a data source named "Customers".
    builder->Write(u"Full name:\t");
    builder->InsertField(u" MERGEFIELD FullName ");
    builder->Write(u"\nAddress:\t");
    builder->InsertField(u" MERGEFIELD Address ");
    builder->Write(u"\nOrders:\n");

    // Create a second mail merge region inside the outer region for a data source named "Orders".
    // The "Orders" data entries have a many-to-one relationship with the "Customers" data source.
    builder->InsertField(u" MERGEFIELD TableStart:Orders");

    builder->Write(u"\tItem name:\t");
    builder->InsertField(u" MERGEFIELD Name ");
    builder->Write(u"\n\tQuantity:\t");
    builder->InsertField(u" MERGEFIELD Quantity ");
    builder->InsertParagraph();

    builder->InsertField(u" MERGEFIELD TableEnd:Orders");
    builder->InsertField(u" MERGEFIELD TableEnd:Customers");

    // Create related data with names that match those of our mail merge regions.
    SharedPtr<System::Collections::Generic::List<SharedPtr<ExMailMergeCustomNested::Customer>>> customers =
        MakeObject<System::Collections::Generic::List<SharedPtr<ExMailMergeCustomNested::Customer>>>();
    customers->Add(MakeObject<ExMailMergeCustomNested::Customer>(u"Thomas Hardy", u"120 Hanover Sq., London"));
    customers->Add(MakeObject<ExMailMergeCustomNested::Customer>(u"Paolo Accorti", u"Via Monte Bianco 34, Torino"));

    customers->idx_get(0)->get_Orders()->Add(MakeObject<ExMailMergeCustomNested::Order>(u"Rugby World Cup Cap", 2));
    customers->idx_get(0)->get_Orders()->Add(MakeObject<ExMailMergeCustomNested::Order>(u"Rugby World Cup Ball", 1));
    customers->idx_get(1)->get_Orders()->Add(MakeObject<ExMailMergeCustomNested::Order>(u"Rugby World Cup Guide", 1));

    // To mail merge from your data source, we must wrap it into an object that implements the IMailMergeDataSource interface.
    auto customersDataSource = MakeObject<ExMailMergeCustomNested::CustomerMailMergeDataSource>(customers);

    doc->get_MailMerge()->ExecuteWithRegions(customersDataSource);

    doc->Save(ArtifactsDir + u"NestedMailMergeCustom.CustomDataSource.docx");
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

    SharedPtr<System::Collections::Generic::List<SharedPtr<ExMailMergeCustomNested::Order>>> get_Orders()
    {
        return pr_Orders;
    }

    void set_Orders(SharedPtr<System::Collections::Generic::List<SharedPtr<ExMailMergeCustomNested::Order>>> value)
    {
        pr_Orders = value;
    }

    Customer(String aFullName, String anAddress)
    {
        set_FullName(aFullName);
        set_Address(anAddress);
        set_Orders(MakeObject<System::Collections::Generic::List<SharedPtr<ExMailMergeCustomNested::Order>>>());
    }

private:
    String pr_FullName;
    String pr_Address;
    SharedPtr<System::Collections::Generic::List<SharedPtr<ExMailMergeCustomNested::Order>>> pr_Orders;
};

class Order : public System::Object
{
public:
    String get_Name()
    {
        return pr_Name;
    }

    void set_Name(String value)
    {
        pr_Name = value;
    }

    int get_Quantity()
    {
        return pr_Quantity;
    }

    void set_Quantity(int value)
    {
        pr_Quantity = value;
    }

    Order(String oName, int oQuantity) : pr_Quantity(0)
    {
        set_Name(oName);
        set_Quantity(oQuantity);
    }

private:
    String pr_Name;
    int pr_Quantity;
};

class CustomerMailMergeDataSource : public IMailMergeDataSource
{
public:
    String get_TableName() override
    {
        return u"Customers";
    }

    CustomerMailMergeDataSource(SharedPtr<System::Collections::Generic::List<SharedPtr<ExMailMergeCustomNested::Customer>>> customers) : mRecordIndex(0)
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
        else if (fieldName == u"Order")
        {
            fieldValue = mCustomers->idx_get(mRecordIndex)->get_Orders();
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
        if (tableName == u"Orders")
        {
            return MakeObject<ExMailMergeCustomNested::OrderMailMergeDataSource>(mCustomers->idx_get(mRecordIndex)->get_Orders());
        }
        else
        {
            return nullptr;
        }
    }

private:
    bool get_IsEof()
    {
        return mRecordIndex >= mCustomers->get_Count();
    }

    SharedPtr<System::Collections::Generic::List<SharedPtr<ExMailMergeCustomNested::Customer>>> mCustomers;
    int mRecordIndex;
};

class OrderMailMergeDataSource : public IMailMergeDataSource
{
public:
    String get_TableName() override
    {
        return u"Orders";
    }

    OrderMailMergeDataSource(SharedPtr<System::Collections::Generic::List<SharedPtr<ExMailMergeCustomNested::Order>>> orders) : mRecordIndex(0)
    {
        mOrders = orders;

        // When we initialize the data source, its position must be before the first record.
        mRecordIndex = -1;
    }

    bool GetValue(String fieldName, SharedPtr<System::Object>& fieldValue) override
    {
        if (fieldName == u"Name")
        {
            fieldValue = System::ObjectExt::Box<String>(mOrders->idx_get(mRecordIndex)->get_Name());
            return true;
        }
        else if (fieldName == u"Quantity")
        {
            fieldValue = System::ObjectExt::Box<int>(mOrders->idx_get(mRecordIndex)->get_Quantity());
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
        return mRecordIndex >= mOrders->get_Count();
    }

    SharedPtr<System::Collections::Generic::List<SharedPtr<ExMailMergeCustomNested::Order>>> mOrders;
    int mRecordIndex;
};
```

## See Also

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) method


Performs a mail merge from a custom data source with mail merge regions.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSourceRoot> &dataSourceRoot)
```


| Parameter | Type | Description |
| --- | --- | --- |
| dataSourceRoot | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\& | An object that implements the custom mail merge data source root interface. |
## Remarks


Use this method to fill mail merge fields in the document with values from any custom data source such as an XML file or collections of business objects. You need to write your own classes that implement the [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/) and [IMailMergeDataSource](../../imailmergedatasource/) interfaces.

You can use this method only when [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) is **false**, that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

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

* Interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
