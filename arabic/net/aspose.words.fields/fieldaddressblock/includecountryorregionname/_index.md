---
title: FieldAddressBlock.IncludeCountryOrRegionName
linktitle: IncludeCountryOrRegionName
articleTitle: IncludeCountryOrRegionName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldAddressBlock IncludeCountryOrRegionName لإدارة تضمين اسم البلد/المنطقة بسهولة لتحسين تنسيق العنوان.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldaddressblock/includecountryorregionname/
---
## FieldAddressBlock.IncludeCountryOrRegionName property

يحصل على أو يعين ما إذا كان سيتم تضمين اسم البلد/المنطقة.

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

// سيؤدي تعيين هذا على "2" إلى تضمين جميع البلدان والمناطق،
// ما لم يكن هو المحدد في خاصية ExcludedCountryOrRegionName.
field.IncludeCountryOrRegionName = "2";
field.FormatAddressOnCountryOrRegion = true;
field.ExcludedCountryOrRegionName = "United States";
field.NameAndAddressFormat = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>";

// بشكل افتراضي، ستحتوي هذه الخاصية على معرف اللغة للحرف الأول من المستند.
//يمكننا تعيين ثقافة مختلفة للحقل لتنسيق النتيجة على هذا النحو.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.GetFieldCode());
```

### أنظر أيضا

* class [FieldAddressBlock](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
