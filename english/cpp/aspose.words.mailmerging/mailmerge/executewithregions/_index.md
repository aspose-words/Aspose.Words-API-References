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

## See Also

* Interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
