---
title: FieldAutoTextList.EntryName
linktitle: EntryName
articleTitle: EntryName
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية إدارة إدخالات النص التلقائي باستخدام خاصية EntryName في FieldAutoTextList—قم بتعيين الأسماء أو استردادها بسهولة لتحرير المستندات بشكل مبسط.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldautotextlist/entryname/
---
## FieldAutoTextList.EntryName property

يحصل على اسم إدخال النص التلقائي أو يعينه.

```csharp
public string EntryName { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل AUTOTEXTLIST للاختيار من قائمة إدخالات النص التلقائي.

```csharp
public void FieldAutoTextList()
{
    Document doc = new Document();

    // قم بإنشاء مستند مسرد وقم بملئه بإدخالات نصية تلقائية.
    doc.GlossaryDocument = new GlossaryDocument();
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 1", "Contents of AutoText 1");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 2", "Contents of AutoText 2");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 3", "Contents of AutoText 3");

    DocumentBuilder builder = new DocumentBuilder(doc);

    // قم بإنشاء حقل AUTOTEXTLIST وحدد النص الذي سيعرضه الحقل في Microsoft Word.
    // تعيين النص ليطلب من المستخدم النقر بزر الماوس الأيمن على هذا الحقل لتحديد كتلة بناء النص التلقائي،
    // الذي سيتم عرض محتوياته في الحقل.
    FieldAutoTextList field = (FieldAutoTextList)builder.InsertField(FieldType.FieldAutoTextList, true);
    field.EntryName = "Right click here to select an AutoText block";
    field.ListStyle = "Heading 1";
    field.ScreenTip = "Hover tip text for AutoTextList goes here";

    Assert.AreEqual(" AUTOTEXTLIST  \"Right click here to select an AutoText block\" " +
                    "\\s \"Heading 1\" " +
                    "\\t \"Hover tip text for AutoTextList goes here\"", field.GetFieldCode());

    doc.Save(ArtifactsDir + "Field.AUTOTEXTLIST.dotx");
}

/// <summary>
/// قم بإنشاء كتلة بناء من نوع النص التلقائي وأضفها إلى مستند المصطلحات.
/// </summary>
private static void AppendAutoTextEntry(GlossaryDocument glossaryDoc, string name, string contents)
{
    BuildingBlock buildingBlock = new BuildingBlock(glossaryDoc);
    buildingBlock.Name = name;
    buildingBlock.Gallery = BuildingBlockGallery.AutoText;
    buildingBlock.Category = "General";
    buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;

    Section section = new Section(glossaryDoc);
    section.AppendChild(new Body(glossaryDoc));
    section.Body.AppendParagraph(contents);
    buildingBlock.AppendChild(section);

    glossaryDoc.AppendChild(buildingBlock);
}
```

### أنظر أيضا

* class [FieldAutoTextList](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
