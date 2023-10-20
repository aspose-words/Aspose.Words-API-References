---
title: MailMerge.ExecuteWithRegionsADO
linktitle: ExecuteWithRegionsADO
articleTitle: ExecuteWithRegionsADO
second_title: Aspose.Words لـ .NET
description: MailMerge ExecuteWithRegionsADO طريقة. إجراء دمج البريد من كائن ADO Recordset في المستند باستخدام مناطق دمج البريد في C#.
type: docs
weight: 210
url: /ar/net/aspose.words.mailmerging/mailmerge/executewithregionsado/
---
## MailMerge.ExecuteWithRegionsADO method

إجراء دمج البريد من كائن ADO Recordset في المستند باستخدام مناطق دمج البريد.

```csharp
public void ExecuteWithRegionsADO(object recordset, string tableName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| recordset | Object | مجموعة سجلات ADO أو كائن التسجيل. |
| tableName | String | اسم منطقة دمج المراسلات في المستند المطلوب تعبئته. |

## ملاحظات

تكون هذه الطريقة مفيدة عندما تنوي استخدام فئات Aspose.Words ككائنات COM من تعليمات برمجية غير مُدارة مثل تطبيق تم إنشاؤه باستخدام ASP أو Visual Basic 6.0.

لمزيد من المعلومات انظر وصف[`ExecuteWithRegions`](../executewithregions/).

## أمثلة

```csharp
[VBScript]

Dim RS
Set RS = CreateObject("ADODB.Recordset")
RS.Open _
    "SELECT * FROM AsposeWordOrderDetails WHERE OrderId = 10444 ORDER BY ProductID", _
    "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"

Dim Helper
Set Helper = CreateObject("Aspose.Words.ComHelper")

Dim Doc
Set Doc = Helper.Open("Invoice.doc")

Doc.MailMerge.ExecuteWithRegionsADO RS, "OrderDetails"
Doc.Save "Invoice Out VBScript.doc"
```

يوضح كيفية تشغيل عملية دمج البريد مع مناطق متعددة، والتي تم تجميعها باستخدام بيانات من مجموعة بيانات ADO.

```csharp
public void ExecuteWithRegionsADO()
{
    Document doc = CreateSourceDocADOMailMergeWithRegions();

    // للعمل مع ADO DataSets، سنحتاج إلى إضافة مرجع إلى مكتبة كائنات بيانات Microsoft ActiveX،
    // المضمن في توزيع .NET والمخزن في "adodb.dll".
    ADODB.Connection connection = new ADODB.Connection();

    // قم بإنشاء سلسلة اتصال تشير إلى ملف قاعدة البيانات "Northwind".
    // في نظام الملفات المحلي لدينا وافتح اتصالاً.
    string connectionString = @"Provider=Microsoft.ACE.OLEDB.12.0;Data Source=" + DatabaseDir + "Northwind.accdb";
    connection.Open(connectionString);

    // قم بملء مجموعة البيانات الخاصة بنا عن طريق تشغيل أمر SQL في قاعدة البيانات الخاصة بنا.
    // يجب أن تتوافق أسماء الأعمدة في جدول النتائج
    // إلى قيم MERGEFIELDS التي ستستوعب بياناتنا.
    string command = "SELECT FirstName, LastName, City FROM Employees";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // قم بتشغيل دمج البريد على المنطقة الأولى فقط، مع ملء حقول الدمج الخاصة بها بالبيانات من مجموعة السجلات.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion1");

    // أغلق مجموعة السجلات وأعد فتحها ببيانات من استعلام SQL آخر.
    command = "SELECT * FROM Customers";

    recordset.Close();
    recordset.Open(command, connection);

    // قم بتشغيل عملية دمج بريدية ثانية في المنطقة الثانية واحفظ المستند.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion2");

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsADO.docx");

}

/// <summary>
/// قم بإنشاء مستند بمنطقتين لدمج البريد.
/// </summary>
private static Document CreateSourceDocADOMailMergeWithRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("\tEmployees: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion1");
    builder.InsertField(" MERGEFIELD FirstName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD LastName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion1");
    builder.InsertParagraph();

    builder.Writeln("\tCustomers: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion2");
    builder.InsertField(" MERGEFIELD ContactName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Address");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion2");

    return doc;
}
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
