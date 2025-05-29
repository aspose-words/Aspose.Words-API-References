---
title: LoadOptions.ConvertShapeToOfficeMath
linktitle: ConvertShapeToOfficeMath
articleTitle: ConvertShapeToOfficeMath
second_title: Aspose.Words لـ .NET
description: قم بتحويل الأشكال باستخدام EquationXML إلى كائنات Office Math بسهولة باستخدام خاصية ConvertShapeToOfficeMath في LoadOptions لتحسين وضوح المستند.
type: docs
weight: 40
url: /ar/net/aspose.words.loading/loadoptions/convertshapetoofficemath/
---
## LoadOptions.ConvertShapeToOfficeMath property

يحصل على أو يحدد ما إذا كان سيتم تحويل الأشكال باستخدام EquationXML إلى كائنات Office Math.

```csharp
public bool ConvertShapeToOfficeMath { get; set; }
```

## أمثلة

يوضح كيفية تحويل أشكال EquationXML إلى كائنات Office Math.

```csharp
LoadOptions loadOptions = new LoadOptions();

// استخدم هذا العلم لتحديد ما إذا كان سيتم تحويل الأشكال باستخدام سمات EquationXML
// إلى كائنات Office Math ثم قم بتحميل المستند.
loadOptions.ConvertShapeToOfficeMath = isConvertShapeToOfficeMath;

Document doc = new Document(MyDir + "Math shapes.docx", loadOptions);

if (isConvertShapeToOfficeMath)
{
    Assert.AreEqual(16, doc.GetChildNodes(NodeType.Shape, true).Count);
    Assert.AreEqual(34, doc.GetChildNodes(NodeType.OfficeMath, true).Count);
}
else
{
    Assert.AreEqual(24, doc.GetChildNodes(NodeType.Shape, true).Count);
    Assert.AreEqual(0, doc.GetChildNodes(NodeType.OfficeMath, true).Count);
}
```

### أنظر أيضا

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
