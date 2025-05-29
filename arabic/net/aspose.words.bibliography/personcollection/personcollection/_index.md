---
title: PersonCollection
linktitle: PersonCollection
articleTitle: PersonCollection
second_title: Aspose.Words لـ .NET
description: أنشئ وأدر مجموعة ديناميكية من الأفراد باستخدام فئة PersonCollection. بسّط معالجة بياناتك وحسّن تطبيقاتك اليوم!
type: docs
weight: 10
url: /ar/net/aspose.words.bibliography/personcollection/personcollection/
---
## PersonCollection() {#constructor}

قم بتهيئة مثيل جديد لـ[`PersonCollection`](../) الصف.

```csharp
public PersonCollection()
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

---

## PersonCollection(*IEnumerable&lt;Person&gt;*) {#constructor_2}

```csharp
public PersonCollection(IEnumerable<Person> persons)
```

### أنظر أيضا

* class [Person](../../person/)
* class [PersonCollection](../)
* مساحة الاسم [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* المجسم [Aspose.Words](../../../)

---

## PersonCollection(*params Person[]*) {#constructor_1}

قم بتهيئة مثيل جديد لـ[`PersonCollection`](../) الصف.

```csharp
public PersonCollection(params Person[] persons)
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

* class [Person](../../person/)
* class [PersonCollection](../)
* مساحة الاسم [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* المجسم [Aspose.Words](../../../)
