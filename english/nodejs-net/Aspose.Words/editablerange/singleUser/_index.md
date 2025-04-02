---
title: EditableRange.singleUser property
linktitle: singleUser property
articleTitle: singleUser property
second_title: Aspose.Words for NodeJs
description: "EditableRange.singleUser property. Returns or sets the single user for editable range."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words/editablerange/singleUser/
---

## EditableRange.singleUser property

Returns or sets the single user for editable range.


```js
get singleUser(): string
```

### Remarks

This editor can be stored in one of the following forms:

DOMAIN\\Username - for users whose access shall be authenticated using the current user's domain credentials.

user@domain.com - for users whose access shall be authenticated using the user's e-mail address as credentials.

user - for users whose access shall be authenticated using the current user's machine credentials.

Single user and editor group cannot be set simultaneously for the specific editable range, 
if the one is set, the other will be clear.




### See Also

* module [Aspose.Words](../../)
* class [EditableRange](../)

