---
title: Document.compare method
linktitle: compare method
articleTitle: compare method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Document.compare method"
type: docs
weight: 560
url: /nodejs-net/aspose.words/document/compare/
---

## compare(document, author, dateTime) {#document_string_date}

Compares this document with another document producing changes as number of edit and format revisions [Revision](../../revision/).



```js
compare(document: Aspose.Words.Document, author: string, dateTime: Date)
```

| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../) | Document to compare. |
| author | string | Initials of the author to use for revisions. |
| dateTime | Date | The date and time to use for revisions. |

### Remarks

> **NOTE**
>
> Documents must not have revisions before comparison.




## compare(document, author, dateTime, options) {#document_string_date_compareoptions}

Compares this document with another document producing changes as a number of edit and format revisions [Revision](../../revision/).
Allows to specify comparison options using [CompareOptions](../../../aspose.words.comparing/compareoptions/).



```js
compare(document: Aspose.Words.Document, author: string, dateTime: Date, options: Aspose.Words.Comparing.CompareOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../) |  |
| author | string |  |
| dateTime | Date |  |
| options | [CompareOptions](../../../aspose.words.comparing/compareoptions/) |  |

## See Also

* module [Aspose.Words](../../)
* class [Document](../)

