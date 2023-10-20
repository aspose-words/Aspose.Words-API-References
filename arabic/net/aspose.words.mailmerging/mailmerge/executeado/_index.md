---
title: MailMerge.ExecuteADO
linktitle: ExecuteADO
articleTitle: ExecuteADO
second_title: Aspose.Words لـ .NET
description: MailMerge ExecuteADO طريقة. تنفيذ دمج البريد من كائن ADO Recordset في المستند في C#.
type: docs
weight: 190
url: /ar/net/aspose.words.mailmerging/mailmerge/executeado/
---
## MailMerge.ExecuteADO method

تنفيذ دمج البريد من كائن ADO Recordset في المستند.

```csharp
public void ExecuteADO(object recordset)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| recordset | Object | مجموعة سجلات ADO أو كائن التسجيل. |

## ملاحظات

تكون هذه الطريقة مفيدة عندما تنوي استخدام فئات Aspose.Words ككائنات COM من تعليمات برمجية غير مُدارة مثل تطبيق تم إنشاؤه باستخدام ASP أو Visual Basic 6.0.

تتجاهل هذه الطريقةRemoveUnusedRegions خيار.

لمزيد من المعلومات انظر وصف[`Execute`](../execute/).

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

يوضح كيفية تشغيل دمج البريد مع البيانات من مجموعة بيانات ADO.

```csharp
public void ExecuteADO()
{
    Document doc = CreateSourceDocADOMailMerge();

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
    const string command = @"SELECT ProductName, QuantityPerUnit, UnitPrice FROM Products";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // تنفيذ دمج البريد وحفظ المستند.
    doc.MailMerge.ExecuteADO(recordset);
    doc.Save(ArtifactsDir + "MailMerge.ExecuteADO.docx");
}

/// <summary>
/// أنشئ مستندًا فارغًا واملأه بـ MERGEFIELDS التي ستقبل البيانات عند تنفيذ دمج البريد.
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
