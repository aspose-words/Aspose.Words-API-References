---
title: FieldAddressBlock.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة GetFieldNames في FieldAddressBlock. استرجع أسماء حقول دمج البريد بسهولة لتحسين عملية أتمتة مستنداتك.
type: docs
weight: 70
url: /ar/net/aspose.words.fields/fieldaddressblock/getfieldnames/
---
## FieldAddressBlock.GetFieldNames method

يعيد مجموعة من أسماء حقول دمج البريد التي يستخدمها الحقل.

```csharp
public string[] GetFieldNames()
```

## أمثلة

يوضح كيفية الحصول على أسماء حقول دمج البريد المستخدمة بواسطة الحقل.

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
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
