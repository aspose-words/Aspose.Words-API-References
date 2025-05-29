---
title: FieldEQ.AsOfficeMath
linktitle: AsOfficeMath
articleTitle: AsOfficeMath
second_title: Aspose.Words لـ .NET
description: قم بتحويل حقول EQ باستخدام طريقة AsOfficeMath الخاصة بـ FieldEQ، وتحويلها بسهولة إلى كائنات Office Math لتحقيق تكامل سلس للمستندات.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ.AsOfficeMath method

إرجاع كائن Office Math الذي يتوافق مع حقل EQ.

```csharp
public OfficeMath AsOfficeMath()
```

### قيمة الإرجاع

إرجاع`باطل` إذا كان رمز الحقل فارغًا أو غير صالح، وإلا[`OfficeMath`](../../../aspose.words.math/officemath/) مثال.

## أمثلة

يوضح كيفية استبدال حقل EQ بـ Office Math.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

### أنظر أيضا

* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [FieldEQ](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
