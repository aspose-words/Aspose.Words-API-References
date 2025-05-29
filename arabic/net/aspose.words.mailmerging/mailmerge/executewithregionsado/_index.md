---
title: MailMerge.ExecuteWithRegionsADO
linktitle: ExecuteWithRegionsADO
articleTitle: ExecuteWithRegionsADO
second_title: Aspose.Words لـ .NET
description: سهّل عملية إنشاء مستنداتك باستخدام طريقة MailMerge ExecuteWithRegionsADO. ادمج بيانات مجموعة سجلات ADO بسهولة للحصول على نتائج مخصصة.
type: docs
weight: 210
url: /ar/net/aspose.words.mailmerging/mailmerge/executewithregionsado/
---
## MailMerge.ExecuteWithRegionsADO method

يقوم بتنفيذ دمج البريد من كائن مجموعة سجلات ADO إلى المستند الذي يحتوي على مناطق دمج البريد.

```csharp
public void ExecuteWithRegionsADO(object recordset, string tableName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| recordset | Object | مجموعة سجلات ADO أو كائن السجل. |
| tableName | String | اسم منطقة دمج البريد في المستند الذي سيتم ملؤه. |

## ملاحظات

تكون هذه الطريقة مفيدة عندما تنوي استخدام فئات Aspose.Words ككائنات COM من التعليمات البرمجية غير المُدارة مثل تطبيق تم إنشاؤه باستخدام ASP أو Visual Basic 6.0.

لمزيد من المعلومات راجع وصف[`ExecuteWithRegions`](../executewithregions/).

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

يوضح كيفية تشغيل دمج البريد مع مناطق متعددة، والتي تم تجميعها باستخدام البيانات من مجموعة بيانات ADO.

```csharp
public void ExecuteWithRegionsADO()
{
    Document doc = CreateSourceDocADOMailMergeWithRegions();

    // للعمل مع مجموعات بيانات ADO، سنحتاج إلى إضافة مرجع إلى مكتبة كائنات بيانات Microsoft ActiveX،
    // والذي تم تضمينه في توزيع .NET وتخزينه في "adodb.dll".
    ADODB.Connection connection = new ADODB.Connection();

    // إنشاء سلسلة اتصال تشير إلى ملف قاعدة البيانات "Northwind"
    // في نظام الملفات المحلي لدينا وافتح اتصالاً.
    string connectionString = @"Provider=Microsoft.ACE.OLEDB.12.0;Data Source=" + DatabaseDir + "Northwind.accdb";
    connection.Open(connectionString);

    // قم بملء مجموعة البيانات الخاصة بنا عن طريق تشغيل أمر SQL على قاعدة البيانات الخاصة بنا.
    // يجب أن تتوافق أسماء الأعمدة في جدول النتائج
    // إلى قيم MERGEFIELDS التي ستستوعب بياناتنا.
    string command = "SELECT FirstName, LastName, City FROM Employees";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // قم بتشغيل دمج البريد على المنطقة الأولى فقط، وملء MERGEFIELDS الخاصة بها بالبيانات من مجموعة السجلات.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion1");

    // أغلق مجموعة السجلات وأعد فتحها باستخدام البيانات من استعلام SQL آخر.
    command = "SELECT * FROM Customers";

    recordset.Close();
    recordset.Open(command, connection);

    // قم بتشغيل دمج البريد الثاني على المنطقة الثانية واحفظ المستند.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion2");

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsADO.docx");

}

/// <summary>
/// إنشاء مستند يحتوي على منطقتين لدمج البريد.
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
