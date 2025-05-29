---
title: FieldUserAddress.UserAddress
linktitle: UserAddress
articleTitle: UserAddress
second_title: Aspose.Words لـ .NET
description: أدر عناوين المستخدمين البريدية بسهولة باستخدام خاصية FieldUserAddress. استرجع معلومات المستخدم الحالية وحدّثها بسهولة لتجربة أفضل.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fielduseraddress/useraddress/
---
## FieldUserAddress.UserAddress property

يحصل على عنوان البريد الإلكتروني للمستخدم الحالي أو يعينه.

```csharp
public string UserAddress { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل USERADDRESS.

```csharp
Document doc = new Document();

// قم بإنشاء كائن UserInformation وقم بتعيينه كمصدر لمعلومات المستخدم لأي حقول نقوم بإنشائها.
UserInformation userInformation = new UserInformation();
userInformation.Address = "123 Main Street";
doc.FieldOptions.CurrentUser = userInformation;

// قم بإنشاء حقل USERADDRESS لعرض عنوان المستخدم الحالي،
//مأخوذ من كائن UserInformation الذي أنشأناه أعلاه.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserAddress fieldUserAddress = (FieldUserAddress)builder.InsertField(FieldType.FieldUserAddress, true);
Assert.AreEqual(" USERADDRESS ", fieldUserAddress.GetFieldCode());
Assert.AreEqual("123 Main Street", fieldUserAddress.Result);

// يمكننا تعيين هذه الخاصية لجعل حقلنا يتجاوز القيمة المخزنة حاليًا في كائن UserInformation.
fieldUserAddress.UserAddress = "456 North Road";
fieldUserAddress.Update();

Assert.AreEqual(" USERADDRESS  \"456 North Road\"", fieldUserAddress.GetFieldCode());
Assert.AreEqual("456 North Road", fieldUserAddress.Result);

// هذا لا يؤثر على القيمة الموجودة في كائن UserInformation.
Assert.AreEqual("123 Main Street", doc.FieldOptions.CurrentUser.Address);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERADDRESS.docx");
```

### أنظر أيضا

* class [FieldUserAddress](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
