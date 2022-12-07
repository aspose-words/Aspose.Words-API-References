---
title: OdsoFieldMapData
second_title: Aspose.Words for C++ API Reference
description: Specifies how a column in the external data source shall be mapped to the predefined merge fields within the document. To learn more, visit the  documentation article.
type: docs
weight: 53
url: /cpp/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class


Specifies how a column in the external data source shall be mapped to the predefined merge fields within the document. To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) documentation article.

```cpp
class OdsoFieldMapData : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [Clone](./clone/)() | Returns a deep clone of this object. |
| [get_Column](./get_column/)() const | Specifies the zero-based index of the column within an external data source which shall be mapped to the local name of a specific MERGEFIELD field. The default value is 0. |
| [get_MappedName](./get_mappedname/)() const | Specifies the predefined merge field name which shall be mapped to the column number specified by the [Column](./get_column/) property within this field mapping. The default value is an empty string. |
| [get_Name](./get_name/)() const | Specifies the column name within an external data source for the column whose index is specified by the [Column](./get_column/) property. The default value is an empty string. |
| [get_Type](./get_type/)() const | Specifies if a given mail merge field has been mapped to a column in the given external data source or not. The default value is [Default](../odsofieldmappingtype/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoFieldMapData](./odsofieldmapdata/)() |  |
| [set_Column](./set_column/)(int32_t) | Specifies the zero-based index of the column within an external data source which shall be mapped to the local name of a specific MERGEFIELD field. The default value is 0. |
| [set_MappedName](./set_mappedname/)(const System::String\&) | Specifies the predefined merge field name which shall be mapped to the column number specified by the [Column](./get_column/) property within this field mapping. The default value is an empty string. |
| [set_Name](./set_name/)(const System::String\&) | Specifies the column name within an external data source for the column whose index is specified by the [Column](./get_column/) property. The default value is an empty string. |
| [set_Type](./set_type/)(Aspose::Words::Settings::OdsoFieldMappingType) | Specifies if a given mail merge field has been mapped to a column in the given external data source or not. The default value is [Default](../odsofieldmappingtype/). |
| static [Type](./type/)() |  |
## Remarks


Microsoft Word provides some predefined merge field names that it allows to insert into a document as MERGEFIELD or use in the ADDRESSBLOCK or GREETINGLINE fields. The information specified in [OdsoFieldMapData](./) allows to map one column in the external data source to a single predefined merge field.

## See Also

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words](../../)
