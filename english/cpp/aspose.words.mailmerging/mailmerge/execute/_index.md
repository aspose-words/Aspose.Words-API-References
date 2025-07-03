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

## Examples



Shows how to merge an image from a URI as mail merge data into a MERGEFIELD. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// MERGEFIELDs with "Image:" tags will receive an image during a mail merge.
// The string after the colon in the "Image:" tag corresponds to a column name
// in the data source whose cells contain URIs of image files.
builder->InsertField(u"MERGEFIELD  Image:logo_FromWeb ");
builder->InsertField(u"MERGEFIELD  Image:logo_FromFileSystem ");

// Create a data source that contains URIs of images that we will merge.
// A URI can be a web URL that points to an image, or a local file system filename of an image file.
System::ArrayPtr<System::String> columns = System::MakeArray<System::String>({u"logo_FromWeb", u"logo_FromFileSystem"});
System::ArrayPtr<System::SharedPtr<System::Object>> URIs = System::MakeArray<System::SharedPtr<System::Object>>({System::ExplicitCast<System::Object>(get_ImageUrl()), System::ExplicitCast<System::Object>(get_ImageDir() + u"Logo.jpg")});

// Execute a mail merge on a data source with one row.
doc->get_MailMerge()->Execute(columns, URIs);

doc->Save(get_ArtifactsDir() + u"MailMergeEvent.ImageFromUrl.docx");
```

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

## See Also

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
