---
title: PersonCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words لـ .NET
description: نظّف مجموعة بياناتك الشخصية بسهولة باستخدام طريقة الإزالة لدينا، حيث نزيل جميع العناصر فورًا لبداية جديدة. بسّط إدارة بياناتك اليوم!
type: docs
weight: 50
url: /ar/net/aspose.words.bibliography/personcollection/clear/
---
## PersonCollection.Clear method

يزيل جميع العناصر من المجموعة.

```csharp
public void Clear()
```

## أمثلة

يوضح كيفية العمل مع مجموعة الأشخاص.

```csharp
// إنشاء مجموعة أشخاص جديدة.
PersonCollection persons = new PersonCollection();
Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
//إضافة شخص جديد إلى المجموعة.
persons.Add(person);
Assert.AreEqual(1, persons.Count);
// قم بإزالة الشخص من المجموعة إذا كان موجودًا.
if (persons.Contains(person))
    persons.Remove(person);
Assert.AreEqual(0, persons.Count);

// إنشاء مجموعة أشخاص تحتوي على شخصين.
persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
Assert.AreEqual(2, persons.Count);
// إزالة الشخص من المجموعة حسب الفهرس.
persons.RemoveAt(0);
Assert.AreEqual(1, persons.Count);
// إزالة جميع الأشخاص من المجموعة.
persons.Clear();
Assert.AreEqual(0, persons.Count);
```

### أنظر أيضا

* class [PersonCollection](../)
* مساحة الاسم [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* المجسم [Aspose.Words](../../../)
