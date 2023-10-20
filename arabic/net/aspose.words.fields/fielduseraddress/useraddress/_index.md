---
title: FieldUserAddress.UserAddress
linktitle: UserAddress
articleTitle: UserAddress
second_title: Aspose.Words لـ .NET
description: FieldUserAddress UserAddress ملكية. الحصول على أو تعيين العنوان البريدي للمستخدم الحالي في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fielduseraddress/useraddress/
---
## FieldUserAddress.UserAddress property

الحصول على أو تعيين العنوان البريدي للمستخدم الحالي.

```csharp
public string UserAddress { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل عنوان المستخدم.

```csharp
Document doc = new Document();

// قم بإنشاء كائن معلومات المستخدم وقم بتعيينه كمصدر لمعلومات المستخدم لأي حقول نقوم بإنشائها.
UserInformation userInformation = new UserInformation();
userInformation.Address = "123 Main Street";
doc.FieldOptions.CurrentUser = userInformation;

// أنشئ حقل عنوان المستخدم لعرض عنوان المستخدم الحالي،
// مأخوذ من كائن معلومات المستخدم الذي أنشأناه أعلاه.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserAddress fieldUserAddress = (FieldUserAddress)builder.InsertField(FieldType.FieldUserAddress, true);
Assert.AreEqual(" USERADDRESS ", fieldUserAddress.GetFieldCode());
Assert.AreEqual("123 Main Street", fieldUserAddress.Result);

 // يمكننا تعيين هذه الخاصية لجعل الحقل الخاص بنا يتجاوز القيمة المخزنة حاليًا في كائن UserInformation.
fieldUserAddress.UserAddress = "456 North Road";
fieldUserAddress.Update();

Assert.AreEqual(" USERADDRESS  \"456 North Road\"", fieldUserAddress.GetFieldCode());
Assert.AreEqual("456 North Road", fieldUserAddress.Result);

// لا يؤثر هذا على القيمة الموجودة في كائن معلومات المستخدم.
Assert.AreEqual("123 Main Street", doc.FieldOptions.CurrentUser.Address);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERADDRESS.docx");
```

### أنظر أيضا

* class [FieldUserAddress](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
