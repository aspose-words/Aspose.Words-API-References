---
title: UserInformation Class
linktitle: UserInformation
articleTitle: UserInformation
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.UserInformation فصل. يحدد معلومات حول المستخدم في C#.
type: docs
weight: 2790
url: /ar/net/aspose.words.fields/userinformation/
---
## UserInformation class

يحدد معلومات حول المستخدم.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class UserInformation
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [UserInformation](userinformation/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| static [DefaultUser](../../aspose.words.fields/userinformation/defaultuser/) { get; } | معلومات المستخدم الافتراضية. |
| [Address](../../aspose.words.fields/userinformation/address/) { get; set; } | الحصول على العنوان البريدي للمستخدم أو تعيينه. |
| [Initials](../../aspose.words.fields/userinformation/initials/) { get; set; } | الحصول على الأحرف الأولى من اسم المستخدم أو تعيينها. |
| [Name](../../aspose.words.fields/userinformation/name/) { get; set; } | الحصول على اسم المستخدم أو تعيينه. |

## أمثلة

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

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
