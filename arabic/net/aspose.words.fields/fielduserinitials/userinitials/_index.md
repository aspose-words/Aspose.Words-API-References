---
title: FieldUserInitials.UserInitials
linktitle: UserInitials
articleTitle: UserInitials
second_title: Aspose.Words لـ .NET
description: FieldUserInitials UserInitials ملكية. الحصول على الأحرف الأولى من اسم المستخدم الحالي أو تعيينها في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fielduserinitials/userinitials/
---
## FieldUserInitials.UserInitials property

الحصول على الأحرف الأولى من اسم المستخدم الحالي أو تعيينها.

```csharp
public string UserInitials { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل USERINITIALS.

```csharp
Document doc = new Document();

// قم بإنشاء كائن معلومات المستخدم وقم بتعيينه كمصدر لمعلومات المستخدم لأي حقول نقوم بإنشائها.
UserInformation userInformation = new UserInformation();
userInformation.Initials = "J. D.";
doc.FieldOptions.CurrentUser = userInformation;

// أنشئ حقل USERINITIALS لعرض الأحرف الأولى من اسم المستخدم الحالي،
// مأخوذ من كائن معلومات المستخدم الذي أنشأناه أعلاه.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserInitials fieldUserInitials = (FieldUserInitials)builder.InsertField(FieldType.FieldUserInitials, true);
Assert.AreEqual(userInformation.Initials, fieldUserInitials.Result);

Assert.AreEqual(" USERINITIALS ", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. D.", fieldUserInitials.Result);

 // يمكننا تعيين هذه الخاصية لجعل الحقل الخاص بنا يتجاوز القيمة المخزنة حاليًا في كائن UserInformation.
fieldUserInitials.UserInitials = "J. C.";
fieldUserInitials.Update();

Assert.AreEqual(" USERINITIALS  \"J. C.\"", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. C.", fieldUserInitials.Result);

// لا يؤثر هذا على القيمة الموجودة في كائن معلومات المستخدم.
Assert.AreEqual("J. D.", doc.FieldOptions.CurrentUser.Initials);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERINITIALS.docx");
```

### أنظر أيضا

* class [FieldUserInitials](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
