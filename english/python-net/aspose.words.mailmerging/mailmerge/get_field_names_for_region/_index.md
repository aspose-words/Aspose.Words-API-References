---
title: MailMerge.get_field_names_for_region method
linktitle: get_field_names_for_region method
articleTitle: get_field_names_for_region method
second_title: Aspose.Words for Python
description: "aspose.words.mailmerging.MailMerge.get_field_names_for_region method"
type: docs
weight: 210
url: /python-net/aspose.words.mailmerging/mailmerge/get_field_names_for_region/
---

## get_field_names_for_region(region_name) {#str}

Returns a collection of mail merge field names available in the region.


```python
def get_field_names_for_region(self, region_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| region_name | str | Region name (case-insensitive). |

### Remarks

Returns full merge field names including optional prefix. Does not eliminate duplicate field names.

If document contains multiple regions with the same name the very first region is processed.

A new string array is created on every call.




## get_field_names_for_region(region_name, region_index) {#str_int}

Returns a collection of mail merge field names available in the region.


```python
def get_field_names_for_region(self, region_name: str, region_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| region_name | str | Region name (case-insensitive). |
| region_index | int | Region index (zero-based). |

### Remarks

Returns full merge field names including optional prefix. Does not eliminate duplicate field names.

If document contains multiple regions with the same name the Nth region (zero-based) is processed.

A new string array is created on every call.




## See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

