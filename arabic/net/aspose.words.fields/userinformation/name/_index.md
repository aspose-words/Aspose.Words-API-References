---
title: UserInformation.Name
second_title: Aspose.Words لمراجع .NET API
description: UserInformation ملكية. الحصول على اسم المستخدم أو تعيينه.
type: docs
weight: 50
url: /ar/net/aspose.words.fields/userinformation/name/
---
## UserInformation.Name property

الحصول على اسم المستخدم أو تعيينه.

```csharp
public string Name { get; set; }
```

### أمثلة

يوضح كيفية تعيين تفاصيل المستخدم وعرضها باستخدام الحقول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء كائن معلومات المستخدم وقم بتعيينه كمصدر بيانات للحقول التي تعرض معلومات المستخدم.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// أدخل حقول اسم المستخدم، ومعلومات المستخدم، وعنوان المستخدم، التي تعرض قيم
 // الخصائص الخاصة بكائن UserInformation الذي قمنا بإنشائه أعلاه.
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


