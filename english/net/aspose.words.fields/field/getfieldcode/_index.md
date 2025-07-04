---
title: Field.GetFieldCode
linktitle: GetFieldCode
articleTitle: GetFieldCode
second_title: Aspose.Words for .NET
description: Discover the GetFieldCode method, effortlessly retrieve text between field start and separator, including child field codes and results. Enhance your coding efficiency!
type: docs
weight: 110
url: /net/aspose.words.fields/field/getfieldcode/
---
## GetFieldCode() {#getfieldcode}

Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.

```csharp
public string GetFieldCode()
```

## Examples

Shows how to insert a field into a document using a field code.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.That(field.Type, Is.EqualTo(FieldType.FieldDate));
Assert.That(field.GetFieldCode(), Is.EqualTo("DATE \\@ \"dddd, MMMM dd, yyyy\""));

// This overload of the InsertField method automatically updates inserted fields.
Assert.That((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1, Is.True);
```

Shows how to get a field's field code.

```csharp
// Open a document which contains a MERGEFIELD inside an IF field.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// There are two ways of getting a field's field code:
// 1 -  Omit its inner fields:
Assert.That(fieldIf.GetFieldCode(false), Is.EqualTo(" IF  > 0 \" (surplus of ) \" \"\" "));

// 2 -  Include its inner fields:
Assert.That(fieldIf.GetFieldCode(true), Is.EqualTo($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "));

// By default, the GetFieldCode method displays inner fields.
Assert.That(fieldIf.GetFieldCode(true), Is.EqualTo(fieldIf.GetFieldCode()));
```

### See Also

* class [Field](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)

---

## GetFieldCode(*bool*) {#getfieldcode_1}

Returns text between field start and field separator (or field end if there is no separator).

```csharp
public string GetFieldCode(bool includeChildFieldCodes)
```

| Parameter | Type | Description |
| --- | --- | --- |
| includeChildFieldCodes | Boolean | `true` if child field codes should be included. |

## Examples

Shows how to get a field's field code.

```csharp
// Open a document which contains a MERGEFIELD inside an IF field.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// There are two ways of getting a field's field code:
// 1 -  Omit its inner fields:
Assert.That(fieldIf.GetFieldCode(false), Is.EqualTo(" IF  > 0 \" (surplus of ) \" \"\" "));

// 2 -  Include its inner fields:
Assert.That(fieldIf.GetFieldCode(true), Is.EqualTo($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "));

// By default, the GetFieldCode method displays inner fields.
Assert.That(fieldIf.GetFieldCode(true), Is.EqualTo(fieldIf.GetFieldCode()));
```

### See Also

* class [Field](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
