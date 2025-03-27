---
title: Field.getFieldCode method
linktitle: getFieldCode method
articleTitle: getFieldCode method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fields.Field.getFieldCode method"
type: docs
weight: 1060
url: /nodejs-net/Aspose.Words/field/getFieldCode/
---

## getFieldCode() {#default}

Returns text between field start and field separator (or field end if there is no separator).
Both field code and field result of child fields are included.


```js
getFieldCode()
```

## getFieldCode(includeChildFieldCodes) {#boolean}

Returns text between field start and field separator (or field end if there is no separator).


```js
getFieldCode(includeChildFieldCodes: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| includeChildFieldCodes | boolean | ``True`` if child field codes should be included. |

## Examples

Shows how to get a field's field code.

```js
// Open a document which contains a MERGEFIELD inside an IF field.
let doc = new aw.Document(base.myDir + "Nested fields.docx");
let fieldIf = doc.range.fields.at(0).asFieldIf();

// There are two ways of getting a field's field code:
// 1 -  Omit its inner fields:
expect(fieldIf.getFieldCode(false)).toEqual(" IF  > 0 \" (surplus of ) \" \"\" ");

// 2 -  Include its inner fields:
expect(fieldIf.getFieldCode(true)).toEqual(` IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" `);

// By default, the GetFieldCode method displays inner fields.
expect(fieldIf.getFieldCode(true)).toEqual(fieldIf.getFieldCode());
```

## See Also

* module [Aspose.Words](../../)
* class [Field](../)

