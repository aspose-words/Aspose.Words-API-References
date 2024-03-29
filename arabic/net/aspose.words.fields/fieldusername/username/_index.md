---
title: FieldUserName.UserName
linktitle: UserName
articleTitle: UserName
second_title: Aspose.Words لـ .NET
description: FieldUserName UserName ملكية. قم بإيماء أو تعيين اسم المستخدم الحالي في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldusername/username/
---
## FieldUserName.UserName property

قم بإيماء أو تعيين اسم المستخدم الحالي.

```csharp
public string UserName { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل USERNAME.

```csharp
Document doc = new Document();

// قم بإنشاء كائن معلومات المستخدم وقم بتعيينه كمصدر لمعلومات المستخدم لأي حقول نقوم بإنشائها.
UserInformation userInformation = new UserInformation();
userInformation.Name = "John Doe";
doc.FieldOptions.CurrentUser = userInformation;

DocumentBuilder builder = new DocumentBuilder(doc);

// أنشئ حقل اسم المستخدم لعرض اسم المستخدم الحالي،
// مأخوذ من كائن معلومات المستخدم الذي أنشأناه أعلاه.
FieldUserName fieldUserName = (FieldUserName)builder.InsertField(FieldType.FieldUserName, true);
Assert.AreEqual(userInformation.Name, fieldUserName.Result);

Assert.AreEqual(" USERNAME ", fieldUserName.GetFieldCode());
Assert.AreEqual("John Doe", fieldUserName.Result);

 // يمكننا تعيين هذه الخاصية لجعل الحقل الخاص بنا يتجاوز القيمة المخزنة حاليًا في كائن UserInformation.
fieldUserName.UserName = "Jane Doe";
fieldUserName.Update();

Assert.AreEqual(" USERNAME  \"Jane Doe\"", fieldUserName.GetFieldCode());
Assert.AreEqual("Jane Doe", fieldUserName.Result);

// لا يؤثر هذا على القيمة الموجودة في كائن معلومات المستخدم.
Assert.AreEqual("John Doe", doc.FieldOptions.CurrentUser.Name);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERNAME.docx");
```

### أنظر أيضا

* class [FieldUserName](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
