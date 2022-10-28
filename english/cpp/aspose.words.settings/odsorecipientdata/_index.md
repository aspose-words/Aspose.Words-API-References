---
title: OdsoRecipientData
second_title: Aspose.Words for C++ API Reference
description: Represents information about a single record within an external data source that is to be excluded from the mail merge.
type: docs
weight: 79
url: /cpp/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class


Represents information about a single record within an external data source that is to be excluded from the mail merge.

```cpp
class OdsoRecipientData : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [Clone](./clone/)() | Returns a deep clone of this object. |
| [get_Active](./get_active/)() const | Specifies whether the record from the data source shall be imported into a document when the mail merge is performed. The default value is **true**. |
| [get_Column](./get_column/)() const | Specifies the column within the data source that contains unique data for the current record. The default value is 0. |
| [get_Hash](./get_hash/)() const | Represents the hash code for this record. Sometimes Microsoft Word uses [Hash](./get_hash/) of a whole record instead of a [UniqueTag](./get_uniquetag/) value. The default value is 0. |
| [get_UniqueTag](./get_uniquetag/)() const | Specifies the contents of a given record in the column containing unique data. The default value is **null**. |
| [OdsoRecipientData](./odsorecipientdata/)() |  |
| [set_Active](./set_active/)(bool) | Specifies whether the record from the data source shall be imported into a document when the mail merge is performed. The default value is **true**. |
| [set_Column](./set_column/)(int32_t) | Specifies the column within the data source that contains unique data for the current record. The default value is 0. |
| [set_Hash](./set_hash/)(int32_t) | Represents the hash code for this record. Sometimes Microsoft Word uses [Hash](./get_hash/) of a whole record instead of a [UniqueTag](./get_uniquetag/) value. The default value is 0. |
| [set_UniqueTag](./set_uniquetag/)(const System::ArrayPtr\<uint8_t\>\&) | Specifies the contents of a given record in the column containing unique data. The default value is **null**. |

If a record shall be merged into a merged document, then no information is needed about that record. However, if a given record shall not be merged into a merged document, then the value of the unique key for that record shall be stored in the [UniqueTag](./get_uniquetag/) property of this object to indicate this exclusion. 
