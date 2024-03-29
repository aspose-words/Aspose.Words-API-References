---
title: FieldAddressBlock.IncludeCountryOrRegionName
linktitle: IncludeCountryOrRegionName
articleTitle: IncludeCountryOrRegionName
second_title: Aspose.Words لـ .NET
description: FieldAddressBlock IncludeCountryOrRegionName ملكية. الحصول على أو تحديد ما إذا كان سيتم تضمين اسم البلد/المنطقة أم لا في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldaddressblock/includecountryorregionname/
---
## FieldAddressBlock.IncludeCountryOrRegionName property

الحصول على أو تحديد ما إذا كان سيتم تضمين اسم البلد/المنطقة أم لا.

```csharp
public string IncludeCountryOrRegionName { get; set; }
```

## أمثلة

يوضح كيفية إدراج حقل ADDRESSBLOCK.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.AreEqual(" ADDRESSBLOCK ", field.GetFieldCode());

// ضبط هذا على "2" سيشمل جميع البلدان والمناطق،
// إلا إذا كان هو المحدد في خاصية ExcludedCountryOrRegionName.
field.IncludeCountryOrRegionName = "2";
field.FormatAddressOnCountryOrRegion = true;
field.ExcludedCountryOrRegionName = "United States";
field.NameAndAddressFormat = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>";

// بشكل افتراضي، ستحتوي هذه الخاصية على معرف اللغة للحرف الأول من المستند.
// يمكننا تعيين ثقافة مختلفة للحقل لتنسيق النتيجة بهذا الشكل.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.GetFieldCode());
```

### أنظر أيضا

* class [FieldAddressBlock](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
