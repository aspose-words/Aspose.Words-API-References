---
title: RevisionGroup
second_title: Aspose.Words for Java API Reference
description: Represents a group of sequential  objects.
type: docs
weight: 486
url: /java/com.aspose.words/revisiongroup/
---

**Inheritance:**
java.lang.Object
```
public class RevisionGroup
```

Represents a group of sequential [Revision](../../com.aspose.words/revision) objects.

To learn more, visit the **Track Changes in a Document** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getText()](#getText--) | Returns inserted/deleted/moved text or description of format change. |
| [getAuthor()](#getAuthor--) | Gets the author of this revision group. |
| [getRevisionType()](#getRevisionType--) | Gets the type of revisions included in this group. |
### getText() {#getText--}
```
public String getText()
```


Returns inserted/deleted/moved text or description of format change.

**Returns:**
java.lang.String - Inserted/deleted/moved text or description of format change.
### getAuthor() {#getAuthor--}
```
public String getAuthor()
```


Gets the author of this revision group.

**Returns:**
java.lang.String - The author of this revision group.
### getRevisionType() {#getRevisionType--}
```
public int getRevisionType()
```


Gets the type of revisions included in this group.

**Returns:**
int - The type of revisions included in this group. The returned value is one of [RevisionType](../../com.aspose.words/revisiontype) constants.
