---
title: FieldUserName.UserName
linktitle: UserName
articleTitle: UserName
second_title: Aspose.Words لـ .NET
description: أدر اسم المستخدم الحالي بسهولة باستخدام خاصية FieldUserName. حسّن تجربة المستخدم وخصص التفاعلات بسلاسة.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldusername/username/
---
## FieldUserName.UserName property

الإشارة إلى اسم المستخدم الحالي أو تعيينه.

```csharp
public string UserName { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل اسم المستخدم.

```csharp
Document doc = new Document();

// قم بإنشاء كائن UserInformation وقم بتعيينه كمصدر لمعلومات المستخدم لأي حقول نقوم بإنشائها.
UserInformation userInformation = new UserInformation();
userInformation.Name = "John Doe";
doc.FieldOptions.CurrentUser = userInformation;

DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل اسم المستخدم لعرض اسم المستخدم الحالي،
//مأخوذ من كائن UserInformation الذي أنشأناه أعلاه.
FieldUserName fieldUserName = (FieldUserName)builder.InsertField(FieldType.FieldUserName, true);
Assert.AreEqual(userInformation.Name, fieldUserName.Result);

Assert.AreEqual(" USERNAME ", fieldUserName.GetFieldCode());
Assert.AreEqual("John Doe", fieldUserName.Result);

 // يمكننا تعيين هذه الخاصية لجعل حقلنا يتجاوز القيمة المخزنة حاليًا في كائن UserInformation.
fieldUserName.UserName = "Jane Doe";
fieldUserName.Update();

Assert.AreEqual(" USERNAME  \"Jane Doe\"", fieldUserName.GetFieldCode());
Assert.AreEqual("Jane Doe", fieldUserName.Result);

// هذا لا يؤثر على القيمة الموجودة في كائن UserInformation.
Assert.AreEqual("John Doe", doc.FieldOptions.CurrentUser.Name);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERNAME.docx");
```

### أنظر أيضا

* class [FieldUserName](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
