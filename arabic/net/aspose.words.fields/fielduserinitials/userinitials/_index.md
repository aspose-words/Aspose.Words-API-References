---
title: FieldUserInitials.UserInitials
second_title: Aspose.Words لمراجع .NET API
description: FieldUserInitials ملكية. الحصول على أو تعيين الأحرف الأولى للمستخدم الحالي.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fielduserinitials/userinitials/
---
## FieldUserInitials.UserInitials property

الحصول على أو تعيين الأحرف الأولى للمستخدم الحالي.

```csharp
public string UserInitials { get; set; }
```

### أمثلة

يوضح كيفية استخدام حقل USERINITIALS.

```csharp
Document doc = new Document();

// إنشاء كائن معلومات المستخدم وتعيينه كمصدر لمعلومات المستخدم لأي حقول نقوم بإنشائها.
UserInformation userInformation = new UserInformation();
userInformation.Initials = "J. D.";
doc.FieldOptions.CurrentUser = userInformation;

// إنشاء حقل USERINITIALS لعرض الأحرف الأولى للمستخدم الحالي ،
// مأخوذ من كائن معلومات المستخدم الذي أنشأناه أعلاه.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserInitials fieldUserInitials = (FieldUserInitials)builder.InsertField(FieldType.FieldUserInitials, true);
Assert.AreEqual(userInformation.Initials, fieldUserInitials.Result);

Assert.AreEqual(" USERINITIALS ", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. D.", fieldUserInitials.Result);

 // يمكننا تعيين هذه الخاصية لجعل حقلنا يتجاوز القيمة المخزنة حاليًا في كائن معلومات المستخدم.
fieldUserInitials.UserInitials = "J. C.";
fieldUserInitials.Update();

Assert.AreEqual(" USERINITIALS  \"J. C.\"", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. C.", fieldUserInitials.Result);

// هذا لا يؤثر على القيمة الموجودة في كائن معلومات المستخدم.
Assert.AreEqual("J. D.", doc.FieldOptions.CurrentUser.Initials);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERINITIALS.docx");
```

### أنظر أيضا

* class [FieldUserInitials](../)
* مساحة الاسم [Aspose.Words.Fields](../../fielduserinitials/)
* المجسم [Aspose.Words](../../../)


