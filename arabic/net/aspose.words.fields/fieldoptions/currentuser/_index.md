---
title: FieldOptions.CurrentUser
linktitle: CurrentUser
articleTitle: CurrentUser
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldOptions CurrentUser لإدارة معلومات المستخدم وتخصيصها بسهولة لتحسين الوظائف في تطبيقاتك.
type: docs
weight: 50
url: /ar/net/aspose.words.fields/fieldoptions/currentuser/
---
## FieldOptions.CurrentUser property

يحصل على معلومات المستخدم الحالية أو يعينها.

```csharp
public UserInformation CurrentUser { get; set; }
```

## أمثلة

يوضح كيفية تعيين تفاصيل المستخدم وعرضها باستخدام الحقول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء كائن UserInformation وقم بتعيينه كمصدر بيانات للحقول التي تعرض معلومات المستخدم.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// أدخل حقول اسم المستخدم، والأحرف الأولى للمستخدم، وعنوان المستخدم، والتي تعرض قيم
 // الخصائص الخاصة بكائن UserInformation الذي أنشأناه أعلاه.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// يحتوي كائن خيارات الحقل أيضًا على مستخدم افتراضي ثابت يمكن للحقول من كافة المستندات الرجوع إليه.
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

### أنظر أيضا

* class [UserInformation](../../userinformation/)
* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
