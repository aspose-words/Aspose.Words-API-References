---
title: FieldSet.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldSet BookmarkName لإدارة وتخصيص إشاراتك المرجعية بسهولة. حسّن تجربة استخدام تطبيقك بهذه الميزة الأساسية!
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldset/bookmarkname/
---
## FieldSet.BookmarkName property

يحصل على اسم الإشارة المرجعية أو يعينه.

```csharp
public string BookmarkName { get; set; }
```

## أمثلة

يوضح كيفية إنشاء نص مرجعي باستخدام حقل SET، ثم عرضه في المستند باستخدام حقل REF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // قم بتسمية النص المضاف إليه إشارة مرجعية باستخدام حقل SET.
// يشير هذا الحقل إلى "الإشارة المرجعية" وليس إلى بنية الإشارة المرجعية التي تظهر داخل النص، بل إلى متغير مسمى.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// قم بالإشارة إلى الإشارة المرجعية بالاسم في حقل REF وعرض محتوياتها.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

### أنظر أيضا

* class [FieldSet](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
