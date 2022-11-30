---
title: Odso
second_title: Aspose.Words for C++ API Reference
description: Specifies the Office Data Source Object (ODSO) settings for a mail merge data source.
type: docs
weight: 40
url: /cpp/aspose.words.settings/odso/
---
## Odso class


Specifies the Office Data Source Object (ODSO) settings for a mail merge data source.

```cpp
class Odso : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [Clone](./clone/)() | Returns a deep clone of this object. |
| [get_ColumnDelimiter](./get_columndelimiter/)() const | Specifies the character which shall be interpreted as the column delimiter used to separate columns within external data sources. The default value is 0 which means there is no column delimiter defined. |
| [get_DataSource](./get_datasource/)() const | Specifies the location of the external data source to be connected to a document to perform the mail merge. The default value is an empty string. |
| [get_DataSourceType](./get_datasourcetype/)() const | Specifies the type of the external data source to be connected to as part of the ODSO connection information for this mail merge. The default value is [Default](../odsodatasourcetype/). |
| [get_FieldMapDatas](./get_fieldmapdatas/)() const | Gets a collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document. This object is never null. |
| [get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/)() const | Specifies that a hosting application shall treat the first row of data in the specified external data source as a header row containing the names of each column in the data source. The default value is **false**. |
| [get_RecipientDatas](./get_recipientdatas/)() const | Gets a collection of objects that specify inclusion/exclusion of individual records in the mail merge. This object is never null. |
| [get_TableName](./get_tablename/)() const | Specifies the particular set of data that a source shall be connected to within an external data source. The default value is an empty string. |
| [get_UdlConnectString](./get_udlconnectstring/)() const | Specifies the Universal Data Link (UDL) connection string used to connect to an external data source. The default value is an empty string. |
| [Odso](./odso/)() |  |
| [set_ColumnDelimiter](./set_columndelimiter/)(char16_t) | Setter for [Aspose::Words::Settings::Odso::get_ColumnDelimiter](./get_columndelimiter/). |
| [set_DataSource](./set_datasource/)(const System::String\&) | Specifies the location of the external data source to be connected to a document to perform the mail merge. The default value is an empty string. |
| [set_DataSourceType](./set_datasourcetype/)(Aspose::Words::Settings::OdsoDataSourceType) | Setter for [Aspose::Words::Settings::Odso::get_DataSourceType](./get_datasourcetype/). |
| [set_FieldMapDatas](./set_fieldmapdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoFieldMapDataCollection\>\&) | Sets a collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document. This object is never null. |
| [set_FirstRowContainsColumnNames](./set_firstrowcontainscolumnnames/)(bool) | Setter for [Aspose::Words::Settings::Odso::get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/). |
| [set_RecipientDatas](./set_recipientdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoRecipientDataCollection\>\&) | Sets a collection of objects that specify inclusion/exclusion of individual records in the mail merge. This object is never null. |
| [set_TableName](./set_tablename/)(const System::String\&) | Specifies the particular set of data that a source shall be connected to within an external data source. The default value is an empty string. |
| [set_UdlConnectString](./set_udlconnectstring/)(const System::String\&) | Specifies the Universal Data Link (UDL) connection string used to connect to an external data source. The default value is an empty string. |
## Remarks


ODSO seems to be the "new" way the newer Microsoft Word versions prefer to use when specifying certain types of data sources for a mail merge document. ODSO probably first appeared in Microsoft Word 2000.

The use of ODSO is poorly documented and the best way to learn how to use the properties of this object is to create a document with a desired data source manually in Microsoft Word and then open that document using Aspose.Words and examine the properties of the [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) and [Odso](../mailmergesettings/get_odso/) objects. This is a good approach to take if you want to learn how to programmatically configure a data source, for example.

You do not normally need to create objects of this class directly because ODSO settings are always available via the [Odso](../mailmergesettings/get_odso/) property.

## See Also

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words](../../)
