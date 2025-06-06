---
title: FieldLink.InsertAsBitmap
linktitle: InsertAsBitmap
articleTitle: InsertAsBitmap
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldLink InsertAsBitmap، وقم بإدارة الكائنات المرتبطة بسهولة عن طريق إدراجها كخرائط بتات عالية الجودة لتحسين الوضوح البصري.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldlink/insertasbitmap/
---
## FieldLink.InsertAsBitmap property

يحصل على أو يحدد ما إذا كان سيتم إدراج الكائن المرتبط كخريطة بتات.

```csharp
public bool InsertAsBitmap { get; set; }
```

## أمثلة

يوضح كيفية استخدام أنواع مختلفة من الحقول للارتباط بمستندات أخرى في نظام الملفات المحلي، وعرض محتوياتها.

```csharp
public void FieldLinkedObjectsAsText(InsertLinkedObjectAs insertLinkedObjectAs)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // فيما يلي ثلاثة أنواع من الحقول التي يمكننا استخدامها لعرض المحتويات من مستند مرتبط في شكل نص.
    // 1 - حقل الرابط:
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", MyDir + "Document.docx", null, true);

    // 2 - حقل DDE:
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - حقل DDEAUTO:
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.docx");
}

public void FieldLinkedObjectsAsImage(InsertLinkedObjectAs insertLinkedObjectAs)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // فيما يلي ثلاثة أنواع من الحقول التي يمكننا استخدامها لعرض المحتويات من مستند مرتبط في شكل صورة.
    // 1 - حقل الرابط:
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "MySpreadsheet.xlsx",
        "Sheet1!R2C2", true);

    // 2 - حقل DDE:
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - حقل DDEAUTO:
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
}

/// <summary>
/// استخدم منشئ المستندات لإدراج حقل LINK وتعيين خصائصه وفقًا للمعلمات.
/// </summary>
private static void InsertFieldLink(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool shouldAutoUpdate)
{
    FieldLink field = (FieldLink)builder.InsertField(FieldType.FieldLink, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;

    builder.Writeln("\n");
}

/// <summary>
/// استخدم منشئ المستندات لإدراج حقل DDE، وتعيين خصائصه وفقًا للمعلمات.
/// </summary>
private static void InsertFieldDde(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs, string progId,
    string sourceFullName, string sourceItem, bool isLinked, bool shouldAutoUpdate)
{
    FieldDde field = (FieldDde)builder.InsertField(FieldType.FieldDDE, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;

    builder.Writeln("\n");
}

/// <summary>
/// استخدم منشئ المستندات لإدراج حقل DDEAUTO وتعيين خصائصه وفقًا للمعلمات.
/// </summary>
private static void InsertFieldDdeAuto(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool isLinked)
{
    FieldDdeAuto field = (FieldDdeAuto)builder.InsertField(FieldType.FieldDDEAuto, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;
}

public enum InsertLinkedObjectAs
{
    // كائن مرتبط كنص
    Text,
    Unicode,
    Html,
    Rtf,
    // كائن مرتبط كصورة
    Picture,
    Bitmap
}
```

### أنظر أيضا

* class [FieldLink](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
