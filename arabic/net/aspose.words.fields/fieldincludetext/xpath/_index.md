---
title: FieldIncludeText.XPath
linktitle: XPath
articleTitle: XPath
second_title: Aspose.Words لـ .NET
description: FieldIncludeText XPath ملكية. الحصول على XPath أو تعيينه للجزء المطلوب من ملف XML في C#.
type: docs
weight: 90
url: /ar/net/aspose.words.fields/fieldincludetext/xpath/
---
## FieldIncludeText.XPath property

الحصول على XPath أو تعيينه للجزء المطلوب من ملف XML.

```csharp
public string XPath { get; set; }
```

## أمثلة

يوضح كيفية إنشاء حقل INCLUDETEXT وتعيين خصائصه.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // فيما يلي طريقتان لاستخدام حقول INCLUDETEXT لعرض محتويات ملف XML في نظام الملفات المحلي.
    // 1 - إجراء تحويل XSL على مستند XML:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 - استخدم XPath لأخذ عناصر محددة من مستند XML:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");
}

/// <summary>
/// استخدم منشئ المستندات لإدراج حقل INCLUDETEXT بخصائص مخصصة.
/// </summary>
public FieldIncludeText CreateFieldIncludeText(DocumentBuilder builder, string sourceFullName, bool lockFields, string mimeType, string textConverter, string encoding)
{
    FieldIncludeText fieldIncludeText = (FieldIncludeText)builder.InsertField(FieldType.FieldIncludeText, true);
    fieldIncludeText.SourceFullName = sourceFullName;
    fieldIncludeText.LockFields = lockFields;
    fieldIncludeText.MimeType = mimeType;
    fieldIncludeText.TextConverter = textConverter;
    fieldIncludeText.Encoding = encoding;

    return fieldIncludeText;
}
```

### أنظر أيضا

* class [FieldIncludeText](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
