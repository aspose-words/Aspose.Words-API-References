---
title: Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion method
linktitle: GetFieldNamesForRegion
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion method. Returns a collection of mail merge field names available in the region in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## MailMerge::GetFieldNamesForRegion(const System::String\&) method


Returns a collection of mail merge field names available in the region.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| regionName | const System::String\& | Region name (case-insensitive). |
## Remarks


Returns full merge field names including optional prefix. Does not eliminate duplicate field names.

If document contains multiple regions with the same name the very first region is processed.

A new string array is created on every call.

## See Also

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::GetFieldNamesForRegion(const System::String\&, int32_t) method


Returns a collection of mail merge field names available in the region.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName, int32_t regionIndex)
```


| Parameter | Type | Description |
| --- | --- | --- |
| regionName | const System::String\& | Region name (case-insensitive). |
| regionIndex | int32_t | Region index (zero-based). |
## Remarks


Returns full merge field names including optional prefix. Does not eliminate duplicate field names.

If document contains multiple regions with the same name the Nth region (zero-based) is processed.

A new string array is created on every call.

## See Also

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
