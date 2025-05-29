---
title: MailMerge.ExecuteADO
linktitle: ExecuteADO
articleTitle: ExecuteADO
second_title: Aspose.Words لـ .NET
description: سهّل عملية إنشاء مستنداتك باستخدام طريقة MailMerge ExecuteADO. ادمج بيانات مجموعة سجلات ADO بسهولة للحصول على نتائج فعّالة ومخصصة.
type: docs
weight: 190
url: /ar/net/aspose.words.mailmerging/mailmerge/executeado/
---
## MailMerge.ExecuteADO method

يقوم بتنفيذ دمج البريد من كائن مجموعة سجلات ADO إلى المستند.

```csharp
public void ExecuteADO(object recordset)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| recordset | Object | مجموعة سجلات ADO أو كائن السجل. |

## ملاحظات

تكون هذه الطريقة مفيدة عندما تنوي استخدام فئات Aspose.Words ككائنات COM من التعليمات البرمجية غير المُدارة مثل تطبيق تم إنشاؤه باستخدام ASP أو Visual Basic 6.0.

هذه الطريقة تتجاهلRemoveUnusedRegions خيار.

لمزيد من المعلومات راجع وصف[`Execute`](../execute/).

## أمثلة

```csharp
[VBScript]

Dim RS
Set RS = CreateObject("ADODB.Recordset")
RS.Open _
    "SELECT TOP 50 * FROM Customers ORDER BY Country, CompanyName", _
    "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"

Dim License
Set License = CreateObject("Aspose.Words.License")
License.SetLicense "C:\MyPath\MyLicense.lic"

Dim Helper
Set Helper = CreateObject("Aspose.Words.ComHelper")
Dim Doc
Set Doc = Helper.Open("CustomerLabels.doc")

Doc.MailMerge.ExecuteADO RS
Doc.Save "C:\MyPath\CustomerLabels Out VBScript.doc"
```

يوضح كيفية تشغيل دمج البريد باستخدام البيانات من مجموعة بيانات ADO.

```csharp
public void ExecuteADO()
{
    Document doc = CreateSourceDocADOMailMerge();

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
    const string command = @"SELECT ProductName, QuantityPerUnit, UnitPrice FROM Products";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    //تنفيذ دمج البريد وحفظ المستند.
    doc.MailMerge.ExecuteADO(recordset);
    doc.Save(ArtifactsDir + "MailMerge.ExecuteADO.docx");
}

/// <summary>
/// قم بإنشاء مستند فارغ واملأه بـ MERGEFIELDS التي ستقبل البيانات عند تنفيذ دمج البريد.
/// </summary>
private static Document CreateSourceDocADOMailMerge()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Write("Product:\t");
    builder.InsertField(" MERGEFIELD ProductName");
    builder.Writeln();
    builder.InsertField(" MERGEFIELD QuantityPerUnit");
    builder.Write(" for $");
    builder.InsertField(" MERGEFIELD UnitPrice");

    return doc;
}
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
