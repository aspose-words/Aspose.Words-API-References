---
title: IMailMergeDataSource.table_name property
linktitle: table_name property
articleTitle: table_name property
second_title: Aspose.Words for Python
description: "IMailMergeDataSource.table_name property. Returns the name of the data source."
type: docs
weight: 10
url: /python-net/aspose.words.mailmerging/imailmergedatasource/table_name/
---

## IMailMergeDataSource.table_name property

Returns the name of the data source.


```python
@property
def table_name(self) -> str:
    ...

```

### Remarks

If you are implementing [IMailMergeDataSource](../), return the name of the data
source from this property.

Aspose.Words uses this name to match against the mail merge region name specified
in the template document. The comparison between the data source name and
the mail merge region name is not case sensitive.




### See Also

* module [aspose.words.mailmerging](../../)
* class [IMailMergeDataSource](../)

