---
title: Document.start_track_revisions method
linktitle: start_track_revisions method
articleTitle: start_track_revisions method
second_title: Aspose.Words for Python
description: "aspose.words.Document.start_track_revisions method"
type: docs
weight: 750
url: /python-net/aspose.words/document/start_track_revisions/
---

## start_track_revisions(author, date_time) {#str_datetime}

Starts automatically marking all further changes you make to the document programmatically as revision changes.


```python
def start_track_revisions(self, author: str, date_time: datetime.datetime):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | str | Initials of the author to use for revisions. |
| date_time | datetime.datetime | The date and time to use for revisions. |

### Remarks

If you call this method and then make some changes to the document programmatically,
save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not
recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations
as well as when using [DocumentBuilder](../../documentbuilder/)


This method does not change the [Document.track_revisions](../track_revisions/) option and does not use its value
for the purposes of revision tracking.




## start_track_revisions(author) {#str}

Starts automatically marking all further changes you make to the document programmatically as revision changes.


```python
def start_track_revisions(self, author: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | str | Initials of the author to use for revisions. |

### Remarks

If you call this method and then make some changes to the document programmatically,
save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not
recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations
as well as when using [DocumentBuilder](../../documentbuilder/)


This method does not change the [Document.track_revisions](../track_revisions/) option and does not use its value
for the purposes of revision tracking.




## See Also

* module [aspose.words](../../)
* class [Document](../)
* method [Document.stop_track_revisions()](../stop_track_revisions/#default)

