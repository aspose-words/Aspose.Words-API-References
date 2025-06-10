---
title: Revision class
linktitle: Revision class
articleTitle: Revision class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Revision class. Represents a revision (tracked change) in a document node or style"
type: docs
weight: 1050
url: /nodejs-net/aspose.words/revision/
---

## Revision class

Represents a revision (tracked change) in a document node or style.
Use [Revision.revisionType](./revisionType/) to check the type of this revision.
To learn more, visit the [Track Changes in a Document](https://docs.aspose.com/words/nodejs-net/track-changes-in-a-document/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [author](./author/) | Gets or sets the author of this revision. Can not be empty string or ``null``. |
| [dateTime](./dateTime/) | Gets or sets the date/time of this revision. |
| [group](./group/) | Gets the revision group. Returns ``null`` if the revision does not belong to any group. |
| [parentNode](./parentNode/) | Gets the immediate parent node (owner) of this revision. This property will work for any revision type other than [RevisionType.StyleDefinitionChange](../revisiontype/#StyleDefinitionChange). |
| [parentStyle](./parentStyle/) | Gets the immediate parent style (owner) of this revision. This property will work for only for the [RevisionType.StyleDefinitionChange](../revisiontype/#StyleDefinitionChange) revision type. |
| [revisionType](./revisionType/) | Gets the type of this revision. |

### Methods

| Name | Description |
| --- | --- |
|[ accept()](./accept/#default) | Accepts this revision. |
|[ reject()](./reject/#default) | Reject this revision. |

### See Also

* module [Aspose.Words](../)

