---
title: Document.startTrackRevisions method
linktitle: startTrackRevisions method
articleTitle: startTrackRevisions method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Document.startTrackRevisions method"
type: docs
weight: 690
url: /nodejs-net/aspose.words/document/startTrackRevisions/
---

## startTrackRevisions(author, dateTime) {#string_date}

Starts automatically marking all further changes you make to the document programmatically as revision changes.


```js
startTrackRevisions(author: string, dateTime: Date)
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | string | Initials of the author to use for revisions. |
| dateTime | Date | The date and time to use for revisions. |

### Remarks

If you call this method and then make some changes to the document programmatically,
save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not
recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations
as well as when using [DocumentBuilder](../../documentbuilder/)


This method does not change the [Document.trackRevisions](../trackRevisions/) option and does not use its value
for the purposes of revision tracking.




## startTrackRevisions(author) {#string}

Starts automatically marking all further changes you make to the document programmatically as revision changes.


```js
startTrackRevisions(author: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | string | Initials of the author to use for revisions. |

### Remarks

If you call this method and then make some changes to the document programmatically,
save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not
recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations
as well as when using [DocumentBuilder](../../documentbuilder/)


This method does not change the [Document.trackRevisions](../trackRevisions/) option and does not use its value
for the purposes of revision tracking.




## See Also

* module [Aspose.Words](../../)
* class [Document](../)
* method [Document.stopTrackRevisions()](../stopTrackRevisions/#default)

