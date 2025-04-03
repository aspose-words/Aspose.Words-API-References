---
title: FieldAddressBlock.getFieldNames method
linktitle: getFieldNames method
articleTitle: getFieldNames method
second_title: Aspose.Words for NodeJs
description: "FieldAddressBlock.getFieldNames method. Returns a collection of mail merge field names used by the field."
type: docs
weight: 70
url: /nodejs-net/aspose.words.fields/fieldaddressblock/getFieldNames/
---

## getFieldNames() {#default}

Returns a collection of mail merge field names used by the field.


```js
getFieldNames()
```

### Examples

Shows how to get mail merge field names used by a field.

```js
let doc = new aw.Document(base.myDir + "Field sample - ADDRESSBLOCK.docx");

string[] addressFieldsExpect =
{
  "Company", "First Name", "Middle Name", "Last Name", "Suffix", "Address 1", "City", "State",
  "Country or Region", "Postal Code"
};

let addressBlockField = (FieldAddressBlock) doc.range.fields.at(0);
string[] addressBlockFieldNames = addressBlockField.getFieldNames();
```

### See Also

* module [Aspose.Words.Fields](../../)
* class [FieldAddressBlock](../)

