---
title: FieldIncludeText.MimeType
linktitle: MimeType
articleTitle: MimeType
second_title: Aspose.Words لـ .NET
description: قم بإدارة ملفاتك بسهولة باستخدام خاصية FieldIncludeText MimeType، مما يسمح لك بالحصول على نوع MIME أو تعيينه بسهولة لتحقيق تكامل سلس.
type: docs
weight: 50
url: /ar/net/aspose.words.fields/fieldincludetext/mimetype/
---
## FieldIncludeText.MimeType property

يحصل على نوع MIME للملف المرجعي أو يعينه.

```csharp
public string MimeType { get; set; }
```

## أمثلة

يوضح كيفية إنشاء حقل INCLUDETEXT وتعيين خصائصه.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // فيما يلي طريقتان لاستخدام حقول INCLUDETEXT لعرض محتويات ملف XML في نظام الملفات المحلي.
    // 1 - تنفيذ تحويل XSL على مستند XML:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 - استخدام XPath لأخذ عناصر محددة من مستند XML:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");
}

/// <summary>
/// استخدم منشئ المستندات لإدراج حقل INCLUDETEXT مع خصائص مخصصة.
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
