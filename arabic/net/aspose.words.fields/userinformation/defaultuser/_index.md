---
title: UserInformation.DefaultUser
second_title: Aspose.Words لمراجع .NET API
description: UserInformation ملكية. معلومات المستخدم الافتراضية .
type: docs
weight: 20
url: /ar/net/aspose.words.fields/userinformation/defaultuser/
---
## UserInformation.DefaultUser property

معلومات المستخدم الافتراضية .

```csharp
public static UserInformation DefaultUser { get; }
```

### ملاحظات

استخدم ملف[`CurrentUser`](../../fieldoptions/currentuser/)الخاصية لتحديد معلومات المستخدم لمستند واحد.

### أمثلة

يوضح كيفية تعيين تفاصيل المستخدم ، وعرضها باستخدام الحقول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء كائن معلومات المستخدم وتعيينه كمصدر بيانات للحقول التي تعرض معلومات المستخدم.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// أدخل حقول اسم المستخدم والمستخدمين و USERADDRESS التي تعرض قيم
// الخصائص الخاصة بكائن معلومات المستخدم الذي أنشأناه أعلاه. 
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// يحتوي كائن خيارات الحقل أيضًا على مستخدم افتراضي ثابت يمكن أن تشير إليه الحقول من جميع المستندات.
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

* class [UserInformation](../)
* مساحة الاسم [Aspose.Words.Fields](../../userinformation/)
* المجسم [Aspose.Words](../../../)


