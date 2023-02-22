---
title: FieldUserName.UserName
second_title: Aspose.Words لمراجع .NET API
description: FieldUserName ملكية. Gest أو تعيين اسم المستخدم الحالي.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldusername/username/
---
## FieldUserName.UserName property

Gest أو تعيين اسم المستخدم الحالي.

```csharp
public string UserName { get; set; }
```

### أمثلة

يوضح كيفية استخدام حقل اسم المستخدم.

```csharp
Document doc = new Document();

// إنشاء كائن معلومات المستخدم وتعيينه كمصدر لمعلومات المستخدم لأي حقول نقوم بإنشائها.
UserInformation userInformation = new UserInformation();
userInformation.Name = "John Doe";
doc.FieldOptions.CurrentUser = userInformation;

DocumentBuilder builder = new DocumentBuilder(doc);

// أنشئ حقل اسم المستخدم لعرض اسم المستخدم الحالي ،
// مأخوذ من كائن معلومات المستخدم الذي أنشأناه أعلاه.
FieldUserName fieldUserName = (FieldUserName)builder.InsertField(FieldType.FieldUserName, true);
Assert.AreEqual(userInformation.Name, fieldUserName.Result);

Assert.AreEqual(" USERNAME ", fieldUserName.GetFieldCode());
Assert.AreEqual("John Doe", fieldUserName.Result);

 // يمكننا تعيين هذه الخاصية لجعل حقلنا يتجاوز القيمة المخزنة حاليًا في كائن معلومات المستخدم.
fieldUserName.UserName = "Jane Doe";
fieldUserName.Update();

Assert.AreEqual(" USERNAME  \"Jane Doe\"", fieldUserName.GetFieldCode());
Assert.AreEqual("Jane Doe", fieldUserName.Result);

// هذا لا يؤثر على القيمة الموجودة في كائن معلومات المستخدم.
Assert.AreEqual("John Doe", doc.FieldOptions.CurrentUser.Name);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERNAME.docx");
```

### أنظر أيضا

* class [FieldUserName](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldusername/)
* المجسم [Aspose.Words](../../../)


