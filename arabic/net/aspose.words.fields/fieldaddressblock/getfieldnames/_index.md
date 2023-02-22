---
title: FieldAddressBlock.GetFieldNames
second_title: Aspose.Words لمراجع .NET API
description: FieldAddressBlock طريقة. إرجاع مجموعة من أسماء حقول دمج المراسلات المستخدمة بواسطة الحقل.
type: docs
weight: 70
url: /ar/net/aspose.words.fields/fieldaddressblock/getfieldnames/
---
## FieldAddressBlock.GetFieldNames method

إرجاع مجموعة من أسماء حقول دمج المراسلات المستخدمة بواسطة الحقل.

```csharp
public string[] GetFieldNames()
```

### أمثلة

يوضح كيفية الحصول على أسماء حقول دمج المراسلات التي يستخدمها أحد الحقول.

```csharp
Document doc = new Document(MyDir + "Field sample - ADDRESSBLOCK.docx");

string[] addressFieldsExpect =
{
    "Company", "First Name", "Middle Name", "Last Name", "Suffix", "Address 1", "City", "State",
    "Country or Region", "Postal Code"
};

FieldAddressBlock addressBlockField = (FieldAddressBlock) doc.Range.Fields[0];
string[] addressBlockFieldNames = addressBlockField.GetFieldNames();
```

### أنظر أيضا

* class [FieldAddressBlock](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldaddressblock/)
* المجسم [Aspose.Words](../../../)


